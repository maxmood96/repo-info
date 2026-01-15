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
$ docker pull clickhouse@sha256:5aa0c7b7149bf365cfb992709a71a766bcc80c123efd36c938988f1f01796dfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:be1427dbc3962250a6296e2332a253482175ff14db8df6504160e8f0cd0d3905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233034711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3144dcc70d52afcd6e396e49d6aed6091fd69612ba3caca1345224f8ea47b27`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.10.4.104
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:07 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:07 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e7b102770073d1f6d95c2089ecb56cfa9a7918d4bad75919ab6aba79b47bd6`  
		Last Modified: Thu, 08 Jan 2026 19:11:55 GMT  
		Size: 7.6 MB (7598430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904ed3983f2df46ff8ffee9358b3e0f045bda34688dce81f27f64989e4e46d3e`  
		Last Modified: Thu, 08 Jan 2026 22:50:18 GMT  
		Size: 195.0 MB (195029460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd44caccbfb3f32e7bb8cfcd600fdf20f0a1963ecf94a687f445dee1a2798b1`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99370367f91447171ecff260d78462b554d47f996b2b4874e5998e819d8d45f2`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388fa276530998826f116cf6967c804bbf2fd7600fc9ad1709cf36494cf3728c`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6202a22226378e2751163dbc009180e0874666d6f3d4077a8f20d05c35b6cab2`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30eb1b038690c7f9ec5f77a0ef3ebd116dfd0f9d775489eb1cbc29df8a8005b`  
		Last Modified: Thu, 08 Jan 2026 19:12:05 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4e28c1a35e8b79fdc3934ed271eadf954c6d86a15c2ab2612d0163c5209deb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54857c0a15b23b75e66117056053db556e683c09194a61c1d0bb538e144f0452`

```dockerfile
```

-	Layers:
	-	`sha256:fe400f19be7d0fa801bb49c17ba780abe81d12d672a05232ba5214e61fd541a5`  
		Last Modified: Thu, 08 Jan 2026 22:49:33 GMT  
		Size: 25.5 KB (25452 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b4598c303e7831ec6e264b5b8107da57a48dd5578e4806e88593eb8a743a4e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217601655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8d4d50816bfe9a69c71dc577892dda19d5a9dc72f34ca1e72cd4b20a214103`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.10.4.104
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:02 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:02 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:02 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709bacb4ac82edbe53ed506d91510bfdc7fef45dc73dfd57c75996eb7a44a0b`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7576644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed4fca358a4c698f6d92949e575927279b17e589124f162618d1c540f47fa50`  
		Last Modified: Thu, 08 Jan 2026 19:12:43 GMT  
		Size: 181.8 MB (181771117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7de71402c9deada2910f7035814857487a8a5dabc4a97dc09067b30027455d`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a31d4f59b1680e560226821da4bcd28dea9a472e7136be0ae69768e8605d51d`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c87861c84e1c4b70bc99dff54e0472f51abd94ec36f75942a46c1e6ce792504`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23aa42c48192f6f65919eb730ce673588ced5200875501dc9e797ccc5464121`  
		Last Modified: Thu, 08 Jan 2026 19:12:33 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1f088497f2cb4f2b0fdf233bd945ae79fdcd954f370512db1ee3be3161cde9`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b6bb9f9c4f8a9b559c49a78ba5c769286a5f2cd069162450fc2a19e0fd763fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedb543424a4cd2ce18e58d59503f72ef96cc0fd79e28c26505e397cf9237671`

```dockerfile
```

-	Layers:
	-	`sha256:fab673b4ca71434b09fcee4a08498ed2fd25fd31f3e98ef62f52a2bae91eae6d`  
		Last Modified: Thu, 08 Jan 2026 22:49:37 GMT  
		Size: 25.6 KB (25640 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10-jammy`

```console
$ docker pull clickhouse@sha256:5aa0c7b7149bf365cfb992709a71a766bcc80c123efd36c938988f1f01796dfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:be1427dbc3962250a6296e2332a253482175ff14db8df6504160e8f0cd0d3905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233034711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3144dcc70d52afcd6e396e49d6aed6091fd69612ba3caca1345224f8ea47b27`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.10.4.104
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:07 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:07 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e7b102770073d1f6d95c2089ecb56cfa9a7918d4bad75919ab6aba79b47bd6`  
		Last Modified: Thu, 08 Jan 2026 19:11:55 GMT  
		Size: 7.6 MB (7598430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904ed3983f2df46ff8ffee9358b3e0f045bda34688dce81f27f64989e4e46d3e`  
		Last Modified: Thu, 08 Jan 2026 22:50:18 GMT  
		Size: 195.0 MB (195029460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd44caccbfb3f32e7bb8cfcd600fdf20f0a1963ecf94a687f445dee1a2798b1`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99370367f91447171ecff260d78462b554d47f996b2b4874e5998e819d8d45f2`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388fa276530998826f116cf6967c804bbf2fd7600fc9ad1709cf36494cf3728c`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6202a22226378e2751163dbc009180e0874666d6f3d4077a8f20d05c35b6cab2`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30eb1b038690c7f9ec5f77a0ef3ebd116dfd0f9d775489eb1cbc29df8a8005b`  
		Last Modified: Thu, 08 Jan 2026 19:12:05 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4e28c1a35e8b79fdc3934ed271eadf954c6d86a15c2ab2612d0163c5209deb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54857c0a15b23b75e66117056053db556e683c09194a61c1d0bb538e144f0452`

```dockerfile
```

-	Layers:
	-	`sha256:fe400f19be7d0fa801bb49c17ba780abe81d12d672a05232ba5214e61fd541a5`  
		Last Modified: Thu, 08 Jan 2026 22:49:33 GMT  
		Size: 25.5 KB (25452 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b4598c303e7831ec6e264b5b8107da57a48dd5578e4806e88593eb8a743a4e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217601655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8d4d50816bfe9a69c71dc577892dda19d5a9dc72f34ca1e72cd4b20a214103`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.10.4.104
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:02 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:02 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:02 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709bacb4ac82edbe53ed506d91510bfdc7fef45dc73dfd57c75996eb7a44a0b`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7576644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed4fca358a4c698f6d92949e575927279b17e589124f162618d1c540f47fa50`  
		Last Modified: Thu, 08 Jan 2026 19:12:43 GMT  
		Size: 181.8 MB (181771117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7de71402c9deada2910f7035814857487a8a5dabc4a97dc09067b30027455d`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a31d4f59b1680e560226821da4bcd28dea9a472e7136be0ae69768e8605d51d`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c87861c84e1c4b70bc99dff54e0472f51abd94ec36f75942a46c1e6ce792504`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23aa42c48192f6f65919eb730ce673588ced5200875501dc9e797ccc5464121`  
		Last Modified: Thu, 08 Jan 2026 19:12:33 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1f088497f2cb4f2b0fdf233bd945ae79fdcd954f370512db1ee3be3161cde9`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b6bb9f9c4f8a9b559c49a78ba5c769286a5f2cd069162450fc2a19e0fd763fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedb543424a4cd2ce18e58d59503f72ef96cc0fd79e28c26505e397cf9237671`

```dockerfile
```

-	Layers:
	-	`sha256:fab673b4ca71434b09fcee4a08498ed2fd25fd31f3e98ef62f52a2bae91eae6d`  
		Last Modified: Thu, 08 Jan 2026 22:49:37 GMT  
		Size: 25.6 KB (25640 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10.4`

```console
$ docker pull clickhouse@sha256:5aa0c7b7149bf365cfb992709a71a766bcc80c123efd36c938988f1f01796dfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:be1427dbc3962250a6296e2332a253482175ff14db8df6504160e8f0cd0d3905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233034711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3144dcc70d52afcd6e396e49d6aed6091fd69612ba3caca1345224f8ea47b27`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.10.4.104
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:07 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:07 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e7b102770073d1f6d95c2089ecb56cfa9a7918d4bad75919ab6aba79b47bd6`  
		Last Modified: Thu, 08 Jan 2026 19:11:55 GMT  
		Size: 7.6 MB (7598430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904ed3983f2df46ff8ffee9358b3e0f045bda34688dce81f27f64989e4e46d3e`  
		Last Modified: Thu, 08 Jan 2026 22:50:18 GMT  
		Size: 195.0 MB (195029460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd44caccbfb3f32e7bb8cfcd600fdf20f0a1963ecf94a687f445dee1a2798b1`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99370367f91447171ecff260d78462b554d47f996b2b4874e5998e819d8d45f2`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388fa276530998826f116cf6967c804bbf2fd7600fc9ad1709cf36494cf3728c`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6202a22226378e2751163dbc009180e0874666d6f3d4077a8f20d05c35b6cab2`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30eb1b038690c7f9ec5f77a0ef3ebd116dfd0f9d775489eb1cbc29df8a8005b`  
		Last Modified: Thu, 08 Jan 2026 19:12:05 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4e28c1a35e8b79fdc3934ed271eadf954c6d86a15c2ab2612d0163c5209deb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54857c0a15b23b75e66117056053db556e683c09194a61c1d0bb538e144f0452`

```dockerfile
```

-	Layers:
	-	`sha256:fe400f19be7d0fa801bb49c17ba780abe81d12d672a05232ba5214e61fd541a5`  
		Last Modified: Thu, 08 Jan 2026 22:49:33 GMT  
		Size: 25.5 KB (25452 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b4598c303e7831ec6e264b5b8107da57a48dd5578e4806e88593eb8a743a4e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217601655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8d4d50816bfe9a69c71dc577892dda19d5a9dc72f34ca1e72cd4b20a214103`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.10.4.104
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:02 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:02 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:02 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709bacb4ac82edbe53ed506d91510bfdc7fef45dc73dfd57c75996eb7a44a0b`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7576644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed4fca358a4c698f6d92949e575927279b17e589124f162618d1c540f47fa50`  
		Last Modified: Thu, 08 Jan 2026 19:12:43 GMT  
		Size: 181.8 MB (181771117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7de71402c9deada2910f7035814857487a8a5dabc4a97dc09067b30027455d`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a31d4f59b1680e560226821da4bcd28dea9a472e7136be0ae69768e8605d51d`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c87861c84e1c4b70bc99dff54e0472f51abd94ec36f75942a46c1e6ce792504`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23aa42c48192f6f65919eb730ce673588ced5200875501dc9e797ccc5464121`  
		Last Modified: Thu, 08 Jan 2026 19:12:33 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1f088497f2cb4f2b0fdf233bd945ae79fdcd954f370512db1ee3be3161cde9`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b6bb9f9c4f8a9b559c49a78ba5c769286a5f2cd069162450fc2a19e0fd763fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedb543424a4cd2ce18e58d59503f72ef96cc0fd79e28c26505e397cf9237671`

```dockerfile
```

-	Layers:
	-	`sha256:fab673b4ca71434b09fcee4a08498ed2fd25fd31f3e98ef62f52a2bae91eae6d`  
		Last Modified: Thu, 08 Jan 2026 22:49:37 GMT  
		Size: 25.6 KB (25640 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10.4-jammy`

```console
$ docker pull clickhouse@sha256:5aa0c7b7149bf365cfb992709a71a766bcc80c123efd36c938988f1f01796dfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:be1427dbc3962250a6296e2332a253482175ff14db8df6504160e8f0cd0d3905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233034711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3144dcc70d52afcd6e396e49d6aed6091fd69612ba3caca1345224f8ea47b27`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.10.4.104
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:07 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:07 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e7b102770073d1f6d95c2089ecb56cfa9a7918d4bad75919ab6aba79b47bd6`  
		Last Modified: Thu, 08 Jan 2026 19:11:55 GMT  
		Size: 7.6 MB (7598430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904ed3983f2df46ff8ffee9358b3e0f045bda34688dce81f27f64989e4e46d3e`  
		Last Modified: Thu, 08 Jan 2026 22:50:18 GMT  
		Size: 195.0 MB (195029460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd44caccbfb3f32e7bb8cfcd600fdf20f0a1963ecf94a687f445dee1a2798b1`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99370367f91447171ecff260d78462b554d47f996b2b4874e5998e819d8d45f2`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388fa276530998826f116cf6967c804bbf2fd7600fc9ad1709cf36494cf3728c`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6202a22226378e2751163dbc009180e0874666d6f3d4077a8f20d05c35b6cab2`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30eb1b038690c7f9ec5f77a0ef3ebd116dfd0f9d775489eb1cbc29df8a8005b`  
		Last Modified: Thu, 08 Jan 2026 19:12:05 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4e28c1a35e8b79fdc3934ed271eadf954c6d86a15c2ab2612d0163c5209deb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54857c0a15b23b75e66117056053db556e683c09194a61c1d0bb538e144f0452`

```dockerfile
```

-	Layers:
	-	`sha256:fe400f19be7d0fa801bb49c17ba780abe81d12d672a05232ba5214e61fd541a5`  
		Last Modified: Thu, 08 Jan 2026 22:49:33 GMT  
		Size: 25.5 KB (25452 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b4598c303e7831ec6e264b5b8107da57a48dd5578e4806e88593eb8a743a4e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217601655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8d4d50816bfe9a69c71dc577892dda19d5a9dc72f34ca1e72cd4b20a214103`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.10.4.104
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:02 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:02 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:02 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709bacb4ac82edbe53ed506d91510bfdc7fef45dc73dfd57c75996eb7a44a0b`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7576644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed4fca358a4c698f6d92949e575927279b17e589124f162618d1c540f47fa50`  
		Last Modified: Thu, 08 Jan 2026 19:12:43 GMT  
		Size: 181.8 MB (181771117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7de71402c9deada2910f7035814857487a8a5dabc4a97dc09067b30027455d`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a31d4f59b1680e560226821da4bcd28dea9a472e7136be0ae69768e8605d51d`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c87861c84e1c4b70bc99dff54e0472f51abd94ec36f75942a46c1e6ce792504`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23aa42c48192f6f65919eb730ce673588ced5200875501dc9e797ccc5464121`  
		Last Modified: Thu, 08 Jan 2026 19:12:33 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1f088497f2cb4f2b0fdf233bd945ae79fdcd954f370512db1ee3be3161cde9`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b6bb9f9c4f8a9b559c49a78ba5c769286a5f2cd069162450fc2a19e0fd763fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedb543424a4cd2ce18e58d59503f72ef96cc0fd79e28c26505e397cf9237671`

```dockerfile
```

-	Layers:
	-	`sha256:fab673b4ca71434b09fcee4a08498ed2fd25fd31f3e98ef62f52a2bae91eae6d`  
		Last Modified: Thu, 08 Jan 2026 22:49:37 GMT  
		Size: 25.6 KB (25640 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10.4.104`

```console
$ docker pull clickhouse@sha256:5aa0c7b7149bf365cfb992709a71a766bcc80c123efd36c938988f1f01796dfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10.4.104` - linux; amd64

```console
$ docker pull clickhouse@sha256:be1427dbc3962250a6296e2332a253482175ff14db8df6504160e8f0cd0d3905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233034711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3144dcc70d52afcd6e396e49d6aed6091fd69612ba3caca1345224f8ea47b27`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.10.4.104
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:07 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:07 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e7b102770073d1f6d95c2089ecb56cfa9a7918d4bad75919ab6aba79b47bd6`  
		Last Modified: Thu, 08 Jan 2026 19:11:55 GMT  
		Size: 7.6 MB (7598430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904ed3983f2df46ff8ffee9358b3e0f045bda34688dce81f27f64989e4e46d3e`  
		Last Modified: Thu, 08 Jan 2026 22:50:18 GMT  
		Size: 195.0 MB (195029460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd44caccbfb3f32e7bb8cfcd600fdf20f0a1963ecf94a687f445dee1a2798b1`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99370367f91447171ecff260d78462b554d47f996b2b4874e5998e819d8d45f2`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388fa276530998826f116cf6967c804bbf2fd7600fc9ad1709cf36494cf3728c`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6202a22226378e2751163dbc009180e0874666d6f3d4077a8f20d05c35b6cab2`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30eb1b038690c7f9ec5f77a0ef3ebd116dfd0f9d775489eb1cbc29df8a8005b`  
		Last Modified: Thu, 08 Jan 2026 19:12:05 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.4.104` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4e28c1a35e8b79fdc3934ed271eadf954c6d86a15c2ab2612d0163c5209deb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54857c0a15b23b75e66117056053db556e683c09194a61c1d0bb538e144f0452`

```dockerfile
```

-	Layers:
	-	`sha256:fe400f19be7d0fa801bb49c17ba780abe81d12d672a05232ba5214e61fd541a5`  
		Last Modified: Thu, 08 Jan 2026 22:49:33 GMT  
		Size: 25.5 KB (25452 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10.4.104` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b4598c303e7831ec6e264b5b8107da57a48dd5578e4806e88593eb8a743a4e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217601655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8d4d50816bfe9a69c71dc577892dda19d5a9dc72f34ca1e72cd4b20a214103`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.10.4.104
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:02 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:02 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:02 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709bacb4ac82edbe53ed506d91510bfdc7fef45dc73dfd57c75996eb7a44a0b`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7576644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed4fca358a4c698f6d92949e575927279b17e589124f162618d1c540f47fa50`  
		Last Modified: Thu, 08 Jan 2026 19:12:43 GMT  
		Size: 181.8 MB (181771117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7de71402c9deada2910f7035814857487a8a5dabc4a97dc09067b30027455d`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a31d4f59b1680e560226821da4bcd28dea9a472e7136be0ae69768e8605d51d`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c87861c84e1c4b70bc99dff54e0472f51abd94ec36f75942a46c1e6ce792504`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23aa42c48192f6f65919eb730ce673588ced5200875501dc9e797ccc5464121`  
		Last Modified: Thu, 08 Jan 2026 19:12:33 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1f088497f2cb4f2b0fdf233bd945ae79fdcd954f370512db1ee3be3161cde9`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.4.104` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b6bb9f9c4f8a9b559c49a78ba5c769286a5f2cd069162450fc2a19e0fd763fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedb543424a4cd2ce18e58d59503f72ef96cc0fd79e28c26505e397cf9237671`

```dockerfile
```

-	Layers:
	-	`sha256:fab673b4ca71434b09fcee4a08498ed2fd25fd31f3e98ef62f52a2bae91eae6d`  
		Last Modified: Thu, 08 Jan 2026 22:49:37 GMT  
		Size: 25.6 KB (25640 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10.4.104-jammy`

```console
$ docker pull clickhouse@sha256:5aa0c7b7149bf365cfb992709a71a766bcc80c123efd36c938988f1f01796dfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10.4.104-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:be1427dbc3962250a6296e2332a253482175ff14db8df6504160e8f0cd0d3905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.0 MB (233034711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3144dcc70d52afcd6e396e49d6aed6091fd69612ba3caca1345224f8ea47b27`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.10.4.104
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:07 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:07 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e7b102770073d1f6d95c2089ecb56cfa9a7918d4bad75919ab6aba79b47bd6`  
		Last Modified: Thu, 08 Jan 2026 19:11:55 GMT  
		Size: 7.6 MB (7598430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904ed3983f2df46ff8ffee9358b3e0f045bda34688dce81f27f64989e4e46d3e`  
		Last Modified: Thu, 08 Jan 2026 22:50:18 GMT  
		Size: 195.0 MB (195029460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd44caccbfb3f32e7bb8cfcd600fdf20f0a1963ecf94a687f445dee1a2798b1`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99370367f91447171ecff260d78462b554d47f996b2b4874e5998e819d8d45f2`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388fa276530998826f116cf6967c804bbf2fd7600fc9ad1709cf36494cf3728c`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6202a22226378e2751163dbc009180e0874666d6f3d4077a8f20d05c35b6cab2`  
		Last Modified: Thu, 08 Jan 2026 19:11:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30eb1b038690c7f9ec5f77a0ef3ebd116dfd0f9d775489eb1cbc29df8a8005b`  
		Last Modified: Thu, 08 Jan 2026 19:12:05 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.4.104-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4e28c1a35e8b79fdc3934ed271eadf954c6d86a15c2ab2612d0163c5209deb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54857c0a15b23b75e66117056053db556e683c09194a61c1d0bb538e144f0452`

```dockerfile
```

-	Layers:
	-	`sha256:fe400f19be7d0fa801bb49c17ba780abe81d12d672a05232ba5214e61fd541a5`  
		Last Modified: Thu, 08 Jan 2026 22:49:33 GMT  
		Size: 25.5 KB (25452 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10.4.104-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b4598c303e7831ec6e264b5b8107da57a48dd5578e4806e88593eb8a743a4e89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.6 MB (217601655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb8d4d50816bfe9a69c71dc577892dda19d5a9dc72f34ca1e72cd4b20a214103`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.10.4.104
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:02 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.4.104 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:02 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:02 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709bacb4ac82edbe53ed506d91510bfdc7fef45dc73dfd57c75996eb7a44a0b`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7576644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed4fca358a4c698f6d92949e575927279b17e589124f162618d1c540f47fa50`  
		Last Modified: Thu, 08 Jan 2026 19:12:43 GMT  
		Size: 181.8 MB (181771117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d7de71402c9deada2910f7035814857487a8a5dabc4a97dc09067b30027455d`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a31d4f59b1680e560226821da4bcd28dea9a472e7136be0ae69768e8605d51d`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c87861c84e1c4b70bc99dff54e0472f51abd94ec36f75942a46c1e6ce792504`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e23aa42c48192f6f65919eb730ce673588ced5200875501dc9e797ccc5464121`  
		Last Modified: Thu, 08 Jan 2026 19:12:33 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1f088497f2cb4f2b0fdf233bd945ae79fdcd954f370512db1ee3be3161cde9`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.4.104-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b6bb9f9c4f8a9b559c49a78ba5c769286a5f2cd069162450fc2a19e0fd763fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dedb543424a4cd2ce18e58d59503f72ef96cc0fd79e28c26505e397cf9237671`

```dockerfile
```

-	Layers:
	-	`sha256:fab673b4ca71434b09fcee4a08498ed2fd25fd31f3e98ef62f52a2bae91eae6d`  
		Last Modified: Thu, 08 Jan 2026 22:49:37 GMT  
		Size: 25.6 KB (25640 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11`

```console
$ docker pull clickhouse@sha256:c7a59eac53dd03a74d5d0e40395a3c7b7c4e056396791382550ec552760b61fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:ad0f60a5ccc37b08721434659b22a15a9061ad6241ed4995ff22db7d19af1275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234045255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3c1d5404011aa403528209054a64cbaac3e074b21eccf77592bda78b070906`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:29 GMT
ARG VERSION=25.11.6.11
# Thu, 08 Jan 2026 19:10:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:30 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:30 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb14fd12795a68aeafb457d019391ea985cdb6996ed8d1f44875d37ceec3e1c`  
		Last Modified: Thu, 08 Jan 2026 19:12:03 GMT  
		Size: 7.6 MB (7598434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b215a01d29af0b26366646d7ffad0c39c0920d5063ccb599f781a13fd751f407`  
		Last Modified: Thu, 08 Jan 2026 19:12:17 GMT  
		Size: 196.0 MB (196039976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc7af9ff02f3d456b559f3fda263684f9ec78a9c7097a5d4e2fe9986eecd797`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae5dd9bc47edc8a8c24a0b1325a0fae54cdfe77ec18c70bf074fdb3307c3a55`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead0fbe5361cfa602245b41aa2834ad2947b1066dbd47cc88def966c512b35fa`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cce43d6a7cfa7852209693df4b7d0c47cf78e59920b6a94eecefc822513dc50`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2993dc97437ad1ffe46d0bf9eb76f0dd89f0767b9d9a996ab0dc221f93c7aaee`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:82b5a1ff5ecc63b41e49696942ab3652022ebd9f5898f085fa4ccf5303dfe588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72af1317014de4e5791987e7eaf1971b7a113f2f33d8aa28f975b9350589a70e`

```dockerfile
```

-	Layers:
	-	`sha256:cddc016287b1032951f42cf0a3f5340b647c87d7cf833b466f456cbf3ba2870b`  
		Last Modified: Thu, 08 Jan 2026 22:49:39 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:63436b2af97abd78c6c84cb3fb114c7df623270e8d256869f3d123d5a11cd9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218955162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31088df241ff9bdea78906f3298e8bab388cbc9b06485e5c740bc6a6e6e7c462`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.11.6.11
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:04 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:05 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:05 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709bacb4ac82edbe53ed506d91510bfdc7fef45dc73dfd57c75996eb7a44a0b`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7576644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc2780d8bc7ac75e506b23fd15459ee0c2ec0492a09fbb376ddfb3022fb97b2`  
		Last Modified: Thu, 08 Jan 2026 19:11:48 GMT  
		Size: 183.1 MB (183124602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfeff6874a0ae0352e4b9c33ac56c553c7cbe573651fe33159b8db84f88d2b6e`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fefd59d6dc8189bf1b47ad12f6f45e4878bbc5dc63a68c93539a882df7e63e`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6dea5c2aad496faa4d97282e93f534e7647ca208162a11f4cf860880a898`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6718dccf931000a4c58ec5846aef4c7e2828af9eb606af60a71e1a83e6c62f3b`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7067044a142ee468d9a43fc0dd53b8021b337fa86d1b0064a6d4bd39a28c8781`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5aadb2838490c7921fac3a33d6ce4819ebb8c1db8ec7b286295281d361792aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9acb80e2e08ab759bde89d9529ea7d7cd6696e12b31d0f7fa6769652d642d7`

```dockerfile
```

-	Layers:
	-	`sha256:eb161c141096482128fec757d4b841101eba148808f048b25ccb09bd726f34de`  
		Last Modified: Thu, 08 Jan 2026 22:49:42 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11-jammy`

```console
$ docker pull clickhouse@sha256:c7a59eac53dd03a74d5d0e40395a3c7b7c4e056396791382550ec552760b61fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ad0f60a5ccc37b08721434659b22a15a9061ad6241ed4995ff22db7d19af1275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234045255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3c1d5404011aa403528209054a64cbaac3e074b21eccf77592bda78b070906`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:29 GMT
ARG VERSION=25.11.6.11
# Thu, 08 Jan 2026 19:10:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:30 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:30 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb14fd12795a68aeafb457d019391ea985cdb6996ed8d1f44875d37ceec3e1c`  
		Last Modified: Thu, 08 Jan 2026 19:12:03 GMT  
		Size: 7.6 MB (7598434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b215a01d29af0b26366646d7ffad0c39c0920d5063ccb599f781a13fd751f407`  
		Last Modified: Thu, 08 Jan 2026 19:12:17 GMT  
		Size: 196.0 MB (196039976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc7af9ff02f3d456b559f3fda263684f9ec78a9c7097a5d4e2fe9986eecd797`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae5dd9bc47edc8a8c24a0b1325a0fae54cdfe77ec18c70bf074fdb3307c3a55`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead0fbe5361cfa602245b41aa2834ad2947b1066dbd47cc88def966c512b35fa`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cce43d6a7cfa7852209693df4b7d0c47cf78e59920b6a94eecefc822513dc50`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2993dc97437ad1ffe46d0bf9eb76f0dd89f0767b9d9a996ab0dc221f93c7aaee`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:82b5a1ff5ecc63b41e49696942ab3652022ebd9f5898f085fa4ccf5303dfe588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72af1317014de4e5791987e7eaf1971b7a113f2f33d8aa28f975b9350589a70e`

```dockerfile
```

-	Layers:
	-	`sha256:cddc016287b1032951f42cf0a3f5340b647c87d7cf833b466f456cbf3ba2870b`  
		Last Modified: Thu, 08 Jan 2026 22:49:39 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:63436b2af97abd78c6c84cb3fb114c7df623270e8d256869f3d123d5a11cd9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218955162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31088df241ff9bdea78906f3298e8bab388cbc9b06485e5c740bc6a6e6e7c462`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.11.6.11
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:04 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:05 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:05 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709bacb4ac82edbe53ed506d91510bfdc7fef45dc73dfd57c75996eb7a44a0b`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7576644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc2780d8bc7ac75e506b23fd15459ee0c2ec0492a09fbb376ddfb3022fb97b2`  
		Last Modified: Thu, 08 Jan 2026 19:11:48 GMT  
		Size: 183.1 MB (183124602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfeff6874a0ae0352e4b9c33ac56c553c7cbe573651fe33159b8db84f88d2b6e`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fefd59d6dc8189bf1b47ad12f6f45e4878bbc5dc63a68c93539a882df7e63e`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6dea5c2aad496faa4d97282e93f534e7647ca208162a11f4cf860880a898`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6718dccf931000a4c58ec5846aef4c7e2828af9eb606af60a71e1a83e6c62f3b`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7067044a142ee468d9a43fc0dd53b8021b337fa86d1b0064a6d4bd39a28c8781`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5aadb2838490c7921fac3a33d6ce4819ebb8c1db8ec7b286295281d361792aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9acb80e2e08ab759bde89d9529ea7d7cd6696e12b31d0f7fa6769652d642d7`

```dockerfile
```

-	Layers:
	-	`sha256:eb161c141096482128fec757d4b841101eba148808f048b25ccb09bd726f34de`  
		Last Modified: Thu, 08 Jan 2026 22:49:42 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.6`

```console
$ docker pull clickhouse@sha256:c7a59eac53dd03a74d5d0e40395a3c7b7c4e056396791382550ec552760b61fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:ad0f60a5ccc37b08721434659b22a15a9061ad6241ed4995ff22db7d19af1275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234045255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3c1d5404011aa403528209054a64cbaac3e074b21eccf77592bda78b070906`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:29 GMT
ARG VERSION=25.11.6.11
# Thu, 08 Jan 2026 19:10:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:30 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:30 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb14fd12795a68aeafb457d019391ea985cdb6996ed8d1f44875d37ceec3e1c`  
		Last Modified: Thu, 08 Jan 2026 19:12:03 GMT  
		Size: 7.6 MB (7598434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b215a01d29af0b26366646d7ffad0c39c0920d5063ccb599f781a13fd751f407`  
		Last Modified: Thu, 08 Jan 2026 19:12:17 GMT  
		Size: 196.0 MB (196039976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc7af9ff02f3d456b559f3fda263684f9ec78a9c7097a5d4e2fe9986eecd797`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae5dd9bc47edc8a8c24a0b1325a0fae54cdfe77ec18c70bf074fdb3307c3a55`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead0fbe5361cfa602245b41aa2834ad2947b1066dbd47cc88def966c512b35fa`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cce43d6a7cfa7852209693df4b7d0c47cf78e59920b6a94eecefc822513dc50`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2993dc97437ad1ffe46d0bf9eb76f0dd89f0767b9d9a996ab0dc221f93c7aaee`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:82b5a1ff5ecc63b41e49696942ab3652022ebd9f5898f085fa4ccf5303dfe588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72af1317014de4e5791987e7eaf1971b7a113f2f33d8aa28f975b9350589a70e`

```dockerfile
```

-	Layers:
	-	`sha256:cddc016287b1032951f42cf0a3f5340b647c87d7cf833b466f456cbf3ba2870b`  
		Last Modified: Thu, 08 Jan 2026 22:49:39 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:63436b2af97abd78c6c84cb3fb114c7df623270e8d256869f3d123d5a11cd9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218955162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31088df241ff9bdea78906f3298e8bab388cbc9b06485e5c740bc6a6e6e7c462`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.11.6.11
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:04 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:05 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:05 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709bacb4ac82edbe53ed506d91510bfdc7fef45dc73dfd57c75996eb7a44a0b`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7576644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc2780d8bc7ac75e506b23fd15459ee0c2ec0492a09fbb376ddfb3022fb97b2`  
		Last Modified: Thu, 08 Jan 2026 19:11:48 GMT  
		Size: 183.1 MB (183124602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfeff6874a0ae0352e4b9c33ac56c553c7cbe573651fe33159b8db84f88d2b6e`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fefd59d6dc8189bf1b47ad12f6f45e4878bbc5dc63a68c93539a882df7e63e`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6dea5c2aad496faa4d97282e93f534e7647ca208162a11f4cf860880a898`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6718dccf931000a4c58ec5846aef4c7e2828af9eb606af60a71e1a83e6c62f3b`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7067044a142ee468d9a43fc0dd53b8021b337fa86d1b0064a6d4bd39a28c8781`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5aadb2838490c7921fac3a33d6ce4819ebb8c1db8ec7b286295281d361792aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9acb80e2e08ab759bde89d9529ea7d7cd6696e12b31d0f7fa6769652d642d7`

```dockerfile
```

-	Layers:
	-	`sha256:eb161c141096482128fec757d4b841101eba148808f048b25ccb09bd726f34de`  
		Last Modified: Thu, 08 Jan 2026 22:49:42 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.6-jammy`

```console
$ docker pull clickhouse@sha256:c7a59eac53dd03a74d5d0e40395a3c7b7c4e056396791382550ec552760b61fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ad0f60a5ccc37b08721434659b22a15a9061ad6241ed4995ff22db7d19af1275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234045255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3c1d5404011aa403528209054a64cbaac3e074b21eccf77592bda78b070906`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:29 GMT
ARG VERSION=25.11.6.11
# Thu, 08 Jan 2026 19:10:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:30 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:30 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb14fd12795a68aeafb457d019391ea985cdb6996ed8d1f44875d37ceec3e1c`  
		Last Modified: Thu, 08 Jan 2026 19:12:03 GMT  
		Size: 7.6 MB (7598434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b215a01d29af0b26366646d7ffad0c39c0920d5063ccb599f781a13fd751f407`  
		Last Modified: Thu, 08 Jan 2026 19:12:17 GMT  
		Size: 196.0 MB (196039976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc7af9ff02f3d456b559f3fda263684f9ec78a9c7097a5d4e2fe9986eecd797`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae5dd9bc47edc8a8c24a0b1325a0fae54cdfe77ec18c70bf074fdb3307c3a55`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead0fbe5361cfa602245b41aa2834ad2947b1066dbd47cc88def966c512b35fa`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cce43d6a7cfa7852209693df4b7d0c47cf78e59920b6a94eecefc822513dc50`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2993dc97437ad1ffe46d0bf9eb76f0dd89f0767b9d9a996ab0dc221f93c7aaee`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:82b5a1ff5ecc63b41e49696942ab3652022ebd9f5898f085fa4ccf5303dfe588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72af1317014de4e5791987e7eaf1971b7a113f2f33d8aa28f975b9350589a70e`

```dockerfile
```

-	Layers:
	-	`sha256:cddc016287b1032951f42cf0a3f5340b647c87d7cf833b466f456cbf3ba2870b`  
		Last Modified: Thu, 08 Jan 2026 22:49:39 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:63436b2af97abd78c6c84cb3fb114c7df623270e8d256869f3d123d5a11cd9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218955162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31088df241ff9bdea78906f3298e8bab388cbc9b06485e5c740bc6a6e6e7c462`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.11.6.11
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:04 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:05 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:05 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709bacb4ac82edbe53ed506d91510bfdc7fef45dc73dfd57c75996eb7a44a0b`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7576644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc2780d8bc7ac75e506b23fd15459ee0c2ec0492a09fbb376ddfb3022fb97b2`  
		Last Modified: Thu, 08 Jan 2026 19:11:48 GMT  
		Size: 183.1 MB (183124602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfeff6874a0ae0352e4b9c33ac56c553c7cbe573651fe33159b8db84f88d2b6e`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fefd59d6dc8189bf1b47ad12f6f45e4878bbc5dc63a68c93539a882df7e63e`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6dea5c2aad496faa4d97282e93f534e7647ca208162a11f4cf860880a898`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6718dccf931000a4c58ec5846aef4c7e2828af9eb606af60a71e1a83e6c62f3b`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7067044a142ee468d9a43fc0dd53b8021b337fa86d1b0064a6d4bd39a28c8781`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5aadb2838490c7921fac3a33d6ce4819ebb8c1db8ec7b286295281d361792aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9acb80e2e08ab759bde89d9529ea7d7cd6696e12b31d0f7fa6769652d642d7`

```dockerfile
```

-	Layers:
	-	`sha256:eb161c141096482128fec757d4b841101eba148808f048b25ccb09bd726f34de`  
		Last Modified: Thu, 08 Jan 2026 22:49:42 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.6.11`

```console
$ docker pull clickhouse@sha256:c7a59eac53dd03a74d5d0e40395a3c7b7c4e056396791382550ec552760b61fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.6.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:ad0f60a5ccc37b08721434659b22a15a9061ad6241ed4995ff22db7d19af1275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234045255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3c1d5404011aa403528209054a64cbaac3e074b21eccf77592bda78b070906`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:29 GMT
ARG VERSION=25.11.6.11
# Thu, 08 Jan 2026 19:10:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:30 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:30 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb14fd12795a68aeafb457d019391ea985cdb6996ed8d1f44875d37ceec3e1c`  
		Last Modified: Thu, 08 Jan 2026 19:12:03 GMT  
		Size: 7.6 MB (7598434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b215a01d29af0b26366646d7ffad0c39c0920d5063ccb599f781a13fd751f407`  
		Last Modified: Thu, 08 Jan 2026 19:12:17 GMT  
		Size: 196.0 MB (196039976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc7af9ff02f3d456b559f3fda263684f9ec78a9c7097a5d4e2fe9986eecd797`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae5dd9bc47edc8a8c24a0b1325a0fae54cdfe77ec18c70bf074fdb3307c3a55`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead0fbe5361cfa602245b41aa2834ad2947b1066dbd47cc88def966c512b35fa`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cce43d6a7cfa7852209693df4b7d0c47cf78e59920b6a94eecefc822513dc50`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2993dc97437ad1ffe46d0bf9eb76f0dd89f0767b9d9a996ab0dc221f93c7aaee`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.6.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:82b5a1ff5ecc63b41e49696942ab3652022ebd9f5898f085fa4ccf5303dfe588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72af1317014de4e5791987e7eaf1971b7a113f2f33d8aa28f975b9350589a70e`

```dockerfile
```

-	Layers:
	-	`sha256:cddc016287b1032951f42cf0a3f5340b647c87d7cf833b466f456cbf3ba2870b`  
		Last Modified: Thu, 08 Jan 2026 22:49:39 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.6.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:63436b2af97abd78c6c84cb3fb114c7df623270e8d256869f3d123d5a11cd9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218955162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31088df241ff9bdea78906f3298e8bab388cbc9b06485e5c740bc6a6e6e7c462`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.11.6.11
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:04 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:05 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:05 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709bacb4ac82edbe53ed506d91510bfdc7fef45dc73dfd57c75996eb7a44a0b`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7576644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc2780d8bc7ac75e506b23fd15459ee0c2ec0492a09fbb376ddfb3022fb97b2`  
		Last Modified: Thu, 08 Jan 2026 19:11:48 GMT  
		Size: 183.1 MB (183124602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfeff6874a0ae0352e4b9c33ac56c553c7cbe573651fe33159b8db84f88d2b6e`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fefd59d6dc8189bf1b47ad12f6f45e4878bbc5dc63a68c93539a882df7e63e`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6dea5c2aad496faa4d97282e93f534e7647ca208162a11f4cf860880a898`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6718dccf931000a4c58ec5846aef4c7e2828af9eb606af60a71e1a83e6c62f3b`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7067044a142ee468d9a43fc0dd53b8021b337fa86d1b0064a6d4bd39a28c8781`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.6.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5aadb2838490c7921fac3a33d6ce4819ebb8c1db8ec7b286295281d361792aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9acb80e2e08ab759bde89d9529ea7d7cd6696e12b31d0f7fa6769652d642d7`

```dockerfile
```

-	Layers:
	-	`sha256:eb161c141096482128fec757d4b841101eba148808f048b25ccb09bd726f34de`  
		Last Modified: Thu, 08 Jan 2026 22:49:42 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.6.11-jammy`

```console
$ docker pull clickhouse@sha256:c7a59eac53dd03a74d5d0e40395a3c7b7c4e056396791382550ec552760b61fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.6.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ad0f60a5ccc37b08721434659b22a15a9061ad6241ed4995ff22db7d19af1275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (234045255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3c1d5404011aa403528209054a64cbaac3e074b21eccf77592bda78b070906`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:29 GMT
ARG VERSION=25.11.6.11
# Thu, 08 Jan 2026 19:10:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:30 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:30 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb14fd12795a68aeafb457d019391ea985cdb6996ed8d1f44875d37ceec3e1c`  
		Last Modified: Thu, 08 Jan 2026 19:12:03 GMT  
		Size: 7.6 MB (7598434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b215a01d29af0b26366646d7ffad0c39c0920d5063ccb599f781a13fd751f407`  
		Last Modified: Thu, 08 Jan 2026 19:12:17 GMT  
		Size: 196.0 MB (196039976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc7af9ff02f3d456b559f3fda263684f9ec78a9c7097a5d4e2fe9986eecd797`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae5dd9bc47edc8a8c24a0b1325a0fae54cdfe77ec18c70bf074fdb3307c3a55`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead0fbe5361cfa602245b41aa2834ad2947b1066dbd47cc88def966c512b35fa`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cce43d6a7cfa7852209693df4b7d0c47cf78e59920b6a94eecefc822513dc50`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2993dc97437ad1ffe46d0bf9eb76f0dd89f0767b9d9a996ab0dc221f93c7aaee`  
		Last Modified: Thu, 08 Jan 2026 19:12:02 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.6.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:82b5a1ff5ecc63b41e49696942ab3652022ebd9f5898f085fa4ccf5303dfe588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72af1317014de4e5791987e7eaf1971b7a113f2f33d8aa28f975b9350589a70e`

```dockerfile
```

-	Layers:
	-	`sha256:cddc016287b1032951f42cf0a3f5340b647c87d7cf833b466f456cbf3ba2870b`  
		Last Modified: Thu, 08 Jan 2026 22:49:39 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.6.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:63436b2af97abd78c6c84cb3fb114c7df623270e8d256869f3d123d5a11cd9c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218955162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31088df241ff9bdea78906f3298e8bab388cbc9b06485e5c740bc6a6e6e7c462`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:35 GMT
ARG VERSION=25.11.6.11
# Thu, 08 Jan 2026 19:10:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:04 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:04 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.6.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:05 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:05 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:05 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3709bacb4ac82edbe53ed506d91510bfdc7fef45dc73dfd57c75996eb7a44a0b`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7576644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc2780d8bc7ac75e506b23fd15459ee0c2ec0492a09fbb376ddfb3022fb97b2`  
		Last Modified: Thu, 08 Jan 2026 19:11:48 GMT  
		Size: 183.1 MB (183124602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfeff6874a0ae0352e4b9c33ac56c553c7cbe573651fe33159b8db84f88d2b6e`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9fefd59d6dc8189bf1b47ad12f6f45e4878bbc5dc63a68c93539a882df7e63e`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6dea5c2aad496faa4d97282e93f534e7647ca208162a11f4cf860880a898`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6718dccf931000a4c58ec5846aef4c7e2828af9eb606af60a71e1a83e6c62f3b`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 357.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7067044a142ee468d9a43fc0dd53b8021b337fa86d1b0064a6d4bd39a28c8781`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.6.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5aadb2838490c7921fac3a33d6ce4819ebb8c1db8ec7b286295281d361792aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9acb80e2e08ab759bde89d9529ea7d7cd6696e12b31d0f7fa6769652d642d7`

```dockerfile
```

-	Layers:
	-	`sha256:eb161c141096482128fec757d4b841101eba148808f048b25ccb09bd726f34de`  
		Last Modified: Thu, 08 Jan 2026 22:49:42 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12`

```console
$ docker pull clickhouse@sha256:1f72b42e0277e70befc6720dfb81d05e531098ae38a1d80d725822bc52177f19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12` - linux; amd64

```console
$ docker pull clickhouse@sha256:5953fee9e7204deb6f57bbe95d98eff05b8c2df4daf7f8d1d8b8ef33d6528ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246459240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636fde9e3ac86031d6a1794d93486f1bf1fbf2230c17118dcb2d8e6ddd053603`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:27 GMT
ARG VERSION=25.12.2.54
# Thu, 08 Jan 2026 19:10:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:10:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:10:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:10:55 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:10:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:10:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:10:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:10:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3abfc4054c194a9cefd39672b876926786daed6977f9d2ddf3ea9b01b910c9`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7598404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4189e8d3cf58cc07948ac61090fd9dfd06da555f31bb8b322e8bfe55347f4a07`  
		Last Modified: Thu, 08 Jan 2026 23:03:42 GMT  
		Size: 208.5 MB (208453993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cf40e289eb4959252ffeb1cb4f64fcaa5face990d33c2b2d477cde08f7ade0`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb906d86fdcfa4424f5d4aeefb7472e97a615ed92eea646ce31ca5e370fa177`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbce7a23330521b82b0a971f543d66e041c3472ce7e30c121a46ee0fa40aba7`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6aa7eb7e363161bae220c5567d1871e3c1c2e3fa6885df01d2882387d2cb45`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf9cf136a2beff175113910bebef5b091fc483c264c0ae3a3fa3764fedd3729`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a3e602c43c1d9d713b904900b0a8e349817a6dbb4c515a8314351a88e7396154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9531cd0eaa9793dba37b157482f5ddc91e934f158bf681c15c5b32d56f716011`

```dockerfile
```

-	Layers:
	-	`sha256:9e9be73a5e40575f6888ce51736c3d9eb361e4536666baa2be83c49d4da978a1`  
		Last Modified: Thu, 08 Jan 2026 22:49:57 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d22c2066bc823cc910b240e095539b5d7bfcf044877ae48936b0a743dee57f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228337624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b98dff4813c02c2ca9c601e5b203b505c2b25c4319886374e5e6320cd157ec9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:30 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:30 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:30 GMT
ARG VERSION=25.12.2.54
# Thu, 08 Jan 2026 19:10:30 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:10:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:10:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:10:59 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:10:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:10:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:10:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:10:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fbf56b5e5593a01971f7c17ff8d743c8577deb81ab12d416edca4c9c6cf2ac`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 7.6 MB (7576596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32371df79fab30e208eac2b1c9871e4195e7c47bf998975649bbb3c719ebebcd`  
		Last Modified: Thu, 08 Jan 2026 19:12:00 GMT  
		Size: 192.5 MB (192507107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567586fd3e2cc17abf4f94350ea19c433f7dc0e7c8276c5f2d60a418df33d86e`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8413fdeae9cadb3fcb66db640fefb6968c58e31e69a8b2dec117de4498d32f`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b87f902825889df29cf646d68088c890c427f535e40eb9940cff4e1d8f8f31`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913dc5a5a01d10c560bc137b67cd99c69e80f16172577b4f1add4f8b619320c`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c1f4e3c0cad0c8550f8db416a508c05ed7897e9ca309c54dd91593711f45c4`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a37f54b2f2cf98654a1902f1a7d7a7b1286720dc36ec34d842d14a114d7ff9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765fcaf50f0b876c1377173e649ed2a4b0afab5000c3579adddc3da93e7b319c`

```dockerfile
```

-	Layers:
	-	`sha256:c24485efdb6114adcfa8b08132bb411ae76e7c7d63fb8e9b9ec1f6bf2b151236`  
		Last Modified: Thu, 08 Jan 2026 22:50:00 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12-jammy`

```console
$ docker pull clickhouse@sha256:1f72b42e0277e70befc6720dfb81d05e531098ae38a1d80d725822bc52177f19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:5953fee9e7204deb6f57bbe95d98eff05b8c2df4daf7f8d1d8b8ef33d6528ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246459240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636fde9e3ac86031d6a1794d93486f1bf1fbf2230c17118dcb2d8e6ddd053603`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:27 GMT
ARG VERSION=25.12.2.54
# Thu, 08 Jan 2026 19:10:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:10:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:10:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:10:55 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:10:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:10:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:10:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:10:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3abfc4054c194a9cefd39672b876926786daed6977f9d2ddf3ea9b01b910c9`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7598404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4189e8d3cf58cc07948ac61090fd9dfd06da555f31bb8b322e8bfe55347f4a07`  
		Last Modified: Thu, 08 Jan 2026 23:03:42 GMT  
		Size: 208.5 MB (208453993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cf40e289eb4959252ffeb1cb4f64fcaa5face990d33c2b2d477cde08f7ade0`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb906d86fdcfa4424f5d4aeefb7472e97a615ed92eea646ce31ca5e370fa177`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbce7a23330521b82b0a971f543d66e041c3472ce7e30c121a46ee0fa40aba7`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6aa7eb7e363161bae220c5567d1871e3c1c2e3fa6885df01d2882387d2cb45`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf9cf136a2beff175113910bebef5b091fc483c264c0ae3a3fa3764fedd3729`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a3e602c43c1d9d713b904900b0a8e349817a6dbb4c515a8314351a88e7396154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9531cd0eaa9793dba37b157482f5ddc91e934f158bf681c15c5b32d56f716011`

```dockerfile
```

-	Layers:
	-	`sha256:9e9be73a5e40575f6888ce51736c3d9eb361e4536666baa2be83c49d4da978a1`  
		Last Modified: Thu, 08 Jan 2026 22:49:57 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d22c2066bc823cc910b240e095539b5d7bfcf044877ae48936b0a743dee57f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228337624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b98dff4813c02c2ca9c601e5b203b505c2b25c4319886374e5e6320cd157ec9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:30 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:30 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:30 GMT
ARG VERSION=25.12.2.54
# Thu, 08 Jan 2026 19:10:30 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:10:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:10:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:10:59 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:10:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:10:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:10:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:10:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fbf56b5e5593a01971f7c17ff8d743c8577deb81ab12d416edca4c9c6cf2ac`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 7.6 MB (7576596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32371df79fab30e208eac2b1c9871e4195e7c47bf998975649bbb3c719ebebcd`  
		Last Modified: Thu, 08 Jan 2026 19:12:00 GMT  
		Size: 192.5 MB (192507107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567586fd3e2cc17abf4f94350ea19c433f7dc0e7c8276c5f2d60a418df33d86e`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8413fdeae9cadb3fcb66db640fefb6968c58e31e69a8b2dec117de4498d32f`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b87f902825889df29cf646d68088c890c427f535e40eb9940cff4e1d8f8f31`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913dc5a5a01d10c560bc137b67cd99c69e80f16172577b4f1add4f8b619320c`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c1f4e3c0cad0c8550f8db416a508c05ed7897e9ca309c54dd91593711f45c4`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a37f54b2f2cf98654a1902f1a7d7a7b1286720dc36ec34d842d14a114d7ff9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765fcaf50f0b876c1377173e649ed2a4b0afab5000c3579adddc3da93e7b319c`

```dockerfile
```

-	Layers:
	-	`sha256:c24485efdb6114adcfa8b08132bb411ae76e7c7d63fb8e9b9ec1f6bf2b151236`  
		Last Modified: Thu, 08 Jan 2026 22:50:00 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.3`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.12.3-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.12.3.21`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.12.3.21-jammy`

```console
$ docker pull clickhouse@sha256:eb37f58646a901dc7727cf448cae36daaefaba79de33b5058dab79aa4c04aefb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 0

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:653cb9229eda62bc04bd4e510f2041c8fb06efbfdd019a1d21d45b505e6d14dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:c2a571f9dfef3f001098070f4c6b1fc3e3fd75872a77fdaf7d6181fc0556ee85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.5 MB (206457436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e7338ecfb8bf6113378cf003350c70b61b23cc72a70a3648d0be682930beb1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:11:51 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:11:51 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:11:51 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:11:51 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:11:51 GMT
ARG VERSION=25.3.12.8
# Thu, 08 Jan 2026 19:11:51 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:17 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:17 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8782cf2349bb2fb1b00e10ce60710ae1af100fca7d98f99f9918b85b2ef8b0d`  
		Last Modified: Thu, 08 Jan 2026 19:12:49 GMT  
		Size: 7.2 MB (7151595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68830b7f49463159b3e914885480588d352d3ec70aac32865a6b737f45ec5c20`  
		Last Modified: Thu, 08 Jan 2026 19:13:02 GMT  
		Size: 168.9 MB (168898800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60abce0e7ac81894275904781aafa9873f3af428a0819283a4de44ed365fd3a0`  
		Last Modified: Thu, 08 Jan 2026 19:12:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618c2beb2d01c3b8c362b022eebfa83ce71f1f491d51eee19a6a3755372bbc14`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0afe23dbf3b7f90b8e557f06ba46da20b4d4668c674a57832ffea9d28f9f5fd`  
		Last Modified: Thu, 08 Jan 2026 19:12:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d2f006bfafe7d75a9fee9ebe08d9b5f1e387962bf8752390bb75599e1741cb`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2069b526349770156d28b82ff03c8c4c7c53670544d6c4c54b7713c6826283`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:319b03bea50f93d122269a14c6135d2b3b0ef74e8b2093f1bcf65bcf721fef64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e32a262905dc65dcf752d877da4ecf20b295d8b85771ce99adb56ec130cc226`

```dockerfile
```

-	Layers:
	-	`sha256:88cd4942ca47c6b3ea550644f421ea5cecc4ea84ee667f05add2b6a1a0fa32f1`  
		Last Modified: Thu, 08 Jan 2026 22:50:16 GMT  
		Size: 25.2 KB (25224 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7970d3cc5cc031c0290ccb671fa46894b6805db8af18abced20235e7106b6942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193931499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dadacbc5c51f4a138095df6567436d7c0cac2c4754c779dc73a14e4e84d5e60`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:12:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:12:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:12:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:12:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:12:44 GMT
ARG VERSION=25.3.12.8
# Thu, 08 Jan 2026 19:12:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:13:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:13:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:13:10 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:13:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:13:10 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:13:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:13:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d95af39e59444c09cb443f89e889cd21e9e9d3e2cd76fdc5efd671592e0f7b`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 7.1 MB (7127092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164e62baf70bd251a4c621328e780694afa8cfd6c1b928f9e80adbeb5060d673`  
		Last Modified: Thu, 08 Jan 2026 19:14:15 GMT  
		Size: 158.6 MB (158550294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825844614a007e4466ed108dbf15aa59ade6f865d99e8f243786104f91bd9588`  
		Last Modified: Thu, 08 Jan 2026 19:24:42 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6965723b5236ad94d47879e6dc7b98c168eeca27bebb508c7b9ee33d1aa5da`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6eae6a5ecc616b92df3662388f302eed5ab6519db30d091f8592191a6d3c16f`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed1a2b63a3ee05dd94415f96c55ee8b13bb3738307af69dbef9dad5774fc72`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff34ece922e69ccfa0afa9152264bc945c300115326c987f84d7d580ca0927a`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ffc215d037729fc9e90bc49db4181d601da3937c3d9c0b944dd14515a69df80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc0b172d620db156b33bac0d3285257f29bff6d44bf44aaac0df13d0c26c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:0d56b63d76568f4bb69fff6b601119706f58b18e2ef3a2b661a9d65cdcd2810e`  
		Last Modified: Thu, 08 Jan 2026 22:50:19 GMT  
		Size: 25.4 KB (25411 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:653cb9229eda62bc04bd4e510f2041c8fb06efbfdd019a1d21d45b505e6d14dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:c2a571f9dfef3f001098070f4c6b1fc3e3fd75872a77fdaf7d6181fc0556ee85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.5 MB (206457436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e7338ecfb8bf6113378cf003350c70b61b23cc72a70a3648d0be682930beb1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:11:51 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:11:51 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:11:51 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:11:51 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:11:51 GMT
ARG VERSION=25.3.12.8
# Thu, 08 Jan 2026 19:11:51 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:17 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:17 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8782cf2349bb2fb1b00e10ce60710ae1af100fca7d98f99f9918b85b2ef8b0d`  
		Last Modified: Thu, 08 Jan 2026 19:12:49 GMT  
		Size: 7.2 MB (7151595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68830b7f49463159b3e914885480588d352d3ec70aac32865a6b737f45ec5c20`  
		Last Modified: Thu, 08 Jan 2026 19:13:02 GMT  
		Size: 168.9 MB (168898800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60abce0e7ac81894275904781aafa9873f3af428a0819283a4de44ed365fd3a0`  
		Last Modified: Thu, 08 Jan 2026 19:12:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618c2beb2d01c3b8c362b022eebfa83ce71f1f491d51eee19a6a3755372bbc14`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0afe23dbf3b7f90b8e557f06ba46da20b4d4668c674a57832ffea9d28f9f5fd`  
		Last Modified: Thu, 08 Jan 2026 19:12:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d2f006bfafe7d75a9fee9ebe08d9b5f1e387962bf8752390bb75599e1741cb`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2069b526349770156d28b82ff03c8c4c7c53670544d6c4c54b7713c6826283`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:319b03bea50f93d122269a14c6135d2b3b0ef74e8b2093f1bcf65bcf721fef64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e32a262905dc65dcf752d877da4ecf20b295d8b85771ce99adb56ec130cc226`

```dockerfile
```

-	Layers:
	-	`sha256:88cd4942ca47c6b3ea550644f421ea5cecc4ea84ee667f05add2b6a1a0fa32f1`  
		Last Modified: Thu, 08 Jan 2026 22:50:16 GMT  
		Size: 25.2 KB (25224 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7970d3cc5cc031c0290ccb671fa46894b6805db8af18abced20235e7106b6942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193931499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dadacbc5c51f4a138095df6567436d7c0cac2c4754c779dc73a14e4e84d5e60`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:12:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:12:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:12:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:12:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:12:44 GMT
ARG VERSION=25.3.12.8
# Thu, 08 Jan 2026 19:12:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:13:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:13:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:13:10 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:13:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:13:10 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:13:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:13:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d95af39e59444c09cb443f89e889cd21e9e9d3e2cd76fdc5efd671592e0f7b`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 7.1 MB (7127092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164e62baf70bd251a4c621328e780694afa8cfd6c1b928f9e80adbeb5060d673`  
		Last Modified: Thu, 08 Jan 2026 19:14:15 GMT  
		Size: 158.6 MB (158550294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825844614a007e4466ed108dbf15aa59ade6f865d99e8f243786104f91bd9588`  
		Last Modified: Thu, 08 Jan 2026 19:24:42 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6965723b5236ad94d47879e6dc7b98c168eeca27bebb508c7b9ee33d1aa5da`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6eae6a5ecc616b92df3662388f302eed5ab6519db30d091f8592191a6d3c16f`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed1a2b63a3ee05dd94415f96c55ee8b13bb3738307af69dbef9dad5774fc72`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff34ece922e69ccfa0afa9152264bc945c300115326c987f84d7d580ca0927a`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ffc215d037729fc9e90bc49db4181d601da3937c3d9c0b944dd14515a69df80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc0b172d620db156b33bac0d3285257f29bff6d44bf44aaac0df13d0c26c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:0d56b63d76568f4bb69fff6b601119706f58b18e2ef3a2b661a9d65cdcd2810e`  
		Last Modified: Thu, 08 Jan 2026 22:50:19 GMT  
		Size: 25.4 KB (25411 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.12`

```console
$ docker pull clickhouse@sha256:653cb9229eda62bc04bd4e510f2041c8fb06efbfdd019a1d21d45b505e6d14dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.12` - linux; amd64

```console
$ docker pull clickhouse@sha256:c2a571f9dfef3f001098070f4c6b1fc3e3fd75872a77fdaf7d6181fc0556ee85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.5 MB (206457436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e7338ecfb8bf6113378cf003350c70b61b23cc72a70a3648d0be682930beb1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:11:51 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:11:51 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:11:51 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:11:51 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:11:51 GMT
ARG VERSION=25.3.12.8
# Thu, 08 Jan 2026 19:11:51 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:17 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:17 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8782cf2349bb2fb1b00e10ce60710ae1af100fca7d98f99f9918b85b2ef8b0d`  
		Last Modified: Thu, 08 Jan 2026 19:12:49 GMT  
		Size: 7.2 MB (7151595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68830b7f49463159b3e914885480588d352d3ec70aac32865a6b737f45ec5c20`  
		Last Modified: Thu, 08 Jan 2026 19:13:02 GMT  
		Size: 168.9 MB (168898800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60abce0e7ac81894275904781aafa9873f3af428a0819283a4de44ed365fd3a0`  
		Last Modified: Thu, 08 Jan 2026 19:12:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618c2beb2d01c3b8c362b022eebfa83ce71f1f491d51eee19a6a3755372bbc14`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0afe23dbf3b7f90b8e557f06ba46da20b4d4668c674a57832ffea9d28f9f5fd`  
		Last Modified: Thu, 08 Jan 2026 19:12:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d2f006bfafe7d75a9fee9ebe08d9b5f1e387962bf8752390bb75599e1741cb`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2069b526349770156d28b82ff03c8c4c7c53670544d6c4c54b7713c6826283`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:319b03bea50f93d122269a14c6135d2b3b0ef74e8b2093f1bcf65bcf721fef64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e32a262905dc65dcf752d877da4ecf20b295d8b85771ce99adb56ec130cc226`

```dockerfile
```

-	Layers:
	-	`sha256:88cd4942ca47c6b3ea550644f421ea5cecc4ea84ee667f05add2b6a1a0fa32f1`  
		Last Modified: Thu, 08 Jan 2026 22:50:16 GMT  
		Size: 25.2 KB (25224 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.12` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7970d3cc5cc031c0290ccb671fa46894b6805db8af18abced20235e7106b6942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193931499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dadacbc5c51f4a138095df6567436d7c0cac2c4754c779dc73a14e4e84d5e60`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:12:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:12:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:12:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:12:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:12:44 GMT
ARG VERSION=25.3.12.8
# Thu, 08 Jan 2026 19:12:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:13:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:13:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:13:10 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:13:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:13:10 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:13:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:13:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d95af39e59444c09cb443f89e889cd21e9e9d3e2cd76fdc5efd671592e0f7b`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 7.1 MB (7127092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164e62baf70bd251a4c621328e780694afa8cfd6c1b928f9e80adbeb5060d673`  
		Last Modified: Thu, 08 Jan 2026 19:14:15 GMT  
		Size: 158.6 MB (158550294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825844614a007e4466ed108dbf15aa59ade6f865d99e8f243786104f91bd9588`  
		Last Modified: Thu, 08 Jan 2026 19:24:42 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6965723b5236ad94d47879e6dc7b98c168eeca27bebb508c7b9ee33d1aa5da`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6eae6a5ecc616b92df3662388f302eed5ab6519db30d091f8592191a6d3c16f`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed1a2b63a3ee05dd94415f96c55ee8b13bb3738307af69dbef9dad5774fc72`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff34ece922e69ccfa0afa9152264bc945c300115326c987f84d7d580ca0927a`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ffc215d037729fc9e90bc49db4181d601da3937c3d9c0b944dd14515a69df80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc0b172d620db156b33bac0d3285257f29bff6d44bf44aaac0df13d0c26c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:0d56b63d76568f4bb69fff6b601119706f58b18e2ef3a2b661a9d65cdcd2810e`  
		Last Modified: Thu, 08 Jan 2026 22:50:19 GMT  
		Size: 25.4 KB (25411 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.12-jammy`

```console
$ docker pull clickhouse@sha256:653cb9229eda62bc04bd4e510f2041c8fb06efbfdd019a1d21d45b505e6d14dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.12-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:c2a571f9dfef3f001098070f4c6b1fc3e3fd75872a77fdaf7d6181fc0556ee85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.5 MB (206457436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e7338ecfb8bf6113378cf003350c70b61b23cc72a70a3648d0be682930beb1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:11:51 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:11:51 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:11:51 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:11:51 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:11:51 GMT
ARG VERSION=25.3.12.8
# Thu, 08 Jan 2026 19:11:51 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:17 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:17 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8782cf2349bb2fb1b00e10ce60710ae1af100fca7d98f99f9918b85b2ef8b0d`  
		Last Modified: Thu, 08 Jan 2026 19:12:49 GMT  
		Size: 7.2 MB (7151595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68830b7f49463159b3e914885480588d352d3ec70aac32865a6b737f45ec5c20`  
		Last Modified: Thu, 08 Jan 2026 19:13:02 GMT  
		Size: 168.9 MB (168898800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60abce0e7ac81894275904781aafa9873f3af428a0819283a4de44ed365fd3a0`  
		Last Modified: Thu, 08 Jan 2026 19:12:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618c2beb2d01c3b8c362b022eebfa83ce71f1f491d51eee19a6a3755372bbc14`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0afe23dbf3b7f90b8e557f06ba46da20b4d4668c674a57832ffea9d28f9f5fd`  
		Last Modified: Thu, 08 Jan 2026 19:12:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d2f006bfafe7d75a9fee9ebe08d9b5f1e387962bf8752390bb75599e1741cb`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2069b526349770156d28b82ff03c8c4c7c53670544d6c4c54b7713c6826283`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:319b03bea50f93d122269a14c6135d2b3b0ef74e8b2093f1bcf65bcf721fef64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e32a262905dc65dcf752d877da4ecf20b295d8b85771ce99adb56ec130cc226`

```dockerfile
```

-	Layers:
	-	`sha256:88cd4942ca47c6b3ea550644f421ea5cecc4ea84ee667f05add2b6a1a0fa32f1`  
		Last Modified: Thu, 08 Jan 2026 22:50:16 GMT  
		Size: 25.2 KB (25224 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.12-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7970d3cc5cc031c0290ccb671fa46894b6805db8af18abced20235e7106b6942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193931499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dadacbc5c51f4a138095df6567436d7c0cac2c4754c779dc73a14e4e84d5e60`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:12:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:12:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:12:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:12:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:12:44 GMT
ARG VERSION=25.3.12.8
# Thu, 08 Jan 2026 19:12:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:13:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:13:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:13:10 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:13:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:13:10 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:13:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:13:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d95af39e59444c09cb443f89e889cd21e9e9d3e2cd76fdc5efd671592e0f7b`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 7.1 MB (7127092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164e62baf70bd251a4c621328e780694afa8cfd6c1b928f9e80adbeb5060d673`  
		Last Modified: Thu, 08 Jan 2026 19:14:15 GMT  
		Size: 158.6 MB (158550294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825844614a007e4466ed108dbf15aa59ade6f865d99e8f243786104f91bd9588`  
		Last Modified: Thu, 08 Jan 2026 19:24:42 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6965723b5236ad94d47879e6dc7b98c168eeca27bebb508c7b9ee33d1aa5da`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6eae6a5ecc616b92df3662388f302eed5ab6519db30d091f8592191a6d3c16f`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed1a2b63a3ee05dd94415f96c55ee8b13bb3738307af69dbef9dad5774fc72`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff34ece922e69ccfa0afa9152264bc945c300115326c987f84d7d580ca0927a`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ffc215d037729fc9e90bc49db4181d601da3937c3d9c0b944dd14515a69df80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc0b172d620db156b33bac0d3285257f29bff6d44bf44aaac0df13d0c26c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:0d56b63d76568f4bb69fff6b601119706f58b18e2ef3a2b661a9d65cdcd2810e`  
		Last Modified: Thu, 08 Jan 2026 22:50:19 GMT  
		Size: 25.4 KB (25411 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.12.8`

```console
$ docker pull clickhouse@sha256:653cb9229eda62bc04bd4e510f2041c8fb06efbfdd019a1d21d45b505e6d14dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.12.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:c2a571f9dfef3f001098070f4c6b1fc3e3fd75872a77fdaf7d6181fc0556ee85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.5 MB (206457436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e7338ecfb8bf6113378cf003350c70b61b23cc72a70a3648d0be682930beb1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:11:51 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:11:51 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:11:51 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:11:51 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:11:51 GMT
ARG VERSION=25.3.12.8
# Thu, 08 Jan 2026 19:11:51 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:17 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:17 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8782cf2349bb2fb1b00e10ce60710ae1af100fca7d98f99f9918b85b2ef8b0d`  
		Last Modified: Thu, 08 Jan 2026 19:12:49 GMT  
		Size: 7.2 MB (7151595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68830b7f49463159b3e914885480588d352d3ec70aac32865a6b737f45ec5c20`  
		Last Modified: Thu, 08 Jan 2026 19:13:02 GMT  
		Size: 168.9 MB (168898800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60abce0e7ac81894275904781aafa9873f3af428a0819283a4de44ed365fd3a0`  
		Last Modified: Thu, 08 Jan 2026 19:12:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618c2beb2d01c3b8c362b022eebfa83ce71f1f491d51eee19a6a3755372bbc14`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0afe23dbf3b7f90b8e557f06ba46da20b4d4668c674a57832ffea9d28f9f5fd`  
		Last Modified: Thu, 08 Jan 2026 19:12:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d2f006bfafe7d75a9fee9ebe08d9b5f1e387962bf8752390bb75599e1741cb`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2069b526349770156d28b82ff03c8c4c7c53670544d6c4c54b7713c6826283`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.12.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:319b03bea50f93d122269a14c6135d2b3b0ef74e8b2093f1bcf65bcf721fef64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e32a262905dc65dcf752d877da4ecf20b295d8b85771ce99adb56ec130cc226`

```dockerfile
```

-	Layers:
	-	`sha256:88cd4942ca47c6b3ea550644f421ea5cecc4ea84ee667f05add2b6a1a0fa32f1`  
		Last Modified: Thu, 08 Jan 2026 22:50:16 GMT  
		Size: 25.2 KB (25224 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.12.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7970d3cc5cc031c0290ccb671fa46894b6805db8af18abced20235e7106b6942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193931499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dadacbc5c51f4a138095df6567436d7c0cac2c4754c779dc73a14e4e84d5e60`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:12:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:12:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:12:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:12:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:12:44 GMT
ARG VERSION=25.3.12.8
# Thu, 08 Jan 2026 19:12:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:13:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:13:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:13:10 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:13:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:13:10 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:13:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:13:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d95af39e59444c09cb443f89e889cd21e9e9d3e2cd76fdc5efd671592e0f7b`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 7.1 MB (7127092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164e62baf70bd251a4c621328e780694afa8cfd6c1b928f9e80adbeb5060d673`  
		Last Modified: Thu, 08 Jan 2026 19:14:15 GMT  
		Size: 158.6 MB (158550294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825844614a007e4466ed108dbf15aa59ade6f865d99e8f243786104f91bd9588`  
		Last Modified: Thu, 08 Jan 2026 19:24:42 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6965723b5236ad94d47879e6dc7b98c168eeca27bebb508c7b9ee33d1aa5da`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6eae6a5ecc616b92df3662388f302eed5ab6519db30d091f8592191a6d3c16f`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed1a2b63a3ee05dd94415f96c55ee8b13bb3738307af69dbef9dad5774fc72`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff34ece922e69ccfa0afa9152264bc945c300115326c987f84d7d580ca0927a`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.12.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ffc215d037729fc9e90bc49db4181d601da3937c3d9c0b944dd14515a69df80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc0b172d620db156b33bac0d3285257f29bff6d44bf44aaac0df13d0c26c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:0d56b63d76568f4bb69fff6b601119706f58b18e2ef3a2b661a9d65cdcd2810e`  
		Last Modified: Thu, 08 Jan 2026 22:50:19 GMT  
		Size: 25.4 KB (25411 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.12.8-jammy`

```console
$ docker pull clickhouse@sha256:653cb9229eda62bc04bd4e510f2041c8fb06efbfdd019a1d21d45b505e6d14dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.12.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:c2a571f9dfef3f001098070f4c6b1fc3e3fd75872a77fdaf7d6181fc0556ee85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.5 MB (206457436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2e7338ecfb8bf6113378cf003350c70b61b23cc72a70a3648d0be682930beb1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:11:51 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:11:51 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:11:51 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:11:51 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:11:51 GMT
ARG VERSION=25.3.12.8
# Thu, 08 Jan 2026 19:11:51 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:17 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:17 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8782cf2349bb2fb1b00e10ce60710ae1af100fca7d98f99f9918b85b2ef8b0d`  
		Last Modified: Thu, 08 Jan 2026 19:12:49 GMT  
		Size: 7.2 MB (7151595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68830b7f49463159b3e914885480588d352d3ec70aac32865a6b737f45ec5c20`  
		Last Modified: Thu, 08 Jan 2026 19:13:02 GMT  
		Size: 168.9 MB (168898800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60abce0e7ac81894275904781aafa9873f3af428a0819283a4de44ed365fd3a0`  
		Last Modified: Thu, 08 Jan 2026 19:12:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618c2beb2d01c3b8c362b022eebfa83ce71f1f491d51eee19a6a3755372bbc14`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0afe23dbf3b7f90b8e557f06ba46da20b4d4668c674a57832ffea9d28f9f5fd`  
		Last Modified: Thu, 08 Jan 2026 19:12:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d2f006bfafe7d75a9fee9ebe08d9b5f1e387962bf8752390bb75599e1741cb`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2069b526349770156d28b82ff03c8c4c7c53670544d6c4c54b7713c6826283`  
		Last Modified: Thu, 08 Jan 2026 19:12:48 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.12.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:319b03bea50f93d122269a14c6135d2b3b0ef74e8b2093f1bcf65bcf721fef64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e32a262905dc65dcf752d877da4ecf20b295d8b85771ce99adb56ec130cc226`

```dockerfile
```

-	Layers:
	-	`sha256:88cd4942ca47c6b3ea550644f421ea5cecc4ea84ee667f05add2b6a1a0fa32f1`  
		Last Modified: Thu, 08 Jan 2026 22:50:16 GMT  
		Size: 25.2 KB (25224 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.12.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7970d3cc5cc031c0290ccb671fa46894b6805db8af18abced20235e7106b6942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193931499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dadacbc5c51f4a138095df6567436d7c0cac2c4754c779dc73a14e4e84d5e60`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:12:44 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:12:44 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:12:44 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:12:44 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:12:44 GMT
ARG VERSION=25.3.12.8
# Thu, 08 Jan 2026 19:12:44 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:13:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:13:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:13:10 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:13:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.12.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:13:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:13:10 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:13:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:13:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d95af39e59444c09cb443f89e889cd21e9e9d3e2cd76fdc5efd671592e0f7b`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 7.1 MB (7127092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164e62baf70bd251a4c621328e780694afa8cfd6c1b928f9e80adbeb5060d673`  
		Last Modified: Thu, 08 Jan 2026 19:14:15 GMT  
		Size: 158.6 MB (158550294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825844614a007e4466ed108dbf15aa59ade6f865d99e8f243786104f91bd9588`  
		Last Modified: Thu, 08 Jan 2026 19:24:42 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6965723b5236ad94d47879e6dc7b98c168eeca27bebb508c7b9ee33d1aa5da`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6eae6a5ecc616b92df3662388f302eed5ab6519db30d091f8592191a6d3c16f`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ed1a2b63a3ee05dd94415f96c55ee8b13bb3738307af69dbef9dad5774fc72`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff34ece922e69ccfa0afa9152264bc945c300115326c987f84d7d580ca0927a`  
		Last Modified: Thu, 08 Jan 2026 19:13:54 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.12.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ffc215d037729fc9e90bc49db4181d601da3937c3d9c0b944dd14515a69df80f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc0b172d620db156b33bac0d3285257f29bff6d44bf44aaac0df13d0c26c2b7`

```dockerfile
```

-	Layers:
	-	`sha256:0d56b63d76568f4bb69fff6b601119706f58b18e2ef3a2b661a9d65cdcd2810e`  
		Last Modified: Thu, 08 Jan 2026 22:50:19 GMT  
		Size: 25.4 KB (25411 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:a69ebd347d0d510f27cc014e12d81700695cf1ac9702c4d83f2271857d63cc06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:0dea61ef4d2853bb7f4c3d8cca9fd016c27056b1c46a5eee9dae6d2faf464ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229071355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3056c0f79d082117b6f9f67fdade0abeb17b75970237686a9783ce88bc38aa11`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:27 GMT
ARG VERSION=25.8.14.17
# Thu, 08 Jan 2026 19:10:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:54 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3abfc4054c194a9cefd39672b876926786daed6977f9d2ddf3ea9b01b910c9`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7598404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c0f2cd97f6479d1c26b36ef1106078cd4c1dc763123be19b8dd808c4761af8`  
		Last Modified: Thu, 08 Jan 2026 19:12:17 GMT  
		Size: 191.1 MB (191066131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b81cdfd3a9f3262abbed81e1b5455ed5841e5364a2388879ed8e0eab9d87c62`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f03a1cb6bf3c0c31f517f29389b88a2b5a555cc93f35eba1ccf00b18b1a2a39`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b04a18e14e31a1d49b3cac8dfaf6b7d717dfa36fe35d5fcf7d1accaca3248ae`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae7281af404d8eaf85213c3a817ea7db60051235cde543ce1f65924bb6c8b8`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9969a43f65e07447e477f29720250cf1bd54b73dddafae587b6acce5c4a22207`  
		Last Modified: Thu, 08 Jan 2026 19:12:29 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:81415cb6dab950da391d97520baea34b19b7d5894aa3c18bf6a602723945c398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffcf74cf8fac1f1e2735bc855ed595b7335dc4fb0667c093b321c3bf242bdb6`

```dockerfile
```

-	Layers:
	-	`sha256:f916b3bdc7a6c111db342eae98e7fc3fb1f03012f268513e05f4312eb86a1cea`  
		Last Modified: Thu, 08 Jan 2026 22:50:34 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1bdb625e2b7625aae68a7093f6c5a22fb3abdd4cbbe2ffab2819514b03b07cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (213971526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4dbaab6925010ab43df2b877fb70beb08a9defe9c0fd1e71bdcb55d60d07a3c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:30 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:30 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:30 GMT
ARG VERSION=25.8.14.17
# Thu, 08 Jan 2026 19:10:30 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:03 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fbf56b5e5593a01971f7c17ff8d743c8577deb81ab12d416edca4c9c6cf2ac`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 7.6 MB (7576596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331bdb762605baadef2d702522de91c89a859a158286d13c4aab0dda1542e6fd`  
		Last Modified: Thu, 08 Jan 2026 22:51:13 GMT  
		Size: 178.1 MB (178141035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d774e60bfbaa0b028227462a12a7b263f1462233106198c85eb599b87e25dd60`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606cfcc1893a349268ead021f90b41f553796a74757767da59683505c50ed501`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf9ccc7753b8ac278064b500dcf25e13e4305249738b51dab5e34732945867e`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388fb0b08866fbcdd5bfd6a55223b334154440242293685ad705c4a9f0561198`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38dc6f8e9006520baa57988abc56e5bc7a2c5c35a272f2eff9a8d17955e125f2`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ef4b18aca60a2064aca2f478f4dba651118088c03a7936aff4d114992e817a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdea35a1e209a0cf0669d41be387874ed3bccc4b1e1ca561d7f5af575e73389`

```dockerfile
```

-	Layers:
	-	`sha256:d4c06f6a03cd72817b031e166b8139a77b287cb8f471987e1b4f50b35e152eb5`  
		Last Modified: Thu, 08 Jan 2026 22:50:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:a69ebd347d0d510f27cc014e12d81700695cf1ac9702c4d83f2271857d63cc06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0dea61ef4d2853bb7f4c3d8cca9fd016c27056b1c46a5eee9dae6d2faf464ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229071355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3056c0f79d082117b6f9f67fdade0abeb17b75970237686a9783ce88bc38aa11`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:27 GMT
ARG VERSION=25.8.14.17
# Thu, 08 Jan 2026 19:10:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:54 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3abfc4054c194a9cefd39672b876926786daed6977f9d2ddf3ea9b01b910c9`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7598404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c0f2cd97f6479d1c26b36ef1106078cd4c1dc763123be19b8dd808c4761af8`  
		Last Modified: Thu, 08 Jan 2026 19:12:17 GMT  
		Size: 191.1 MB (191066131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b81cdfd3a9f3262abbed81e1b5455ed5841e5364a2388879ed8e0eab9d87c62`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f03a1cb6bf3c0c31f517f29389b88a2b5a555cc93f35eba1ccf00b18b1a2a39`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b04a18e14e31a1d49b3cac8dfaf6b7d717dfa36fe35d5fcf7d1accaca3248ae`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae7281af404d8eaf85213c3a817ea7db60051235cde543ce1f65924bb6c8b8`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9969a43f65e07447e477f29720250cf1bd54b73dddafae587b6acce5c4a22207`  
		Last Modified: Thu, 08 Jan 2026 19:12:29 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:81415cb6dab950da391d97520baea34b19b7d5894aa3c18bf6a602723945c398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffcf74cf8fac1f1e2735bc855ed595b7335dc4fb0667c093b321c3bf242bdb6`

```dockerfile
```

-	Layers:
	-	`sha256:f916b3bdc7a6c111db342eae98e7fc3fb1f03012f268513e05f4312eb86a1cea`  
		Last Modified: Thu, 08 Jan 2026 22:50:34 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1bdb625e2b7625aae68a7093f6c5a22fb3abdd4cbbe2ffab2819514b03b07cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (213971526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4dbaab6925010ab43df2b877fb70beb08a9defe9c0fd1e71bdcb55d60d07a3c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:30 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:30 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:30 GMT
ARG VERSION=25.8.14.17
# Thu, 08 Jan 2026 19:10:30 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:03 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fbf56b5e5593a01971f7c17ff8d743c8577deb81ab12d416edca4c9c6cf2ac`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 7.6 MB (7576596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331bdb762605baadef2d702522de91c89a859a158286d13c4aab0dda1542e6fd`  
		Last Modified: Thu, 08 Jan 2026 22:51:13 GMT  
		Size: 178.1 MB (178141035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d774e60bfbaa0b028227462a12a7b263f1462233106198c85eb599b87e25dd60`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606cfcc1893a349268ead021f90b41f553796a74757767da59683505c50ed501`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf9ccc7753b8ac278064b500dcf25e13e4305249738b51dab5e34732945867e`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388fb0b08866fbcdd5bfd6a55223b334154440242293685ad705c4a9f0561198`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38dc6f8e9006520baa57988abc56e5bc7a2c5c35a272f2eff9a8d17955e125f2`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ef4b18aca60a2064aca2f478f4dba651118088c03a7936aff4d114992e817a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdea35a1e209a0cf0669d41be387874ed3bccc4b1e1ca561d7f5af575e73389`

```dockerfile
```

-	Layers:
	-	`sha256:d4c06f6a03cd72817b031e166b8139a77b287cb8f471987e1b4f50b35e152eb5`  
		Last Modified: Thu, 08 Jan 2026 22:50:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.14`

```console
$ docker pull clickhouse@sha256:a69ebd347d0d510f27cc014e12d81700695cf1ac9702c4d83f2271857d63cc06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.14` - linux; amd64

```console
$ docker pull clickhouse@sha256:0dea61ef4d2853bb7f4c3d8cca9fd016c27056b1c46a5eee9dae6d2faf464ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229071355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3056c0f79d082117b6f9f67fdade0abeb17b75970237686a9783ce88bc38aa11`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:27 GMT
ARG VERSION=25.8.14.17
# Thu, 08 Jan 2026 19:10:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:54 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3abfc4054c194a9cefd39672b876926786daed6977f9d2ddf3ea9b01b910c9`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7598404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c0f2cd97f6479d1c26b36ef1106078cd4c1dc763123be19b8dd808c4761af8`  
		Last Modified: Thu, 08 Jan 2026 19:12:17 GMT  
		Size: 191.1 MB (191066131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b81cdfd3a9f3262abbed81e1b5455ed5841e5364a2388879ed8e0eab9d87c62`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f03a1cb6bf3c0c31f517f29389b88a2b5a555cc93f35eba1ccf00b18b1a2a39`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b04a18e14e31a1d49b3cac8dfaf6b7d717dfa36fe35d5fcf7d1accaca3248ae`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae7281af404d8eaf85213c3a817ea7db60051235cde543ce1f65924bb6c8b8`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9969a43f65e07447e477f29720250cf1bd54b73dddafae587b6acce5c4a22207`  
		Last Modified: Thu, 08 Jan 2026 19:12:29 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:81415cb6dab950da391d97520baea34b19b7d5894aa3c18bf6a602723945c398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffcf74cf8fac1f1e2735bc855ed595b7335dc4fb0667c093b321c3bf242bdb6`

```dockerfile
```

-	Layers:
	-	`sha256:f916b3bdc7a6c111db342eae98e7fc3fb1f03012f268513e05f4312eb86a1cea`  
		Last Modified: Thu, 08 Jan 2026 22:50:34 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.14` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1bdb625e2b7625aae68a7093f6c5a22fb3abdd4cbbe2ffab2819514b03b07cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (213971526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4dbaab6925010ab43df2b877fb70beb08a9defe9c0fd1e71bdcb55d60d07a3c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:30 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:30 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:30 GMT
ARG VERSION=25.8.14.17
# Thu, 08 Jan 2026 19:10:30 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:03 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fbf56b5e5593a01971f7c17ff8d743c8577deb81ab12d416edca4c9c6cf2ac`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 7.6 MB (7576596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331bdb762605baadef2d702522de91c89a859a158286d13c4aab0dda1542e6fd`  
		Last Modified: Thu, 08 Jan 2026 22:51:13 GMT  
		Size: 178.1 MB (178141035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d774e60bfbaa0b028227462a12a7b263f1462233106198c85eb599b87e25dd60`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606cfcc1893a349268ead021f90b41f553796a74757767da59683505c50ed501`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf9ccc7753b8ac278064b500dcf25e13e4305249738b51dab5e34732945867e`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388fb0b08866fbcdd5bfd6a55223b334154440242293685ad705c4a9f0561198`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38dc6f8e9006520baa57988abc56e5bc7a2c5c35a272f2eff9a8d17955e125f2`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ef4b18aca60a2064aca2f478f4dba651118088c03a7936aff4d114992e817a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdea35a1e209a0cf0669d41be387874ed3bccc4b1e1ca561d7f5af575e73389`

```dockerfile
```

-	Layers:
	-	`sha256:d4c06f6a03cd72817b031e166b8139a77b287cb8f471987e1b4f50b35e152eb5`  
		Last Modified: Thu, 08 Jan 2026 22:50:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.14-jammy`

```console
$ docker pull clickhouse@sha256:a69ebd347d0d510f27cc014e12d81700695cf1ac9702c4d83f2271857d63cc06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.14-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0dea61ef4d2853bb7f4c3d8cca9fd016c27056b1c46a5eee9dae6d2faf464ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229071355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3056c0f79d082117b6f9f67fdade0abeb17b75970237686a9783ce88bc38aa11`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:27 GMT
ARG VERSION=25.8.14.17
# Thu, 08 Jan 2026 19:10:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:54 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3abfc4054c194a9cefd39672b876926786daed6977f9d2ddf3ea9b01b910c9`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7598404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c0f2cd97f6479d1c26b36ef1106078cd4c1dc763123be19b8dd808c4761af8`  
		Last Modified: Thu, 08 Jan 2026 19:12:17 GMT  
		Size: 191.1 MB (191066131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b81cdfd3a9f3262abbed81e1b5455ed5841e5364a2388879ed8e0eab9d87c62`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f03a1cb6bf3c0c31f517f29389b88a2b5a555cc93f35eba1ccf00b18b1a2a39`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b04a18e14e31a1d49b3cac8dfaf6b7d717dfa36fe35d5fcf7d1accaca3248ae`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae7281af404d8eaf85213c3a817ea7db60051235cde543ce1f65924bb6c8b8`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9969a43f65e07447e477f29720250cf1bd54b73dddafae587b6acce5c4a22207`  
		Last Modified: Thu, 08 Jan 2026 19:12:29 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:81415cb6dab950da391d97520baea34b19b7d5894aa3c18bf6a602723945c398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffcf74cf8fac1f1e2735bc855ed595b7335dc4fb0667c093b321c3bf242bdb6`

```dockerfile
```

-	Layers:
	-	`sha256:f916b3bdc7a6c111db342eae98e7fc3fb1f03012f268513e05f4312eb86a1cea`  
		Last Modified: Thu, 08 Jan 2026 22:50:34 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.14-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1bdb625e2b7625aae68a7093f6c5a22fb3abdd4cbbe2ffab2819514b03b07cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (213971526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4dbaab6925010ab43df2b877fb70beb08a9defe9c0fd1e71bdcb55d60d07a3c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:30 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:30 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:30 GMT
ARG VERSION=25.8.14.17
# Thu, 08 Jan 2026 19:10:30 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:03 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fbf56b5e5593a01971f7c17ff8d743c8577deb81ab12d416edca4c9c6cf2ac`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 7.6 MB (7576596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331bdb762605baadef2d702522de91c89a859a158286d13c4aab0dda1542e6fd`  
		Last Modified: Thu, 08 Jan 2026 22:51:13 GMT  
		Size: 178.1 MB (178141035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d774e60bfbaa0b028227462a12a7b263f1462233106198c85eb599b87e25dd60`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606cfcc1893a349268ead021f90b41f553796a74757767da59683505c50ed501`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf9ccc7753b8ac278064b500dcf25e13e4305249738b51dab5e34732945867e`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388fb0b08866fbcdd5bfd6a55223b334154440242293685ad705c4a9f0561198`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38dc6f8e9006520baa57988abc56e5bc7a2c5c35a272f2eff9a8d17955e125f2`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ef4b18aca60a2064aca2f478f4dba651118088c03a7936aff4d114992e817a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdea35a1e209a0cf0669d41be387874ed3bccc4b1e1ca561d7f5af575e73389`

```dockerfile
```

-	Layers:
	-	`sha256:d4c06f6a03cd72817b031e166b8139a77b287cb8f471987e1b4f50b35e152eb5`  
		Last Modified: Thu, 08 Jan 2026 22:50:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.14.17`

```console
$ docker pull clickhouse@sha256:a69ebd347d0d510f27cc014e12d81700695cf1ac9702c4d83f2271857d63cc06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.14.17` - linux; amd64

```console
$ docker pull clickhouse@sha256:0dea61ef4d2853bb7f4c3d8cca9fd016c27056b1c46a5eee9dae6d2faf464ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229071355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3056c0f79d082117b6f9f67fdade0abeb17b75970237686a9783ce88bc38aa11`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:27 GMT
ARG VERSION=25.8.14.17
# Thu, 08 Jan 2026 19:10:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:54 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3abfc4054c194a9cefd39672b876926786daed6977f9d2ddf3ea9b01b910c9`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7598404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c0f2cd97f6479d1c26b36ef1106078cd4c1dc763123be19b8dd808c4761af8`  
		Last Modified: Thu, 08 Jan 2026 19:12:17 GMT  
		Size: 191.1 MB (191066131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b81cdfd3a9f3262abbed81e1b5455ed5841e5364a2388879ed8e0eab9d87c62`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f03a1cb6bf3c0c31f517f29389b88a2b5a555cc93f35eba1ccf00b18b1a2a39`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b04a18e14e31a1d49b3cac8dfaf6b7d717dfa36fe35d5fcf7d1accaca3248ae`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae7281af404d8eaf85213c3a817ea7db60051235cde543ce1f65924bb6c8b8`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9969a43f65e07447e477f29720250cf1bd54b73dddafae587b6acce5c4a22207`  
		Last Modified: Thu, 08 Jan 2026 19:12:29 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.14.17` - unknown; unknown

```console
$ docker pull clickhouse@sha256:81415cb6dab950da391d97520baea34b19b7d5894aa3c18bf6a602723945c398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffcf74cf8fac1f1e2735bc855ed595b7335dc4fb0667c093b321c3bf242bdb6`

```dockerfile
```

-	Layers:
	-	`sha256:f916b3bdc7a6c111db342eae98e7fc3fb1f03012f268513e05f4312eb86a1cea`  
		Last Modified: Thu, 08 Jan 2026 22:50:34 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.14.17` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1bdb625e2b7625aae68a7093f6c5a22fb3abdd4cbbe2ffab2819514b03b07cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (213971526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4dbaab6925010ab43df2b877fb70beb08a9defe9c0fd1e71bdcb55d60d07a3c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:30 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:30 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:30 GMT
ARG VERSION=25.8.14.17
# Thu, 08 Jan 2026 19:10:30 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:03 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fbf56b5e5593a01971f7c17ff8d743c8577deb81ab12d416edca4c9c6cf2ac`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 7.6 MB (7576596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331bdb762605baadef2d702522de91c89a859a158286d13c4aab0dda1542e6fd`  
		Last Modified: Thu, 08 Jan 2026 22:51:13 GMT  
		Size: 178.1 MB (178141035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d774e60bfbaa0b028227462a12a7b263f1462233106198c85eb599b87e25dd60`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606cfcc1893a349268ead021f90b41f553796a74757767da59683505c50ed501`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf9ccc7753b8ac278064b500dcf25e13e4305249738b51dab5e34732945867e`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388fb0b08866fbcdd5bfd6a55223b334154440242293685ad705c4a9f0561198`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38dc6f8e9006520baa57988abc56e5bc7a2c5c35a272f2eff9a8d17955e125f2`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.14.17` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ef4b18aca60a2064aca2f478f4dba651118088c03a7936aff4d114992e817a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdea35a1e209a0cf0669d41be387874ed3bccc4b1e1ca561d7f5af575e73389`

```dockerfile
```

-	Layers:
	-	`sha256:d4c06f6a03cd72817b031e166b8139a77b287cb8f471987e1b4f50b35e152eb5`  
		Last Modified: Thu, 08 Jan 2026 22:50:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.14.17-jammy`

```console
$ docker pull clickhouse@sha256:a69ebd347d0d510f27cc014e12d81700695cf1ac9702c4d83f2271857d63cc06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.14.17-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0dea61ef4d2853bb7f4c3d8cca9fd016c27056b1c46a5eee9dae6d2faf464ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229071355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3056c0f79d082117b6f9f67fdade0abeb17b75970237686a9783ce88bc38aa11`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:27 GMT
ARG VERSION=25.8.14.17
# Thu, 08 Jan 2026 19:10:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:54 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3abfc4054c194a9cefd39672b876926786daed6977f9d2ddf3ea9b01b910c9`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7598404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c0f2cd97f6479d1c26b36ef1106078cd4c1dc763123be19b8dd808c4761af8`  
		Last Modified: Thu, 08 Jan 2026 19:12:17 GMT  
		Size: 191.1 MB (191066131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b81cdfd3a9f3262abbed81e1b5455ed5841e5364a2388879ed8e0eab9d87c62`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f03a1cb6bf3c0c31f517f29389b88a2b5a555cc93f35eba1ccf00b18b1a2a39`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b04a18e14e31a1d49b3cac8dfaf6b7d717dfa36fe35d5fcf7d1accaca3248ae`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae7281af404d8eaf85213c3a817ea7db60051235cde543ce1f65924bb6c8b8`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9969a43f65e07447e477f29720250cf1bd54b73dddafae587b6acce5c4a22207`  
		Last Modified: Thu, 08 Jan 2026 19:12:29 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.14.17-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:81415cb6dab950da391d97520baea34b19b7d5894aa3c18bf6a602723945c398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffcf74cf8fac1f1e2735bc855ed595b7335dc4fb0667c093b321c3bf242bdb6`

```dockerfile
```

-	Layers:
	-	`sha256:f916b3bdc7a6c111db342eae98e7fc3fb1f03012f268513e05f4312eb86a1cea`  
		Last Modified: Thu, 08 Jan 2026 22:50:34 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.14.17-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1bdb625e2b7625aae68a7093f6c5a22fb3abdd4cbbe2ffab2819514b03b07cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (213971526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4dbaab6925010ab43df2b877fb70beb08a9defe9c0fd1e71bdcb55d60d07a3c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:30 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:30 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:30 GMT
ARG VERSION=25.8.14.17
# Thu, 08 Jan 2026 19:10:30 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:03 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fbf56b5e5593a01971f7c17ff8d743c8577deb81ab12d416edca4c9c6cf2ac`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 7.6 MB (7576596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331bdb762605baadef2d702522de91c89a859a158286d13c4aab0dda1542e6fd`  
		Last Modified: Thu, 08 Jan 2026 22:51:13 GMT  
		Size: 178.1 MB (178141035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d774e60bfbaa0b028227462a12a7b263f1462233106198c85eb599b87e25dd60`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606cfcc1893a349268ead021f90b41f553796a74757767da59683505c50ed501`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf9ccc7753b8ac278064b500dcf25e13e4305249738b51dab5e34732945867e`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388fb0b08866fbcdd5bfd6a55223b334154440242293685ad705c4a9f0561198`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38dc6f8e9006520baa57988abc56e5bc7a2c5c35a272f2eff9a8d17955e125f2`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.14.17-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ef4b18aca60a2064aca2f478f4dba651118088c03a7936aff4d114992e817a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdea35a1e209a0cf0669d41be387874ed3bccc4b1e1ca561d7f5af575e73389`

```dockerfile
```

-	Layers:
	-	`sha256:d4c06f6a03cd72817b031e166b8139a77b287cb8f471987e1b4f50b35e152eb5`  
		Last Modified: Thu, 08 Jan 2026 22:50:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:1f72b42e0277e70befc6720dfb81d05e531098ae38a1d80d725822bc52177f19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:5953fee9e7204deb6f57bbe95d98eff05b8c2df4daf7f8d1d8b8ef33d6528ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246459240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636fde9e3ac86031d6a1794d93486f1bf1fbf2230c17118dcb2d8e6ddd053603`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:27 GMT
ARG VERSION=25.12.2.54
# Thu, 08 Jan 2026 19:10:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:10:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:10:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:10:55 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:10:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:10:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:10:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:10:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3abfc4054c194a9cefd39672b876926786daed6977f9d2ddf3ea9b01b910c9`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7598404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4189e8d3cf58cc07948ac61090fd9dfd06da555f31bb8b322e8bfe55347f4a07`  
		Last Modified: Thu, 08 Jan 2026 23:03:42 GMT  
		Size: 208.5 MB (208453993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cf40e289eb4959252ffeb1cb4f64fcaa5face990d33c2b2d477cde08f7ade0`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb906d86fdcfa4424f5d4aeefb7472e97a615ed92eea646ce31ca5e370fa177`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbce7a23330521b82b0a971f543d66e041c3472ce7e30c121a46ee0fa40aba7`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6aa7eb7e363161bae220c5567d1871e3c1c2e3fa6885df01d2882387d2cb45`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf9cf136a2beff175113910bebef5b091fc483c264c0ae3a3fa3764fedd3729`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a3e602c43c1d9d713b904900b0a8e349817a6dbb4c515a8314351a88e7396154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9531cd0eaa9793dba37b157482f5ddc91e934f158bf681c15c5b32d56f716011`

```dockerfile
```

-	Layers:
	-	`sha256:9e9be73a5e40575f6888ce51736c3d9eb361e4536666baa2be83c49d4da978a1`  
		Last Modified: Thu, 08 Jan 2026 22:49:57 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d22c2066bc823cc910b240e095539b5d7bfcf044877ae48936b0a743dee57f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228337624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b98dff4813c02c2ca9c601e5b203b505c2b25c4319886374e5e6320cd157ec9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:30 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:30 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:30 GMT
ARG VERSION=25.12.2.54
# Thu, 08 Jan 2026 19:10:30 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:10:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:10:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:10:59 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:10:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:10:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:10:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:10:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fbf56b5e5593a01971f7c17ff8d743c8577deb81ab12d416edca4c9c6cf2ac`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 7.6 MB (7576596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32371df79fab30e208eac2b1c9871e4195e7c47bf998975649bbb3c719ebebcd`  
		Last Modified: Thu, 08 Jan 2026 19:12:00 GMT  
		Size: 192.5 MB (192507107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567586fd3e2cc17abf4f94350ea19c433f7dc0e7c8276c5f2d60a418df33d86e`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8413fdeae9cadb3fcb66db640fefb6968c58e31e69a8b2dec117de4498d32f`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b87f902825889df29cf646d68088c890c427f535e40eb9940cff4e1d8f8f31`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913dc5a5a01d10c560bc137b67cd99c69e80f16172577b4f1add4f8b619320c`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c1f4e3c0cad0c8550f8db416a508c05ed7897e9ca309c54dd91593711f45c4`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a37f54b2f2cf98654a1902f1a7d7a7b1286720dc36ec34d842d14a114d7ff9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765fcaf50f0b876c1377173e649ed2a4b0afab5000c3579adddc3da93e7b319c`

```dockerfile
```

-	Layers:
	-	`sha256:c24485efdb6114adcfa8b08132bb411ae76e7c7d63fb8e9b9ec1f6bf2b151236`  
		Last Modified: Thu, 08 Jan 2026 22:50:00 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:1f72b42e0277e70befc6720dfb81d05e531098ae38a1d80d725822bc52177f19
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:5953fee9e7204deb6f57bbe95d98eff05b8c2df4daf7f8d1d8b8ef33d6528ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.5 MB (246459240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636fde9e3ac86031d6a1794d93486f1bf1fbf2230c17118dcb2d8e6ddd053603`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:27 GMT
ARG VERSION=25.12.2.54
# Thu, 08 Jan 2026 19:10:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:10:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:10:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:10:55 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:10:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:10:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:10:55 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:10:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:10:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3abfc4054c194a9cefd39672b876926786daed6977f9d2ddf3ea9b01b910c9`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7598404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4189e8d3cf58cc07948ac61090fd9dfd06da555f31bb8b322e8bfe55347f4a07`  
		Last Modified: Thu, 08 Jan 2026 23:03:42 GMT  
		Size: 208.5 MB (208453993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cf40e289eb4959252ffeb1cb4f64fcaa5face990d33c2b2d477cde08f7ade0`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb906d86fdcfa4424f5d4aeefb7472e97a615ed92eea646ce31ca5e370fa177`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cbce7a23330521b82b0a971f543d66e041c3472ce7e30c121a46ee0fa40aba7`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c6aa7eb7e363161bae220c5567d1871e3c1c2e3fa6885df01d2882387d2cb45`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf9cf136a2beff175113910bebef5b091fc483c264c0ae3a3fa3764fedd3729`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a3e602c43c1d9d713b904900b0a8e349817a6dbb4c515a8314351a88e7396154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9531cd0eaa9793dba37b157482f5ddc91e934f158bf681c15c5b32d56f716011`

```dockerfile
```

-	Layers:
	-	`sha256:9e9be73a5e40575f6888ce51736c3d9eb361e4536666baa2be83c49d4da978a1`  
		Last Modified: Thu, 08 Jan 2026 22:49:57 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d22c2066bc823cc910b240e095539b5d7bfcf044877ae48936b0a743dee57f58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228337624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b98dff4813c02c2ca9c601e5b203b505c2b25c4319886374e5e6320cd157ec9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:30 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:30 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:30 GMT
ARG VERSION=25.12.2.54
# Thu, 08 Jan 2026 19:10:30 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:10:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:10:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:10:59 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:10:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.2.54 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:10:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:10:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:10:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:10:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fbf56b5e5593a01971f7c17ff8d743c8577deb81ab12d416edca4c9c6cf2ac`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 7.6 MB (7576596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32371df79fab30e208eac2b1c9871e4195e7c47bf998975649bbb3c719ebebcd`  
		Last Modified: Thu, 08 Jan 2026 19:12:00 GMT  
		Size: 192.5 MB (192507107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567586fd3e2cc17abf4f94350ea19c433f7dc0e7c8276c5f2d60a418df33d86e`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8413fdeae9cadb3fcb66db640fefb6968c58e31e69a8b2dec117de4498d32f`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b87f902825889df29cf646d68088c890c427f535e40eb9940cff4e1d8f8f31`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6913dc5a5a01d10c560bc137b67cd99c69e80f16172577b4f1add4f8b619320c`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c1f4e3c0cad0c8550f8db416a508c05ed7897e9ca309c54dd91593711f45c4`  
		Last Modified: Thu, 08 Jan 2026 19:11:37 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a37f54b2f2cf98654a1902f1a7d7a7b1286720dc36ec34d842d14a114d7ff9d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:765fcaf50f0b876c1377173e649ed2a4b0afab5000c3579adddc3da93e7b319c`

```dockerfile
```

-	Layers:
	-	`sha256:c24485efdb6114adcfa8b08132bb411ae76e7c7d63fb8e9b9ec1f6bf2b151236`  
		Last Modified: Thu, 08 Jan 2026 22:50:00 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:a69ebd347d0d510f27cc014e12d81700695cf1ac9702c4d83f2271857d63cc06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:0dea61ef4d2853bb7f4c3d8cca9fd016c27056b1c46a5eee9dae6d2faf464ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229071355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3056c0f79d082117b6f9f67fdade0abeb17b75970237686a9783ce88bc38aa11`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:27 GMT
ARG VERSION=25.8.14.17
# Thu, 08 Jan 2026 19:10:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:54 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3abfc4054c194a9cefd39672b876926786daed6977f9d2ddf3ea9b01b910c9`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7598404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c0f2cd97f6479d1c26b36ef1106078cd4c1dc763123be19b8dd808c4761af8`  
		Last Modified: Thu, 08 Jan 2026 19:12:17 GMT  
		Size: 191.1 MB (191066131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b81cdfd3a9f3262abbed81e1b5455ed5841e5364a2388879ed8e0eab9d87c62`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f03a1cb6bf3c0c31f517f29389b88a2b5a555cc93f35eba1ccf00b18b1a2a39`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b04a18e14e31a1d49b3cac8dfaf6b7d717dfa36fe35d5fcf7d1accaca3248ae`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae7281af404d8eaf85213c3a817ea7db60051235cde543ce1f65924bb6c8b8`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9969a43f65e07447e477f29720250cf1bd54b73dddafae587b6acce5c4a22207`  
		Last Modified: Thu, 08 Jan 2026 19:12:29 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:81415cb6dab950da391d97520baea34b19b7d5894aa3c18bf6a602723945c398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffcf74cf8fac1f1e2735bc855ed595b7335dc4fb0667c093b321c3bf242bdb6`

```dockerfile
```

-	Layers:
	-	`sha256:f916b3bdc7a6c111db342eae98e7fc3fb1f03012f268513e05f4312eb86a1cea`  
		Last Modified: Thu, 08 Jan 2026 22:50:34 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1bdb625e2b7625aae68a7093f6c5a22fb3abdd4cbbe2ffab2819514b03b07cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (213971526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4dbaab6925010ab43df2b877fb70beb08a9defe9c0fd1e71bdcb55d60d07a3c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:30 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:30 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:30 GMT
ARG VERSION=25.8.14.17
# Thu, 08 Jan 2026 19:10:30 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:03 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fbf56b5e5593a01971f7c17ff8d743c8577deb81ab12d416edca4c9c6cf2ac`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 7.6 MB (7576596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331bdb762605baadef2d702522de91c89a859a158286d13c4aab0dda1542e6fd`  
		Last Modified: Thu, 08 Jan 2026 22:51:13 GMT  
		Size: 178.1 MB (178141035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d774e60bfbaa0b028227462a12a7b263f1462233106198c85eb599b87e25dd60`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606cfcc1893a349268ead021f90b41f553796a74757767da59683505c50ed501`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf9ccc7753b8ac278064b500dcf25e13e4305249738b51dab5e34732945867e`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388fb0b08866fbcdd5bfd6a55223b334154440242293685ad705c4a9f0561198`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38dc6f8e9006520baa57988abc56e5bc7a2c5c35a272f2eff9a8d17955e125f2`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ef4b18aca60a2064aca2f478f4dba651118088c03a7936aff4d114992e817a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdea35a1e209a0cf0669d41be387874ed3bccc4b1e1ca561d7f5af575e73389`

```dockerfile
```

-	Layers:
	-	`sha256:d4c06f6a03cd72817b031e166b8139a77b287cb8f471987e1b4f50b35e152eb5`  
		Last Modified: Thu, 08 Jan 2026 22:50:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:a69ebd347d0d510f27cc014e12d81700695cf1ac9702c4d83f2271857d63cc06
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0dea61ef4d2853bb7f4c3d8cca9fd016c27056b1c46a5eee9dae6d2faf464ccc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229071355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3056c0f79d082117b6f9f67fdade0abeb17b75970237686a9783ce88bc38aa11`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:27 GMT
ARG VERSION=25.8.14.17
# Thu, 08 Jan 2026 19:10:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:11:54 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:11:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:11:54 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:11:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:11:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b3abfc4054c194a9cefd39672b876926786daed6977f9d2ddf3ea9b01b910c9`  
		Last Modified: Thu, 08 Jan 2026 19:11:39 GMT  
		Size: 7.6 MB (7598404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c0f2cd97f6479d1c26b36ef1106078cd4c1dc763123be19b8dd808c4761af8`  
		Last Modified: Thu, 08 Jan 2026 19:12:17 GMT  
		Size: 191.1 MB (191066131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b81cdfd3a9f3262abbed81e1b5455ed5841e5364a2388879ed8e0eab9d87c62`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f03a1cb6bf3c0c31f517f29389b88a2b5a555cc93f35eba1ccf00b18b1a2a39`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b04a18e14e31a1d49b3cac8dfaf6b7d717dfa36fe35d5fcf7d1accaca3248ae`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ae7281af404d8eaf85213c3a817ea7db60051235cde543ce1f65924bb6c8b8`  
		Last Modified: Thu, 08 Jan 2026 19:12:28 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9969a43f65e07447e477f29720250cf1bd54b73dddafae587b6acce5c4a22207`  
		Last Modified: Thu, 08 Jan 2026 19:12:29 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:81415cb6dab950da391d97520baea34b19b7d5894aa3c18bf6a602723945c398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffcf74cf8fac1f1e2735bc855ed595b7335dc4fb0667c093b321c3bf242bdb6`

```dockerfile
```

-	Layers:
	-	`sha256:f916b3bdc7a6c111db342eae98e7fc3fb1f03012f268513e05f4312eb86a1cea`  
		Last Modified: Thu, 08 Jan 2026 22:50:34 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1bdb625e2b7625aae68a7093f6c5a22fb3abdd4cbbe2ffab2819514b03b07cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.0 MB (213971526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4dbaab6925010ab43df2b877fb70beb08a9defe9c0fd1e71bdcb55d60d07a3c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 08 Jan 2026 19:10:30 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 08 Jan 2026 19:10:30 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 08 Jan 2026 19:10:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPO_CHANNEL=stable
# Thu, 08 Jan 2026 19:10:30 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 08 Jan 2026 19:10:30 GMT
ARG VERSION=25.8.14.17
# Thu, 08 Jan 2026 19:10:30 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 08 Jan 2026 19:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 08 Jan 2026 19:12:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 08 Jan 2026 19:12:03 GMT
ENV TZ=UTC
# Thu, 08 Jan 2026 19:12:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.14.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 08 Jan 2026 19:12:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 08 Jan 2026 19:12:04 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 08 Jan 2026 19:12:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 08 Jan 2026 19:12:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Fri, 12 Dec 2025 23:53:40 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fbf56b5e5593a01971f7c17ff8d743c8577deb81ab12d416edca4c9c6cf2ac`  
		Last Modified: Thu, 08 Jan 2026 19:11:38 GMT  
		Size: 7.6 MB (7576596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331bdb762605baadef2d702522de91c89a859a158286d13c4aab0dda1542e6fd`  
		Last Modified: Thu, 08 Jan 2026 22:51:13 GMT  
		Size: 178.1 MB (178141035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d774e60bfbaa0b028227462a12a7b263f1462233106198c85eb599b87e25dd60`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606cfcc1893a349268ead021f90b41f553796a74757767da59683505c50ed501`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf9ccc7753b8ac278064b500dcf25e13e4305249738b51dab5e34732945867e`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388fb0b08866fbcdd5bfd6a55223b334154440242293685ad705c4a9f0561198`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38dc6f8e9006520baa57988abc56e5bc7a2c5c35a272f2eff9a8d17955e125f2`  
		Last Modified: Thu, 08 Jan 2026 19:12:31 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ef4b18aca60a2064aca2f478f4dba651118088c03a7936aff4d114992e817a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdea35a1e209a0cf0669d41be387874ed3bccc4b1e1ca561d7f5af575e73389`

```dockerfile
```

-	Layers:
	-	`sha256:d4c06f6a03cd72817b031e166b8139a77b287cb8f471987e1b4f50b35e152eb5`  
		Last Modified: Thu, 08 Jan 2026 22:50:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json
