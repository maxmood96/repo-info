<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.20`](#clickhouse25820)
-	[`clickhouse:25.8.20-jammy`](#clickhouse25820-jammy)
-	[`clickhouse:25.8.20.4`](#clickhouse258204)
-	[`clickhouse:25.8.20.4-jammy`](#clickhouse258204-jammy)
-	[`clickhouse:26.1`](#clickhouse261)
-	[`clickhouse:26.1-jammy`](#clickhouse261-jammy)
-	[`clickhouse:26.1.6`](#clickhouse2616)
-	[`clickhouse:26.1.6-jammy`](#clickhouse2616-jammy)
-	[`clickhouse:26.1.6.6`](#clickhouse26166)
-	[`clickhouse:26.1.6.6-jammy`](#clickhouse26166-jammy)
-	[`clickhouse:26.2`](#clickhouse262)
-	[`clickhouse:26.2-jammy`](#clickhouse262-jammy)
-	[`clickhouse:26.2.5`](#clickhouse2625)
-	[`clickhouse:26.2.5-jammy`](#clickhouse2625-jammy)
-	[`clickhouse:26.2.5.45`](#clickhouse262545)
-	[`clickhouse:26.2.5.45-jammy`](#clickhouse262545-jammy)
-	[`clickhouse:26.3`](#clickhouse263)
-	[`clickhouse:26.3-jammy`](#clickhouse263-jammy)
-	[`clickhouse:26.3.1`](#clickhouse2631)
-	[`clickhouse:26.3.1-jammy`](#clickhouse2631-jammy)
-	[`clickhouse:26.3.1.896`](#clickhouse2631896)
-	[`clickhouse:26.3.1.896-jammy`](#clickhouse2631896-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:4ef1ad45bc187c91b1cfdfd977871c7ae4940036ebe8b666d42ccf70db004688
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:55ef1f211514a17a353171fea8c1ade888e379082583e9a783edc79c233ff5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228999206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884d6cad0df35122ece62d68e0d1da0ef84f633195cc510259850cd2f2722f06`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:06 GMT
ARG VERSION=25.8.20.4
# Fri, 27 Mar 2026 17:59:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:32 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:32 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040d6d889b12905b3e5a83996354dfb14bbe228fd3f84454773546fcdfe8247a`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 7.6 MB (7598240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc15689fc695354813c65a3f5c0a081357e4f676276a137317769eb21ccd5101`  
		Last Modified: Fri, 27 Mar 2026 17:59:55 GMT  
		Size: 191.0 MB (190992416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc96acc37198205f7c0c6f6bdbb3b18f35332ec4ce2405f5338704a838ef702`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb94eeb0cdd6fa51d15337578686872b3bf461981c3ef603b93b52c8fdb21f04`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87b23a7034d076dfd8422c419010f07e49f7aa5700b3391eee7e251ffa98099`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125711fdf3aa8247377a37f5c656f90c39bd652262bddef53a04a811205e2c05`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48b498efe644e33d2dd55db901a546cc930e4c43fa6045ab5e1361a0d8bff78`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a150ab55c907ec5661807ccdd7c9785414819c0a03a80b5b6869ff7ce5865ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98131fb37815a73d4006e68c952f1bad77ef42644b7d07b853be09651d6105d`

```dockerfile
```

-	Layers:
	-	`sha256:140b30ce87684e3c6e9c5f84643fa348c06461b4942692e37568d10926fad2b9`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f29aea68588148a629783b4bd6bf162ca76d5bc4c6eda6cfc469ed410bc7a17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213912519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaab8a5b86778cb30a695f7a7eaf52c75b96092e770f2471fa07f6de1a61d220`
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
# Fri, 27 Mar 2026 17:57:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:10 GMT
ARG VERSION=25.8.20.4
# Fri, 27 Mar 2026 17:57:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:57:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:57:55 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:57:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:57:55 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:57:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:57:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9190cab5ae15f4858810f8f01aad497cbeea40e9f9a0f4dcb8b917d69e569c4f`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 7.6 MB (7577373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9dc3477400d8147f54b18126223384063edbc5a1eba29b68916b679d201de9`  
		Last Modified: Fri, 27 Mar 2026 17:58:18 GMT  
		Size: 178.1 MB (178076094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a011c32af5a8ad314e044ff16a1ab64e88d60c56ec65c097f5d0c07ac047c627`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5716cf75e4ba3878bede3c8c5efe30f690f306bbf3485234ec90e14020a65cda`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe04ec673e58aaf87ffd732ca159d4ee91240e1faaeed9c0bd422622b4cc2218`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5f827941d800c21f7f7e4dfc993457613ad23ec357d5646b3457a87e9e316f`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63719d7d0eca99170add67ae15a32d3c5557561a22075d5c3c3538a252bf88d`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:51b16ceaa78fe72a0888949b34cb1c4d34bbde4532a3a45ebd9f4035a6fc5162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617616e7b4bed8b8a32993c28cb7987987b0a91e9c39847750e2bcbd41d3ddf1`

```dockerfile
```

-	Layers:
	-	`sha256:8ea2b673759eae99be8b257f1bf7a41a8585a7100b673615446b7d9f27ab06e3`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:4ef1ad45bc187c91b1cfdfd977871c7ae4940036ebe8b666d42ccf70db004688
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:55ef1f211514a17a353171fea8c1ade888e379082583e9a783edc79c233ff5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228999206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884d6cad0df35122ece62d68e0d1da0ef84f633195cc510259850cd2f2722f06`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:06 GMT
ARG VERSION=25.8.20.4
# Fri, 27 Mar 2026 17:59:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:32 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:32 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040d6d889b12905b3e5a83996354dfb14bbe228fd3f84454773546fcdfe8247a`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 7.6 MB (7598240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc15689fc695354813c65a3f5c0a081357e4f676276a137317769eb21ccd5101`  
		Last Modified: Fri, 27 Mar 2026 17:59:55 GMT  
		Size: 191.0 MB (190992416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc96acc37198205f7c0c6f6bdbb3b18f35332ec4ce2405f5338704a838ef702`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb94eeb0cdd6fa51d15337578686872b3bf461981c3ef603b93b52c8fdb21f04`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87b23a7034d076dfd8422c419010f07e49f7aa5700b3391eee7e251ffa98099`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125711fdf3aa8247377a37f5c656f90c39bd652262bddef53a04a811205e2c05`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48b498efe644e33d2dd55db901a546cc930e4c43fa6045ab5e1361a0d8bff78`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a150ab55c907ec5661807ccdd7c9785414819c0a03a80b5b6869ff7ce5865ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98131fb37815a73d4006e68c952f1bad77ef42644b7d07b853be09651d6105d`

```dockerfile
```

-	Layers:
	-	`sha256:140b30ce87684e3c6e9c5f84643fa348c06461b4942692e37568d10926fad2b9`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f29aea68588148a629783b4bd6bf162ca76d5bc4c6eda6cfc469ed410bc7a17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213912519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaab8a5b86778cb30a695f7a7eaf52c75b96092e770f2471fa07f6de1a61d220`
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
# Fri, 27 Mar 2026 17:57:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:10 GMT
ARG VERSION=25.8.20.4
# Fri, 27 Mar 2026 17:57:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:57:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:57:55 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:57:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:57:55 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:57:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:57:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9190cab5ae15f4858810f8f01aad497cbeea40e9f9a0f4dcb8b917d69e569c4f`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 7.6 MB (7577373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9dc3477400d8147f54b18126223384063edbc5a1eba29b68916b679d201de9`  
		Last Modified: Fri, 27 Mar 2026 17:58:18 GMT  
		Size: 178.1 MB (178076094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a011c32af5a8ad314e044ff16a1ab64e88d60c56ec65c097f5d0c07ac047c627`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5716cf75e4ba3878bede3c8c5efe30f690f306bbf3485234ec90e14020a65cda`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe04ec673e58aaf87ffd732ca159d4ee91240e1faaeed9c0bd422622b4cc2218`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5f827941d800c21f7f7e4dfc993457613ad23ec357d5646b3457a87e9e316f`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63719d7d0eca99170add67ae15a32d3c5557561a22075d5c3c3538a252bf88d`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:51b16ceaa78fe72a0888949b34cb1c4d34bbde4532a3a45ebd9f4035a6fc5162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617616e7b4bed8b8a32993c28cb7987987b0a91e9c39847750e2bcbd41d3ddf1`

```dockerfile
```

-	Layers:
	-	`sha256:8ea2b673759eae99be8b257f1bf7a41a8585a7100b673615446b7d9f27ab06e3`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.20`

```console
$ docker pull clickhouse@sha256:4ef1ad45bc187c91b1cfdfd977871c7ae4940036ebe8b666d42ccf70db004688
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.20` - linux; amd64

```console
$ docker pull clickhouse@sha256:55ef1f211514a17a353171fea8c1ade888e379082583e9a783edc79c233ff5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228999206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884d6cad0df35122ece62d68e0d1da0ef84f633195cc510259850cd2f2722f06`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:06 GMT
ARG VERSION=25.8.20.4
# Fri, 27 Mar 2026 17:59:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:32 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:32 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040d6d889b12905b3e5a83996354dfb14bbe228fd3f84454773546fcdfe8247a`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 7.6 MB (7598240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc15689fc695354813c65a3f5c0a081357e4f676276a137317769eb21ccd5101`  
		Last Modified: Fri, 27 Mar 2026 17:59:55 GMT  
		Size: 191.0 MB (190992416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc96acc37198205f7c0c6f6bdbb3b18f35332ec4ce2405f5338704a838ef702`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb94eeb0cdd6fa51d15337578686872b3bf461981c3ef603b93b52c8fdb21f04`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87b23a7034d076dfd8422c419010f07e49f7aa5700b3391eee7e251ffa98099`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125711fdf3aa8247377a37f5c656f90c39bd652262bddef53a04a811205e2c05`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48b498efe644e33d2dd55db901a546cc930e4c43fa6045ab5e1361a0d8bff78`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.20` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a150ab55c907ec5661807ccdd7c9785414819c0a03a80b5b6869ff7ce5865ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98131fb37815a73d4006e68c952f1bad77ef42644b7d07b853be09651d6105d`

```dockerfile
```

-	Layers:
	-	`sha256:140b30ce87684e3c6e9c5f84643fa348c06461b4942692e37568d10926fad2b9`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.20` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f29aea68588148a629783b4bd6bf162ca76d5bc4c6eda6cfc469ed410bc7a17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213912519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaab8a5b86778cb30a695f7a7eaf52c75b96092e770f2471fa07f6de1a61d220`
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
# Fri, 27 Mar 2026 17:57:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:10 GMT
ARG VERSION=25.8.20.4
# Fri, 27 Mar 2026 17:57:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:57:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:57:55 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:57:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:57:55 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:57:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:57:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9190cab5ae15f4858810f8f01aad497cbeea40e9f9a0f4dcb8b917d69e569c4f`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 7.6 MB (7577373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9dc3477400d8147f54b18126223384063edbc5a1eba29b68916b679d201de9`  
		Last Modified: Fri, 27 Mar 2026 17:58:18 GMT  
		Size: 178.1 MB (178076094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a011c32af5a8ad314e044ff16a1ab64e88d60c56ec65c097f5d0c07ac047c627`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5716cf75e4ba3878bede3c8c5efe30f690f306bbf3485234ec90e14020a65cda`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe04ec673e58aaf87ffd732ca159d4ee91240e1faaeed9c0bd422622b4cc2218`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5f827941d800c21f7f7e4dfc993457613ad23ec357d5646b3457a87e9e316f`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63719d7d0eca99170add67ae15a32d3c5557561a22075d5c3c3538a252bf88d`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.20` - unknown; unknown

```console
$ docker pull clickhouse@sha256:51b16ceaa78fe72a0888949b34cb1c4d34bbde4532a3a45ebd9f4035a6fc5162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617616e7b4bed8b8a32993c28cb7987987b0a91e9c39847750e2bcbd41d3ddf1`

```dockerfile
```

-	Layers:
	-	`sha256:8ea2b673759eae99be8b257f1bf7a41a8585a7100b673615446b7d9f27ab06e3`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.20-jammy`

```console
$ docker pull clickhouse@sha256:4ef1ad45bc187c91b1cfdfd977871c7ae4940036ebe8b666d42ccf70db004688
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.20-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:55ef1f211514a17a353171fea8c1ade888e379082583e9a783edc79c233ff5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228999206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884d6cad0df35122ece62d68e0d1da0ef84f633195cc510259850cd2f2722f06`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:06 GMT
ARG VERSION=25.8.20.4
# Fri, 27 Mar 2026 17:59:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:32 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:32 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040d6d889b12905b3e5a83996354dfb14bbe228fd3f84454773546fcdfe8247a`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 7.6 MB (7598240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc15689fc695354813c65a3f5c0a081357e4f676276a137317769eb21ccd5101`  
		Last Modified: Fri, 27 Mar 2026 17:59:55 GMT  
		Size: 191.0 MB (190992416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc96acc37198205f7c0c6f6bdbb3b18f35332ec4ce2405f5338704a838ef702`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb94eeb0cdd6fa51d15337578686872b3bf461981c3ef603b93b52c8fdb21f04`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87b23a7034d076dfd8422c419010f07e49f7aa5700b3391eee7e251ffa98099`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125711fdf3aa8247377a37f5c656f90c39bd652262bddef53a04a811205e2c05`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48b498efe644e33d2dd55db901a546cc930e4c43fa6045ab5e1361a0d8bff78`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.20-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a150ab55c907ec5661807ccdd7c9785414819c0a03a80b5b6869ff7ce5865ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98131fb37815a73d4006e68c952f1bad77ef42644b7d07b853be09651d6105d`

```dockerfile
```

-	Layers:
	-	`sha256:140b30ce87684e3c6e9c5f84643fa348c06461b4942692e37568d10926fad2b9`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.20-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f29aea68588148a629783b4bd6bf162ca76d5bc4c6eda6cfc469ed410bc7a17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213912519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaab8a5b86778cb30a695f7a7eaf52c75b96092e770f2471fa07f6de1a61d220`
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
# Fri, 27 Mar 2026 17:57:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:10 GMT
ARG VERSION=25.8.20.4
# Fri, 27 Mar 2026 17:57:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:57:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:57:55 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:57:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:57:55 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:57:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:57:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9190cab5ae15f4858810f8f01aad497cbeea40e9f9a0f4dcb8b917d69e569c4f`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 7.6 MB (7577373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9dc3477400d8147f54b18126223384063edbc5a1eba29b68916b679d201de9`  
		Last Modified: Fri, 27 Mar 2026 17:58:18 GMT  
		Size: 178.1 MB (178076094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a011c32af5a8ad314e044ff16a1ab64e88d60c56ec65c097f5d0c07ac047c627`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5716cf75e4ba3878bede3c8c5efe30f690f306bbf3485234ec90e14020a65cda`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe04ec673e58aaf87ffd732ca159d4ee91240e1faaeed9c0bd422622b4cc2218`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5f827941d800c21f7f7e4dfc993457613ad23ec357d5646b3457a87e9e316f`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63719d7d0eca99170add67ae15a32d3c5557561a22075d5c3c3538a252bf88d`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.20-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:51b16ceaa78fe72a0888949b34cb1c4d34bbde4532a3a45ebd9f4035a6fc5162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617616e7b4bed8b8a32993c28cb7987987b0a91e9c39847750e2bcbd41d3ddf1`

```dockerfile
```

-	Layers:
	-	`sha256:8ea2b673759eae99be8b257f1bf7a41a8585a7100b673615446b7d9f27ab06e3`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.20.4`

```console
$ docker pull clickhouse@sha256:4ef1ad45bc187c91b1cfdfd977871c7ae4940036ebe8b666d42ccf70db004688
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.20.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:55ef1f211514a17a353171fea8c1ade888e379082583e9a783edc79c233ff5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228999206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884d6cad0df35122ece62d68e0d1da0ef84f633195cc510259850cd2f2722f06`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:06 GMT
ARG VERSION=25.8.20.4
# Fri, 27 Mar 2026 17:59:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:32 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:32 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040d6d889b12905b3e5a83996354dfb14bbe228fd3f84454773546fcdfe8247a`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 7.6 MB (7598240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc15689fc695354813c65a3f5c0a081357e4f676276a137317769eb21ccd5101`  
		Last Modified: Fri, 27 Mar 2026 17:59:55 GMT  
		Size: 191.0 MB (190992416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc96acc37198205f7c0c6f6bdbb3b18f35332ec4ce2405f5338704a838ef702`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb94eeb0cdd6fa51d15337578686872b3bf461981c3ef603b93b52c8fdb21f04`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87b23a7034d076dfd8422c419010f07e49f7aa5700b3391eee7e251ffa98099`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125711fdf3aa8247377a37f5c656f90c39bd652262bddef53a04a811205e2c05`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48b498efe644e33d2dd55db901a546cc930e4c43fa6045ab5e1361a0d8bff78`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.20.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a150ab55c907ec5661807ccdd7c9785414819c0a03a80b5b6869ff7ce5865ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98131fb37815a73d4006e68c952f1bad77ef42644b7d07b853be09651d6105d`

```dockerfile
```

-	Layers:
	-	`sha256:140b30ce87684e3c6e9c5f84643fa348c06461b4942692e37568d10926fad2b9`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.20.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f29aea68588148a629783b4bd6bf162ca76d5bc4c6eda6cfc469ed410bc7a17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213912519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaab8a5b86778cb30a695f7a7eaf52c75b96092e770f2471fa07f6de1a61d220`
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
# Fri, 27 Mar 2026 17:57:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:10 GMT
ARG VERSION=25.8.20.4
# Fri, 27 Mar 2026 17:57:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:57:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:57:55 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:57:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:57:55 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:57:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:57:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9190cab5ae15f4858810f8f01aad497cbeea40e9f9a0f4dcb8b917d69e569c4f`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 7.6 MB (7577373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9dc3477400d8147f54b18126223384063edbc5a1eba29b68916b679d201de9`  
		Last Modified: Fri, 27 Mar 2026 17:58:18 GMT  
		Size: 178.1 MB (178076094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a011c32af5a8ad314e044ff16a1ab64e88d60c56ec65c097f5d0c07ac047c627`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5716cf75e4ba3878bede3c8c5efe30f690f306bbf3485234ec90e14020a65cda`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe04ec673e58aaf87ffd732ca159d4ee91240e1faaeed9c0bd422622b4cc2218`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5f827941d800c21f7f7e4dfc993457613ad23ec357d5646b3457a87e9e316f`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63719d7d0eca99170add67ae15a32d3c5557561a22075d5c3c3538a252bf88d`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.20.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:51b16ceaa78fe72a0888949b34cb1c4d34bbde4532a3a45ebd9f4035a6fc5162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617616e7b4bed8b8a32993c28cb7987987b0a91e9c39847750e2bcbd41d3ddf1`

```dockerfile
```

-	Layers:
	-	`sha256:8ea2b673759eae99be8b257f1bf7a41a8585a7100b673615446b7d9f27ab06e3`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.20.4-jammy`

```console
$ docker pull clickhouse@sha256:4ef1ad45bc187c91b1cfdfd977871c7ae4940036ebe8b666d42ccf70db004688
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.20.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:55ef1f211514a17a353171fea8c1ade888e379082583e9a783edc79c233ff5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.0 MB (228999206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884d6cad0df35122ece62d68e0d1da0ef84f633195cc510259850cd2f2722f06`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:06 GMT
ARG VERSION=25.8.20.4
# Fri, 27 Mar 2026 17:59:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:32 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:32 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040d6d889b12905b3e5a83996354dfb14bbe228fd3f84454773546fcdfe8247a`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 7.6 MB (7598240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc15689fc695354813c65a3f5c0a081357e4f676276a137317769eb21ccd5101`  
		Last Modified: Fri, 27 Mar 2026 17:59:55 GMT  
		Size: 191.0 MB (190992416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc96acc37198205f7c0c6f6bdbb3b18f35332ec4ce2405f5338704a838ef702`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb94eeb0cdd6fa51d15337578686872b3bf461981c3ef603b93b52c8fdb21f04`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87b23a7034d076dfd8422c419010f07e49f7aa5700b3391eee7e251ffa98099`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125711fdf3aa8247377a37f5c656f90c39bd652262bddef53a04a811205e2c05`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48b498efe644e33d2dd55db901a546cc930e4c43fa6045ab5e1361a0d8bff78`  
		Last Modified: Fri, 27 Mar 2026 17:59:53 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.20.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a150ab55c907ec5661807ccdd7c9785414819c0a03a80b5b6869ff7ce5865ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b98131fb37815a73d4006e68c952f1bad77ef42644b7d07b853be09651d6105d`

```dockerfile
```

-	Layers:
	-	`sha256:140b30ce87684e3c6e9c5f84643fa348c06461b4942692e37568d10926fad2b9`  
		Last Modified: Fri, 27 Mar 2026 17:59:52 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.20.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f29aea68588148a629783b4bd6bf162ca76d5bc4c6eda6cfc469ed410bc7a17b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.9 MB (213912519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaab8a5b86778cb30a695f7a7eaf52c75b96092e770f2471fa07f6de1a61d220`
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
# Fri, 27 Mar 2026 17:57:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:10 GMT
ARG VERSION=25.8.20.4
# Fri, 27 Mar 2026 17:57:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:57:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:57:55 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:57:55 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.20.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:57:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:57:55 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:57:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:57:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9190cab5ae15f4858810f8f01aad497cbeea40e9f9a0f4dcb8b917d69e569c4f`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 7.6 MB (7577373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9dc3477400d8147f54b18126223384063edbc5a1eba29b68916b679d201de9`  
		Last Modified: Fri, 27 Mar 2026 17:58:18 GMT  
		Size: 178.1 MB (178076094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a011c32af5a8ad314e044ff16a1ab64e88d60c56ec65c097f5d0c07ac047c627`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5716cf75e4ba3878bede3c8c5efe30f690f306bbf3485234ec90e14020a65cda`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe04ec673e58aaf87ffd732ca159d4ee91240e1faaeed9c0bd422622b4cc2218`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b5f827941d800c21f7f7e4dfc993457613ad23ec357d5646b3457a87e9e316f`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a63719d7d0eca99170add67ae15a32d3c5557561a22075d5c3c3538a252bf88d`  
		Last Modified: Fri, 27 Mar 2026 17:58:15 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.20.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:51b16ceaa78fe72a0888949b34cb1c4d34bbde4532a3a45ebd9f4035a6fc5162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617616e7b4bed8b8a32993c28cb7987987b0a91e9c39847750e2bcbd41d3ddf1`

```dockerfile
```

-	Layers:
	-	`sha256:8ea2b673759eae99be8b257f1bf7a41a8585a7100b673615446b7d9f27ab06e3`  
		Last Modified: Fri, 27 Mar 2026 17:58:14 GMT  
		Size: 25.6 KB (25609 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1`

```console
$ docker pull clickhouse@sha256:8b8800dc4fb1d6ea6d4780614fc0326a940fcac27d939b278ae1411aad3874d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:881262726ee1c7782f3ad3928f354a539271ec519b64a02c12bed1e8d368aaf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246092652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37a73cc89458859d3464d2293bd97c6c779e222134275224dfdb8777d4a24b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:07 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:07 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:07 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:07 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:07 GMT
ARG VERSION=26.1.6.6
# Fri, 27 Mar 2026 17:59:07 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:39 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7906ca226064ab4899817f9c97187fbc55aa4715fa7bebe2e8ae864c2471e03f`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 7.6 MB (7598285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfde37f3b0a16b39b6fd0e9805d45e4983b40228b7e51489886b01220207329`  
		Last Modified: Fri, 27 Mar 2026 18:00:07 GMT  
		Size: 208.1 MB (208085797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca8922d442f5411dd8f1c5eb90e608a14d61d1c20999364e33831fb2d5b9a1`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18da8d896c9fbbddc758acac4b2d0eeadebcac684b5c13128e44ccd1e6ce575f`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa437ed0d38fb3fd3a7988c64b41b3de7445bde6b7f02a37a3213b657d77d50e`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46463bd3ef128433cc216497bc0a75b91e45be53cfbdd0eb6d7cc2d71c449d1`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65036d9c49fee9f1ee2a14996827d1e64a903182295c11752c81367b12087416`  
		Last Modified: Fri, 27 Mar 2026 18:00:07 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:990fe138d7bd3403e9f6a72c9967313f01d75fb50846c15d58c7022746ed698c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cd4f9f81dd811b9ccba350a450e965ead167c5bd17fb6187a85b041fdc4d14`

```dockerfile
```

-	Layers:
	-	`sha256:2e70187418a5458cb841fcbdf2ca884d13c40c33a812f0c88fe4ca5e0a598b67`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 25.4 KB (25407 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b0c75761f21455f637d311623d800e29a4197c96c7e9a58fac0183010455405d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228273185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9fd60768e032ec3ee2ac7a89b0ca86c2541d7ed475def7e9c8d0a2fd8bdd82`
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
# Fri, 27 Mar 2026 17:57:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:33 GMT
ARG VERSION=26.1.6.6
# Fri, 27 Mar 2026 17:57:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:14 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:14 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032568a426d8235adbfd3ba7e1c64d5d26daa35dc8958f2fb0626cf535414c29`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 7.6 MB (7577342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344c4c0eb9c697eedaac19c7f6aa6fdf1e874d1ad6e22df3480b9f557d0ccb71`  
		Last Modified: Fri, 27 Mar 2026 17:58:40 GMT  
		Size: 192.4 MB (192436768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82f3e6fa129534db0eb1285bd8583428f90c55c5aea12b70bf472bdefaac8a`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797efd5581a73d69424fe6afc3e614dc354f842cfa6d96588f02b57b052ae94c`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a023747a17e355fc2a6ab9efa950b07d080dc8fd5271f266af0f1652481f552`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b8acade8928aa7628e94d632d373c942b7fbf955279fd15d943adae3daf7a8`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c152a298985dfab61f8a939fa9c5874ece7e36906398e8079ac1c2e3d0a9fa09`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f7ec52235ee72bbdcebae410ea6a4dad6be36073dffe917875553b3894a25df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb7d94cf62f2d70030fa7135296c67bf74ecda1e4d2865c8b615c20d8caf6db`

```dockerfile
```

-	Layers:
	-	`sha256:11f6f83690662cb7dd4717e5d86088470179fe009f6ef6238c73e37f21a7ee40`  
		Last Modified: Fri, 27 Mar 2026 17:58:35 GMT  
		Size: 25.6 KB (25595 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1-jammy`

```console
$ docker pull clickhouse@sha256:8b8800dc4fb1d6ea6d4780614fc0326a940fcac27d939b278ae1411aad3874d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:881262726ee1c7782f3ad3928f354a539271ec519b64a02c12bed1e8d368aaf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246092652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37a73cc89458859d3464d2293bd97c6c779e222134275224dfdb8777d4a24b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:07 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:07 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:07 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:07 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:07 GMT
ARG VERSION=26.1.6.6
# Fri, 27 Mar 2026 17:59:07 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:39 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7906ca226064ab4899817f9c97187fbc55aa4715fa7bebe2e8ae864c2471e03f`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 7.6 MB (7598285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfde37f3b0a16b39b6fd0e9805d45e4983b40228b7e51489886b01220207329`  
		Last Modified: Fri, 27 Mar 2026 18:00:07 GMT  
		Size: 208.1 MB (208085797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca8922d442f5411dd8f1c5eb90e608a14d61d1c20999364e33831fb2d5b9a1`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18da8d896c9fbbddc758acac4b2d0eeadebcac684b5c13128e44ccd1e6ce575f`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa437ed0d38fb3fd3a7988c64b41b3de7445bde6b7f02a37a3213b657d77d50e`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46463bd3ef128433cc216497bc0a75b91e45be53cfbdd0eb6d7cc2d71c449d1`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65036d9c49fee9f1ee2a14996827d1e64a903182295c11752c81367b12087416`  
		Last Modified: Fri, 27 Mar 2026 18:00:07 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:990fe138d7bd3403e9f6a72c9967313f01d75fb50846c15d58c7022746ed698c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cd4f9f81dd811b9ccba350a450e965ead167c5bd17fb6187a85b041fdc4d14`

```dockerfile
```

-	Layers:
	-	`sha256:2e70187418a5458cb841fcbdf2ca884d13c40c33a812f0c88fe4ca5e0a598b67`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 25.4 KB (25407 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b0c75761f21455f637d311623d800e29a4197c96c7e9a58fac0183010455405d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228273185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9fd60768e032ec3ee2ac7a89b0ca86c2541d7ed475def7e9c8d0a2fd8bdd82`
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
# Fri, 27 Mar 2026 17:57:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:33 GMT
ARG VERSION=26.1.6.6
# Fri, 27 Mar 2026 17:57:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:14 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:14 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032568a426d8235adbfd3ba7e1c64d5d26daa35dc8958f2fb0626cf535414c29`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 7.6 MB (7577342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344c4c0eb9c697eedaac19c7f6aa6fdf1e874d1ad6e22df3480b9f557d0ccb71`  
		Last Modified: Fri, 27 Mar 2026 17:58:40 GMT  
		Size: 192.4 MB (192436768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82f3e6fa129534db0eb1285bd8583428f90c55c5aea12b70bf472bdefaac8a`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797efd5581a73d69424fe6afc3e614dc354f842cfa6d96588f02b57b052ae94c`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a023747a17e355fc2a6ab9efa950b07d080dc8fd5271f266af0f1652481f552`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b8acade8928aa7628e94d632d373c942b7fbf955279fd15d943adae3daf7a8`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c152a298985dfab61f8a939fa9c5874ece7e36906398e8079ac1c2e3d0a9fa09`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f7ec52235ee72bbdcebae410ea6a4dad6be36073dffe917875553b3894a25df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb7d94cf62f2d70030fa7135296c67bf74ecda1e4d2865c8b615c20d8caf6db`

```dockerfile
```

-	Layers:
	-	`sha256:11f6f83690662cb7dd4717e5d86088470179fe009f6ef6238c73e37f21a7ee40`  
		Last Modified: Fri, 27 Mar 2026 17:58:35 GMT  
		Size: 25.6 KB (25595 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.6`

```console
$ docker pull clickhouse@sha256:8b8800dc4fb1d6ea6d4780614fc0326a940fcac27d939b278ae1411aad3874d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:881262726ee1c7782f3ad3928f354a539271ec519b64a02c12bed1e8d368aaf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246092652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37a73cc89458859d3464d2293bd97c6c779e222134275224dfdb8777d4a24b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:07 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:07 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:07 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:07 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:07 GMT
ARG VERSION=26.1.6.6
# Fri, 27 Mar 2026 17:59:07 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:39 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7906ca226064ab4899817f9c97187fbc55aa4715fa7bebe2e8ae864c2471e03f`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 7.6 MB (7598285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfde37f3b0a16b39b6fd0e9805d45e4983b40228b7e51489886b01220207329`  
		Last Modified: Fri, 27 Mar 2026 18:00:07 GMT  
		Size: 208.1 MB (208085797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca8922d442f5411dd8f1c5eb90e608a14d61d1c20999364e33831fb2d5b9a1`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18da8d896c9fbbddc758acac4b2d0eeadebcac684b5c13128e44ccd1e6ce575f`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa437ed0d38fb3fd3a7988c64b41b3de7445bde6b7f02a37a3213b657d77d50e`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46463bd3ef128433cc216497bc0a75b91e45be53cfbdd0eb6d7cc2d71c449d1`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65036d9c49fee9f1ee2a14996827d1e64a903182295c11752c81367b12087416`  
		Last Modified: Fri, 27 Mar 2026 18:00:07 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:990fe138d7bd3403e9f6a72c9967313f01d75fb50846c15d58c7022746ed698c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cd4f9f81dd811b9ccba350a450e965ead167c5bd17fb6187a85b041fdc4d14`

```dockerfile
```

-	Layers:
	-	`sha256:2e70187418a5458cb841fcbdf2ca884d13c40c33a812f0c88fe4ca5e0a598b67`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 25.4 KB (25407 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b0c75761f21455f637d311623d800e29a4197c96c7e9a58fac0183010455405d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228273185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9fd60768e032ec3ee2ac7a89b0ca86c2541d7ed475def7e9c8d0a2fd8bdd82`
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
# Fri, 27 Mar 2026 17:57:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:33 GMT
ARG VERSION=26.1.6.6
# Fri, 27 Mar 2026 17:57:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:14 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:14 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032568a426d8235adbfd3ba7e1c64d5d26daa35dc8958f2fb0626cf535414c29`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 7.6 MB (7577342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344c4c0eb9c697eedaac19c7f6aa6fdf1e874d1ad6e22df3480b9f557d0ccb71`  
		Last Modified: Fri, 27 Mar 2026 17:58:40 GMT  
		Size: 192.4 MB (192436768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82f3e6fa129534db0eb1285bd8583428f90c55c5aea12b70bf472bdefaac8a`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797efd5581a73d69424fe6afc3e614dc354f842cfa6d96588f02b57b052ae94c`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a023747a17e355fc2a6ab9efa950b07d080dc8fd5271f266af0f1652481f552`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b8acade8928aa7628e94d632d373c942b7fbf955279fd15d943adae3daf7a8`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c152a298985dfab61f8a939fa9c5874ece7e36906398e8079ac1c2e3d0a9fa09`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f7ec52235ee72bbdcebae410ea6a4dad6be36073dffe917875553b3894a25df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb7d94cf62f2d70030fa7135296c67bf74ecda1e4d2865c8b615c20d8caf6db`

```dockerfile
```

-	Layers:
	-	`sha256:11f6f83690662cb7dd4717e5d86088470179fe009f6ef6238c73e37f21a7ee40`  
		Last Modified: Fri, 27 Mar 2026 17:58:35 GMT  
		Size: 25.6 KB (25595 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.6-jammy`

```console
$ docker pull clickhouse@sha256:8b8800dc4fb1d6ea6d4780614fc0326a940fcac27d939b278ae1411aad3874d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:881262726ee1c7782f3ad3928f354a539271ec519b64a02c12bed1e8d368aaf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246092652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37a73cc89458859d3464d2293bd97c6c779e222134275224dfdb8777d4a24b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:07 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:07 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:07 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:07 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:07 GMT
ARG VERSION=26.1.6.6
# Fri, 27 Mar 2026 17:59:07 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:39 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7906ca226064ab4899817f9c97187fbc55aa4715fa7bebe2e8ae864c2471e03f`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 7.6 MB (7598285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfde37f3b0a16b39b6fd0e9805d45e4983b40228b7e51489886b01220207329`  
		Last Modified: Fri, 27 Mar 2026 18:00:07 GMT  
		Size: 208.1 MB (208085797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca8922d442f5411dd8f1c5eb90e608a14d61d1c20999364e33831fb2d5b9a1`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18da8d896c9fbbddc758acac4b2d0eeadebcac684b5c13128e44ccd1e6ce575f`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa437ed0d38fb3fd3a7988c64b41b3de7445bde6b7f02a37a3213b657d77d50e`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46463bd3ef128433cc216497bc0a75b91e45be53cfbdd0eb6d7cc2d71c449d1`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65036d9c49fee9f1ee2a14996827d1e64a903182295c11752c81367b12087416`  
		Last Modified: Fri, 27 Mar 2026 18:00:07 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:990fe138d7bd3403e9f6a72c9967313f01d75fb50846c15d58c7022746ed698c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cd4f9f81dd811b9ccba350a450e965ead167c5bd17fb6187a85b041fdc4d14`

```dockerfile
```

-	Layers:
	-	`sha256:2e70187418a5458cb841fcbdf2ca884d13c40c33a812f0c88fe4ca5e0a598b67`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 25.4 KB (25407 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b0c75761f21455f637d311623d800e29a4197c96c7e9a58fac0183010455405d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228273185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9fd60768e032ec3ee2ac7a89b0ca86c2541d7ed475def7e9c8d0a2fd8bdd82`
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
# Fri, 27 Mar 2026 17:57:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:33 GMT
ARG VERSION=26.1.6.6
# Fri, 27 Mar 2026 17:57:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:14 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:14 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032568a426d8235adbfd3ba7e1c64d5d26daa35dc8958f2fb0626cf535414c29`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 7.6 MB (7577342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344c4c0eb9c697eedaac19c7f6aa6fdf1e874d1ad6e22df3480b9f557d0ccb71`  
		Last Modified: Fri, 27 Mar 2026 17:58:40 GMT  
		Size: 192.4 MB (192436768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82f3e6fa129534db0eb1285bd8583428f90c55c5aea12b70bf472bdefaac8a`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797efd5581a73d69424fe6afc3e614dc354f842cfa6d96588f02b57b052ae94c`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a023747a17e355fc2a6ab9efa950b07d080dc8fd5271f266af0f1652481f552`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b8acade8928aa7628e94d632d373c942b7fbf955279fd15d943adae3daf7a8`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c152a298985dfab61f8a939fa9c5874ece7e36906398e8079ac1c2e3d0a9fa09`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f7ec52235ee72bbdcebae410ea6a4dad6be36073dffe917875553b3894a25df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb7d94cf62f2d70030fa7135296c67bf74ecda1e4d2865c8b615c20d8caf6db`

```dockerfile
```

-	Layers:
	-	`sha256:11f6f83690662cb7dd4717e5d86088470179fe009f6ef6238c73e37f21a7ee40`  
		Last Modified: Fri, 27 Mar 2026 17:58:35 GMT  
		Size: 25.6 KB (25595 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.6.6`

```console
$ docker pull clickhouse@sha256:8b8800dc4fb1d6ea6d4780614fc0326a940fcac27d939b278ae1411aad3874d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.6.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:881262726ee1c7782f3ad3928f354a539271ec519b64a02c12bed1e8d368aaf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246092652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37a73cc89458859d3464d2293bd97c6c779e222134275224dfdb8777d4a24b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:07 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:07 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:07 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:07 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:07 GMT
ARG VERSION=26.1.6.6
# Fri, 27 Mar 2026 17:59:07 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:39 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7906ca226064ab4899817f9c97187fbc55aa4715fa7bebe2e8ae864c2471e03f`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 7.6 MB (7598285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfde37f3b0a16b39b6fd0e9805d45e4983b40228b7e51489886b01220207329`  
		Last Modified: Fri, 27 Mar 2026 18:00:07 GMT  
		Size: 208.1 MB (208085797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca8922d442f5411dd8f1c5eb90e608a14d61d1c20999364e33831fb2d5b9a1`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18da8d896c9fbbddc758acac4b2d0eeadebcac684b5c13128e44ccd1e6ce575f`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa437ed0d38fb3fd3a7988c64b41b3de7445bde6b7f02a37a3213b657d77d50e`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46463bd3ef128433cc216497bc0a75b91e45be53cfbdd0eb6d7cc2d71c449d1`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65036d9c49fee9f1ee2a14996827d1e64a903182295c11752c81367b12087416`  
		Last Modified: Fri, 27 Mar 2026 18:00:07 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.6.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:990fe138d7bd3403e9f6a72c9967313f01d75fb50846c15d58c7022746ed698c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cd4f9f81dd811b9ccba350a450e965ead167c5bd17fb6187a85b041fdc4d14`

```dockerfile
```

-	Layers:
	-	`sha256:2e70187418a5458cb841fcbdf2ca884d13c40c33a812f0c88fe4ca5e0a598b67`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 25.4 KB (25407 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.6.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b0c75761f21455f637d311623d800e29a4197c96c7e9a58fac0183010455405d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228273185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9fd60768e032ec3ee2ac7a89b0ca86c2541d7ed475def7e9c8d0a2fd8bdd82`
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
# Fri, 27 Mar 2026 17:57:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:33 GMT
ARG VERSION=26.1.6.6
# Fri, 27 Mar 2026 17:57:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:14 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:14 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032568a426d8235adbfd3ba7e1c64d5d26daa35dc8958f2fb0626cf535414c29`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 7.6 MB (7577342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344c4c0eb9c697eedaac19c7f6aa6fdf1e874d1ad6e22df3480b9f557d0ccb71`  
		Last Modified: Fri, 27 Mar 2026 17:58:40 GMT  
		Size: 192.4 MB (192436768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82f3e6fa129534db0eb1285bd8583428f90c55c5aea12b70bf472bdefaac8a`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797efd5581a73d69424fe6afc3e614dc354f842cfa6d96588f02b57b052ae94c`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a023747a17e355fc2a6ab9efa950b07d080dc8fd5271f266af0f1652481f552`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b8acade8928aa7628e94d632d373c942b7fbf955279fd15d943adae3daf7a8`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c152a298985dfab61f8a939fa9c5874ece7e36906398e8079ac1c2e3d0a9fa09`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.6.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f7ec52235ee72bbdcebae410ea6a4dad6be36073dffe917875553b3894a25df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb7d94cf62f2d70030fa7135296c67bf74ecda1e4d2865c8b615c20d8caf6db`

```dockerfile
```

-	Layers:
	-	`sha256:11f6f83690662cb7dd4717e5d86088470179fe009f6ef6238c73e37f21a7ee40`  
		Last Modified: Fri, 27 Mar 2026 17:58:35 GMT  
		Size: 25.6 KB (25595 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.6.6-jammy`

```console
$ docker pull clickhouse@sha256:8b8800dc4fb1d6ea6d4780614fc0326a940fcac27d939b278ae1411aad3874d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.6.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:881262726ee1c7782f3ad3928f354a539271ec519b64a02c12bed1e8d368aaf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246092652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c37a73cc89458859d3464d2293bd97c6c779e222134275224dfdb8777d4a24b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:07 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:07 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:07 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:07 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:07 GMT
ARG VERSION=26.1.6.6
# Fri, 27 Mar 2026 17:59:07 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:39 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7906ca226064ab4899817f9c97187fbc55aa4715fa7bebe2e8ae864c2471e03f`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 7.6 MB (7598285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dfde37f3b0a16b39b6fd0e9805d45e4983b40228b7e51489886b01220207329`  
		Last Modified: Fri, 27 Mar 2026 18:00:07 GMT  
		Size: 208.1 MB (208085797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca8922d442f5411dd8f1c5eb90e608a14d61d1c20999364e33831fb2d5b9a1`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18da8d896c9fbbddc758acac4b2d0eeadebcac684b5c13128e44ccd1e6ce575f`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa437ed0d38fb3fd3a7988c64b41b3de7445bde6b7f02a37a3213b657d77d50e`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46463bd3ef128433cc216497bc0a75b91e45be53cfbdd0eb6d7cc2d71c449d1`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65036d9c49fee9f1ee2a14996827d1e64a903182295c11752c81367b12087416`  
		Last Modified: Fri, 27 Mar 2026 18:00:07 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.6.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:990fe138d7bd3403e9f6a72c9967313f01d75fb50846c15d58c7022746ed698c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cd4f9f81dd811b9ccba350a450e965ead167c5bd17fb6187a85b041fdc4d14`

```dockerfile
```

-	Layers:
	-	`sha256:2e70187418a5458cb841fcbdf2ca884d13c40c33a812f0c88fe4ca5e0a598b67`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 25.4 KB (25407 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.6.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b0c75761f21455f637d311623d800e29a4197c96c7e9a58fac0183010455405d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228273185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf9fd60768e032ec3ee2ac7a89b0ca86c2541d7ed475def7e9c8d0a2fd8bdd82`
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
# Fri, 27 Mar 2026 17:57:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:33 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:33 GMT
ARG VERSION=26.1.6.6
# Fri, 27 Mar 2026 17:57:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:14 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.6.6 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:14 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032568a426d8235adbfd3ba7e1c64d5d26daa35dc8958f2fb0626cf535414c29`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 7.6 MB (7577342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344c4c0eb9c697eedaac19c7f6aa6fdf1e874d1ad6e22df3480b9f557d0ccb71`  
		Last Modified: Fri, 27 Mar 2026 17:58:40 GMT  
		Size: 192.4 MB (192436768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd82f3e6fa129534db0eb1285bd8583428f90c55c5aea12b70bf472bdefaac8a`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797efd5581a73d69424fe6afc3e614dc354f842cfa6d96588f02b57b052ae94c`  
		Last Modified: Fri, 27 Mar 2026 17:58:36 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a023747a17e355fc2a6ab9efa950b07d080dc8fd5271f266af0f1652481f552`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b8acade8928aa7628e94d632d373c942b7fbf955279fd15d943adae3daf7a8`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c152a298985dfab61f8a939fa9c5874ece7e36906398e8079ac1c2e3d0a9fa09`  
		Last Modified: Fri, 27 Mar 2026 17:58:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.6.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f7ec52235ee72bbdcebae410ea6a4dad6be36073dffe917875553b3894a25df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb7d94cf62f2d70030fa7135296c67bf74ecda1e4d2865c8b615c20d8caf6db`

```dockerfile
```

-	Layers:
	-	`sha256:11f6f83690662cb7dd4717e5d86088470179fe009f6ef6238c73e37f21a7ee40`  
		Last Modified: Fri, 27 Mar 2026 17:58:35 GMT  
		Size: 25.6 KB (25595 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2`

```console
$ docker pull clickhouse@sha256:cd3c22da7555296e43af71f1e31596269662c1ceb93c9b158a2a9af6e872892b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:d98e0406d2e33873aa6528b714c4d19cf55bf2512d200404ec944e6991d7b11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253596378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406bcbbb409379f93813cfb93e4e7b3eedf79bc4b22e995cd1a600fe8dabfd9a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:01 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:01 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:01 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:01 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:01 GMT
ARG VERSION=26.2.5.45
# Fri, 27 Mar 2026 17:59:01 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:39 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db352a89196559645a31564305abc482406fff1b4acf9c9dd0e61b87d5bd1221`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 7.6 MB (7598264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38da43cbd46ec1ed46ecf7d35d16c3f886e5c1ca7c49330977fe98c80a5b5b54`  
		Last Modified: Fri, 27 Mar 2026 18:00:17 GMT  
		Size: 215.6 MB (215589543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca8922d442f5411dd8f1c5eb90e608a14d61d1c20999364e33831fb2d5b9a1`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d72789abcbc6e4a70a5e04b67f17e3f357abe9423a5589efb632e7fee24f564`  
		Last Modified: Fri, 27 Mar 2026 18:00:10 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa437ed0d38fb3fd3a7988c64b41b3de7445bde6b7f02a37a3213b657d77d50e`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df7ec7d8671e1f6429085753abe654a97e6ae95a44b1c857a28f7f12ea52bf4`  
		Last Modified: Fri, 27 Mar 2026 18:00:10 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e385387b6b29f2d90d62056f635092668524d5548ad0edeacf7bcc91db8d0a9`  
		Last Modified: Fri, 27 Mar 2026 18:00:11 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1dab19e20fe7f530efbc1ba62fcea1a6c7d3ae6294deb08e1e1010a1aac738b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8553df0a3a8f53eea0ec32e74a5cb28fb5292beba7a6c17ef5c6f3a92f340b12`

```dockerfile
```

-	Layers:
	-	`sha256:344fcbebc6ecd30f99b69cb192fd186127c728ab63fe0358b5223c0248e99cec`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 25.4 KB (25417 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ad60b00e0043303f5f86ab8072c200fd0796e71a360a616be0161b3dc2fb6168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237198556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9bc4c7144dfc471ac54c3d54e7fb3bb2c779555782d2240711e3ebad16c42f9`
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
# Fri, 27 Mar 2026 17:56:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:56:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:56:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:56:31 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:56:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:56:31 GMT
ARG VERSION=26.2.5.45
# Fri, 27 Mar 2026 17:56:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:57:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:57:35 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:57:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:57:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:57:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:57:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42907f324322db4092a6e1759337b7c155f124654b86e3db9c9145c8b513fb73`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 7.6 MB (7577344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6211d7ec1ef1854a49843ce280f379d49d63bdd72f738dac0f480b2b59a89c1`  
		Last Modified: Fri, 27 Mar 2026 17:58:01 GMT  
		Size: 201.4 MB (201362135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea22498ec33d677a20ac8084113c5b3e9408b41ef92e0bb91da96cbfff24ff3c`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd99754186a9a893e32e3d3dea41037ac83125adbc74089272c9c724aabf736`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7f9e9e56af1c86f1d65bd5a6173845ca30f8b04af9f747c0f90eb24b992e23`  
		Last Modified: Fri, 27 Mar 2026 17:57:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03a4888a87e8053432a380eceb2965d56c7992f1604abdd190e3eca1275b72d`  
		Last Modified: Fri, 27 Mar 2026 17:57:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7fc1e0ff56024ba35e5252681ae4e86e799a24bd14db482565a30d72929ad4`  
		Last Modified: Fri, 27 Mar 2026 17:57:59 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:14f8da7f51451ef062cda65ee1fc220d3ee21d3c3bf25ec7ed55db6c146c1538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5b93c526f3e88afa84640bd1eae8d7807fe4ba73ceb03dd23cc871ec85e176`

```dockerfile
```

-	Layers:
	-	`sha256:2c7652a332c1dbb39d63ee5d1899520818de246a1b958d81bfc330c1e59dd1f1`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2-jammy`

```console
$ docker pull clickhouse@sha256:cd3c22da7555296e43af71f1e31596269662c1ceb93c9b158a2a9af6e872892b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:d98e0406d2e33873aa6528b714c4d19cf55bf2512d200404ec944e6991d7b11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253596378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406bcbbb409379f93813cfb93e4e7b3eedf79bc4b22e995cd1a600fe8dabfd9a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:01 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:01 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:01 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:01 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:01 GMT
ARG VERSION=26.2.5.45
# Fri, 27 Mar 2026 17:59:01 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:39 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db352a89196559645a31564305abc482406fff1b4acf9c9dd0e61b87d5bd1221`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 7.6 MB (7598264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38da43cbd46ec1ed46ecf7d35d16c3f886e5c1ca7c49330977fe98c80a5b5b54`  
		Last Modified: Fri, 27 Mar 2026 18:00:17 GMT  
		Size: 215.6 MB (215589543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca8922d442f5411dd8f1c5eb90e608a14d61d1c20999364e33831fb2d5b9a1`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d72789abcbc6e4a70a5e04b67f17e3f357abe9423a5589efb632e7fee24f564`  
		Last Modified: Fri, 27 Mar 2026 18:00:10 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa437ed0d38fb3fd3a7988c64b41b3de7445bde6b7f02a37a3213b657d77d50e`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df7ec7d8671e1f6429085753abe654a97e6ae95a44b1c857a28f7f12ea52bf4`  
		Last Modified: Fri, 27 Mar 2026 18:00:10 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e385387b6b29f2d90d62056f635092668524d5548ad0edeacf7bcc91db8d0a9`  
		Last Modified: Fri, 27 Mar 2026 18:00:11 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1dab19e20fe7f530efbc1ba62fcea1a6c7d3ae6294deb08e1e1010a1aac738b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8553df0a3a8f53eea0ec32e74a5cb28fb5292beba7a6c17ef5c6f3a92f340b12`

```dockerfile
```

-	Layers:
	-	`sha256:344fcbebc6ecd30f99b69cb192fd186127c728ab63fe0358b5223c0248e99cec`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 25.4 KB (25417 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ad60b00e0043303f5f86ab8072c200fd0796e71a360a616be0161b3dc2fb6168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237198556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9bc4c7144dfc471ac54c3d54e7fb3bb2c779555782d2240711e3ebad16c42f9`
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
# Fri, 27 Mar 2026 17:56:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:56:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:56:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:56:31 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:56:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:56:31 GMT
ARG VERSION=26.2.5.45
# Fri, 27 Mar 2026 17:56:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:57:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:57:35 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:57:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:57:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:57:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:57:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42907f324322db4092a6e1759337b7c155f124654b86e3db9c9145c8b513fb73`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 7.6 MB (7577344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6211d7ec1ef1854a49843ce280f379d49d63bdd72f738dac0f480b2b59a89c1`  
		Last Modified: Fri, 27 Mar 2026 17:58:01 GMT  
		Size: 201.4 MB (201362135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea22498ec33d677a20ac8084113c5b3e9408b41ef92e0bb91da96cbfff24ff3c`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd99754186a9a893e32e3d3dea41037ac83125adbc74089272c9c724aabf736`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7f9e9e56af1c86f1d65bd5a6173845ca30f8b04af9f747c0f90eb24b992e23`  
		Last Modified: Fri, 27 Mar 2026 17:57:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03a4888a87e8053432a380eceb2965d56c7992f1604abdd190e3eca1275b72d`  
		Last Modified: Fri, 27 Mar 2026 17:57:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7fc1e0ff56024ba35e5252681ae4e86e799a24bd14db482565a30d72929ad4`  
		Last Modified: Fri, 27 Mar 2026 17:57:59 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:14f8da7f51451ef062cda65ee1fc220d3ee21d3c3bf25ec7ed55db6c146c1538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5b93c526f3e88afa84640bd1eae8d7807fe4ba73ceb03dd23cc871ec85e176`

```dockerfile
```

-	Layers:
	-	`sha256:2c7652a332c1dbb39d63ee5d1899520818de246a1b958d81bfc330c1e59dd1f1`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.5`

```console
$ docker pull clickhouse@sha256:cd3c22da7555296e43af71f1e31596269662c1ceb93c9b158a2a9af6e872892b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:d98e0406d2e33873aa6528b714c4d19cf55bf2512d200404ec944e6991d7b11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253596378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406bcbbb409379f93813cfb93e4e7b3eedf79bc4b22e995cd1a600fe8dabfd9a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:01 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:01 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:01 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:01 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:01 GMT
ARG VERSION=26.2.5.45
# Fri, 27 Mar 2026 17:59:01 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:39 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db352a89196559645a31564305abc482406fff1b4acf9c9dd0e61b87d5bd1221`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 7.6 MB (7598264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38da43cbd46ec1ed46ecf7d35d16c3f886e5c1ca7c49330977fe98c80a5b5b54`  
		Last Modified: Fri, 27 Mar 2026 18:00:17 GMT  
		Size: 215.6 MB (215589543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca8922d442f5411dd8f1c5eb90e608a14d61d1c20999364e33831fb2d5b9a1`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d72789abcbc6e4a70a5e04b67f17e3f357abe9423a5589efb632e7fee24f564`  
		Last Modified: Fri, 27 Mar 2026 18:00:10 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa437ed0d38fb3fd3a7988c64b41b3de7445bde6b7f02a37a3213b657d77d50e`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df7ec7d8671e1f6429085753abe654a97e6ae95a44b1c857a28f7f12ea52bf4`  
		Last Modified: Fri, 27 Mar 2026 18:00:10 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e385387b6b29f2d90d62056f635092668524d5548ad0edeacf7bcc91db8d0a9`  
		Last Modified: Fri, 27 Mar 2026 18:00:11 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1dab19e20fe7f530efbc1ba62fcea1a6c7d3ae6294deb08e1e1010a1aac738b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8553df0a3a8f53eea0ec32e74a5cb28fb5292beba7a6c17ef5c6f3a92f340b12`

```dockerfile
```

-	Layers:
	-	`sha256:344fcbebc6ecd30f99b69cb192fd186127c728ab63fe0358b5223c0248e99cec`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 25.4 KB (25417 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ad60b00e0043303f5f86ab8072c200fd0796e71a360a616be0161b3dc2fb6168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237198556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9bc4c7144dfc471ac54c3d54e7fb3bb2c779555782d2240711e3ebad16c42f9`
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
# Fri, 27 Mar 2026 17:56:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:56:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:56:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:56:31 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:56:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:56:31 GMT
ARG VERSION=26.2.5.45
# Fri, 27 Mar 2026 17:56:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:57:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:57:35 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:57:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:57:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:57:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:57:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42907f324322db4092a6e1759337b7c155f124654b86e3db9c9145c8b513fb73`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 7.6 MB (7577344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6211d7ec1ef1854a49843ce280f379d49d63bdd72f738dac0f480b2b59a89c1`  
		Last Modified: Fri, 27 Mar 2026 17:58:01 GMT  
		Size: 201.4 MB (201362135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea22498ec33d677a20ac8084113c5b3e9408b41ef92e0bb91da96cbfff24ff3c`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd99754186a9a893e32e3d3dea41037ac83125adbc74089272c9c724aabf736`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7f9e9e56af1c86f1d65bd5a6173845ca30f8b04af9f747c0f90eb24b992e23`  
		Last Modified: Fri, 27 Mar 2026 17:57:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03a4888a87e8053432a380eceb2965d56c7992f1604abdd190e3eca1275b72d`  
		Last Modified: Fri, 27 Mar 2026 17:57:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7fc1e0ff56024ba35e5252681ae4e86e799a24bd14db482565a30d72929ad4`  
		Last Modified: Fri, 27 Mar 2026 17:57:59 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:14f8da7f51451ef062cda65ee1fc220d3ee21d3c3bf25ec7ed55db6c146c1538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5b93c526f3e88afa84640bd1eae8d7807fe4ba73ceb03dd23cc871ec85e176`

```dockerfile
```

-	Layers:
	-	`sha256:2c7652a332c1dbb39d63ee5d1899520818de246a1b958d81bfc330c1e59dd1f1`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.5-jammy`

```console
$ docker pull clickhouse@sha256:cd3c22da7555296e43af71f1e31596269662c1ceb93c9b158a2a9af6e872892b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:d98e0406d2e33873aa6528b714c4d19cf55bf2512d200404ec944e6991d7b11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253596378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406bcbbb409379f93813cfb93e4e7b3eedf79bc4b22e995cd1a600fe8dabfd9a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:01 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:01 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:01 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:01 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:01 GMT
ARG VERSION=26.2.5.45
# Fri, 27 Mar 2026 17:59:01 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:39 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db352a89196559645a31564305abc482406fff1b4acf9c9dd0e61b87d5bd1221`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 7.6 MB (7598264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38da43cbd46ec1ed46ecf7d35d16c3f886e5c1ca7c49330977fe98c80a5b5b54`  
		Last Modified: Fri, 27 Mar 2026 18:00:17 GMT  
		Size: 215.6 MB (215589543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca8922d442f5411dd8f1c5eb90e608a14d61d1c20999364e33831fb2d5b9a1`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d72789abcbc6e4a70a5e04b67f17e3f357abe9423a5589efb632e7fee24f564`  
		Last Modified: Fri, 27 Mar 2026 18:00:10 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa437ed0d38fb3fd3a7988c64b41b3de7445bde6b7f02a37a3213b657d77d50e`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df7ec7d8671e1f6429085753abe654a97e6ae95a44b1c857a28f7f12ea52bf4`  
		Last Modified: Fri, 27 Mar 2026 18:00:10 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e385387b6b29f2d90d62056f635092668524d5548ad0edeacf7bcc91db8d0a9`  
		Last Modified: Fri, 27 Mar 2026 18:00:11 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1dab19e20fe7f530efbc1ba62fcea1a6c7d3ae6294deb08e1e1010a1aac738b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8553df0a3a8f53eea0ec32e74a5cb28fb5292beba7a6c17ef5c6f3a92f340b12`

```dockerfile
```

-	Layers:
	-	`sha256:344fcbebc6ecd30f99b69cb192fd186127c728ab63fe0358b5223c0248e99cec`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 25.4 KB (25417 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ad60b00e0043303f5f86ab8072c200fd0796e71a360a616be0161b3dc2fb6168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237198556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9bc4c7144dfc471ac54c3d54e7fb3bb2c779555782d2240711e3ebad16c42f9`
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
# Fri, 27 Mar 2026 17:56:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:56:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:56:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:56:31 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:56:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:56:31 GMT
ARG VERSION=26.2.5.45
# Fri, 27 Mar 2026 17:56:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:57:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:57:35 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:57:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:57:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:57:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:57:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42907f324322db4092a6e1759337b7c155f124654b86e3db9c9145c8b513fb73`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 7.6 MB (7577344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6211d7ec1ef1854a49843ce280f379d49d63bdd72f738dac0f480b2b59a89c1`  
		Last Modified: Fri, 27 Mar 2026 17:58:01 GMT  
		Size: 201.4 MB (201362135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea22498ec33d677a20ac8084113c5b3e9408b41ef92e0bb91da96cbfff24ff3c`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd99754186a9a893e32e3d3dea41037ac83125adbc74089272c9c724aabf736`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7f9e9e56af1c86f1d65bd5a6173845ca30f8b04af9f747c0f90eb24b992e23`  
		Last Modified: Fri, 27 Mar 2026 17:57:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03a4888a87e8053432a380eceb2965d56c7992f1604abdd190e3eca1275b72d`  
		Last Modified: Fri, 27 Mar 2026 17:57:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7fc1e0ff56024ba35e5252681ae4e86e799a24bd14db482565a30d72929ad4`  
		Last Modified: Fri, 27 Mar 2026 17:57:59 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:14f8da7f51451ef062cda65ee1fc220d3ee21d3c3bf25ec7ed55db6c146c1538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5b93c526f3e88afa84640bd1eae8d7807fe4ba73ceb03dd23cc871ec85e176`

```dockerfile
```

-	Layers:
	-	`sha256:2c7652a332c1dbb39d63ee5d1899520818de246a1b958d81bfc330c1e59dd1f1`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.5.45`

```console
$ docker pull clickhouse@sha256:cd3c22da7555296e43af71f1e31596269662c1ceb93c9b158a2a9af6e872892b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.5.45` - linux; amd64

```console
$ docker pull clickhouse@sha256:d98e0406d2e33873aa6528b714c4d19cf55bf2512d200404ec944e6991d7b11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253596378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406bcbbb409379f93813cfb93e4e7b3eedf79bc4b22e995cd1a600fe8dabfd9a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:01 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:01 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:01 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:01 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:01 GMT
ARG VERSION=26.2.5.45
# Fri, 27 Mar 2026 17:59:01 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:39 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db352a89196559645a31564305abc482406fff1b4acf9c9dd0e61b87d5bd1221`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 7.6 MB (7598264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38da43cbd46ec1ed46ecf7d35d16c3f886e5c1ca7c49330977fe98c80a5b5b54`  
		Last Modified: Fri, 27 Mar 2026 18:00:17 GMT  
		Size: 215.6 MB (215589543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca8922d442f5411dd8f1c5eb90e608a14d61d1c20999364e33831fb2d5b9a1`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d72789abcbc6e4a70a5e04b67f17e3f357abe9423a5589efb632e7fee24f564`  
		Last Modified: Fri, 27 Mar 2026 18:00:10 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa437ed0d38fb3fd3a7988c64b41b3de7445bde6b7f02a37a3213b657d77d50e`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df7ec7d8671e1f6429085753abe654a97e6ae95a44b1c857a28f7f12ea52bf4`  
		Last Modified: Fri, 27 Mar 2026 18:00:10 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e385387b6b29f2d90d62056f635092668524d5548ad0edeacf7bcc91db8d0a9`  
		Last Modified: Fri, 27 Mar 2026 18:00:11 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.5.45` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1dab19e20fe7f530efbc1ba62fcea1a6c7d3ae6294deb08e1e1010a1aac738b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8553df0a3a8f53eea0ec32e74a5cb28fb5292beba7a6c17ef5c6f3a92f340b12`

```dockerfile
```

-	Layers:
	-	`sha256:344fcbebc6ecd30f99b69cb192fd186127c728ab63fe0358b5223c0248e99cec`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 25.4 KB (25417 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.5.45` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ad60b00e0043303f5f86ab8072c200fd0796e71a360a616be0161b3dc2fb6168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237198556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9bc4c7144dfc471ac54c3d54e7fb3bb2c779555782d2240711e3ebad16c42f9`
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
# Fri, 27 Mar 2026 17:56:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:56:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:56:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:56:31 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:56:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:56:31 GMT
ARG VERSION=26.2.5.45
# Fri, 27 Mar 2026 17:56:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:57:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:57:35 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:57:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:57:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:57:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:57:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42907f324322db4092a6e1759337b7c155f124654b86e3db9c9145c8b513fb73`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 7.6 MB (7577344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6211d7ec1ef1854a49843ce280f379d49d63bdd72f738dac0f480b2b59a89c1`  
		Last Modified: Fri, 27 Mar 2026 17:58:01 GMT  
		Size: 201.4 MB (201362135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea22498ec33d677a20ac8084113c5b3e9408b41ef92e0bb91da96cbfff24ff3c`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd99754186a9a893e32e3d3dea41037ac83125adbc74089272c9c724aabf736`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7f9e9e56af1c86f1d65bd5a6173845ca30f8b04af9f747c0f90eb24b992e23`  
		Last Modified: Fri, 27 Mar 2026 17:57:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03a4888a87e8053432a380eceb2965d56c7992f1604abdd190e3eca1275b72d`  
		Last Modified: Fri, 27 Mar 2026 17:57:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7fc1e0ff56024ba35e5252681ae4e86e799a24bd14db482565a30d72929ad4`  
		Last Modified: Fri, 27 Mar 2026 17:57:59 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.5.45` - unknown; unknown

```console
$ docker pull clickhouse@sha256:14f8da7f51451ef062cda65ee1fc220d3ee21d3c3bf25ec7ed55db6c146c1538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5b93c526f3e88afa84640bd1eae8d7807fe4ba73ceb03dd23cc871ec85e176`

```dockerfile
```

-	Layers:
	-	`sha256:2c7652a332c1dbb39d63ee5d1899520818de246a1b958d81bfc330c1e59dd1f1`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.5.45-jammy`

```console
$ docker pull clickhouse@sha256:cd3c22da7555296e43af71f1e31596269662c1ceb93c9b158a2a9af6e872892b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.5.45-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:d98e0406d2e33873aa6528b714c4d19cf55bf2512d200404ec944e6991d7b11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.6 MB (253596378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:406bcbbb409379f93813cfb93e4e7b3eedf79bc4b22e995cd1a600fe8dabfd9a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:59:01 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:59:01 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:59:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:59:01 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:59:01 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:59:01 GMT
ARG VERSION=26.2.5.45
# Fri, 27 Mar 2026 17:59:01 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:59:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:59:39 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:59:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:59:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:59:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:59:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:59:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db352a89196559645a31564305abc482406fff1b4acf9c9dd0e61b87d5bd1221`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 7.6 MB (7598264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38da43cbd46ec1ed46ecf7d35d16c3f886e5c1ca7c49330977fe98c80a5b5b54`  
		Last Modified: Fri, 27 Mar 2026 18:00:17 GMT  
		Size: 215.6 MB (215589543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ca8922d442f5411dd8f1c5eb90e608a14d61d1c20999364e33831fb2d5b9a1`  
		Last Modified: Fri, 27 Mar 2026 18:00:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d72789abcbc6e4a70a5e04b67f17e3f357abe9423a5589efb632e7fee24f564`  
		Last Modified: Fri, 27 Mar 2026 18:00:10 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa437ed0d38fb3fd3a7988c64b41b3de7445bde6b7f02a37a3213b657d77d50e`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df7ec7d8671e1f6429085753abe654a97e6ae95a44b1c857a28f7f12ea52bf4`  
		Last Modified: Fri, 27 Mar 2026 18:00:10 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e385387b6b29f2d90d62056f635092668524d5548ad0edeacf7bcc91db8d0a9`  
		Last Modified: Fri, 27 Mar 2026 18:00:11 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.5.45-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1dab19e20fe7f530efbc1ba62fcea1a6c7d3ae6294deb08e1e1010a1aac738b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8553df0a3a8f53eea0ec32e74a5cb28fb5292beba7a6c17ef5c6f3a92f340b12`

```dockerfile
```

-	Layers:
	-	`sha256:344fcbebc6ecd30f99b69cb192fd186127c728ab63fe0358b5223c0248e99cec`  
		Last Modified: Fri, 27 Mar 2026 18:00:06 GMT  
		Size: 25.4 KB (25417 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.5.45-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ad60b00e0043303f5f86ab8072c200fd0796e71a360a616be0161b3dc2fb6168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237198556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9bc4c7144dfc471ac54c3d54e7fb3bb2c779555782d2240711e3ebad16c42f9`
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
# Fri, 27 Mar 2026 17:56:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:56:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:56:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:56:31 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:56:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:56:31 GMT
ARG VERSION=26.2.5.45
# Fri, 27 Mar 2026 17:56:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:57:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:57:35 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:57:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.5.45 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:57:35 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:57:35 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:57:35 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:57:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42907f324322db4092a6e1759337b7c155f124654b86e3db9c9145c8b513fb73`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 7.6 MB (7577344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6211d7ec1ef1854a49843ce280f379d49d63bdd72f738dac0f480b2b59a89c1`  
		Last Modified: Fri, 27 Mar 2026 17:58:01 GMT  
		Size: 201.4 MB (201362135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea22498ec33d677a20ac8084113c5b3e9408b41ef92e0bb91da96cbfff24ff3c`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd99754186a9a893e32e3d3dea41037ac83125adbc74089272c9c724aabf736`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7f9e9e56af1c86f1d65bd5a6173845ca30f8b04af9f747c0f90eb24b992e23`  
		Last Modified: Fri, 27 Mar 2026 17:57:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03a4888a87e8053432a380eceb2965d56c7992f1604abdd190e3eca1275b72d`  
		Last Modified: Fri, 27 Mar 2026 17:57:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7fc1e0ff56024ba35e5252681ae4e86e799a24bd14db482565a30d72929ad4`  
		Last Modified: Fri, 27 Mar 2026 17:57:59 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.5.45-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:14f8da7f51451ef062cda65ee1fc220d3ee21d3c3bf25ec7ed55db6c146c1538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5b93c526f3e88afa84640bd1eae8d7807fe4ba73ceb03dd23cc871ec85e176`

```dockerfile
```

-	Layers:
	-	`sha256:2c7652a332c1dbb39d63ee5d1899520818de246a1b958d81bfc330c1e59dd1f1`  
		Last Modified: Fri, 27 Mar 2026 17:57:57 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3`

```console
$ docker pull clickhouse@sha256:7209d66ea16d16bc5d8d8c0a2a5b712e033c7e54ec362cc0e26dfbb4e1ce6b8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:8409fcc9907e4f3cd0795b93082d55698ada60016ac1d220efe92d6a49fa74cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262030105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f48d17d24002e2eabca736b57109b9ce6b627d3b0ccbf86f0ff6a08bd7c5df4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:58:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:58:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:58:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:58:25 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:58:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:54 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:55 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d29f5937d84999d6195496245f17e938228a9af026c18a41969460b1b4b29b`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 7.6 MB (7598282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac104939c93adbb5228f6bae54f43893b22d848054f4e9962cf34c0a3edf59`  
		Last Modified: Fri, 27 Mar 2026 17:59:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea22d985d102971c1bedbbf5ada05f171a2f9b3e6ef44e77ed14e55eed1725c7`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70823c1afc0ba2f0b238951412871ed6f3c8dde7e897364fa2870fef1e970377`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35450c5c524342b0eb8d68c1b61fbbefa57f586460a8c59aa3933ae2137d1fa1`  
		Last Modified: Fri, 27 Mar 2026 17:59:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b4377bbb40df44d2d2fccc0cf7b64c9754cbf352a7586ef9b83b9bd0d35ea4`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ec1feddf9084d1a4b55e8a04195232a4102c3436ad4b0a702ffa9d97dbdb5f`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b9b0ba74ca5ebacd9669e574e6777fa3da705009fe4700b4adaa87b95fa555a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbcd44178df178df8ca56fcc4d01d8c7cda2e362a3402873c036f1984c361e5`

```dockerfile
```

-	Layers:
	-	`sha256:5d918106d6b675c284342874c3aa752ac9dedddd9a3e24b8c3102a46d1c0d616`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9e68a86d90bd79882ee5a9b2bf968914a6c79e231276ec39921138bebb3a4d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244246448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353daa05b8234663d1dc5e1f7864b15bffe63eee1f5e1e421e7e3ebb13c3e668`
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
# Fri, 27 Mar 2026 17:57:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:56 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:57:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:27 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:28 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c85276d4b19814f6f44a62487af9f88b051491e4163a08a52cb92a69fa29174`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 7.6 MB (7577376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d7526c1c842a1243f1044e67e28bdf45261a25931e0e136ef46627aca1c27c`  
		Last Modified: Fri, 27 Mar 2026 17:58:54 GMT  
		Size: 208.4 MB (208409989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88ba8f294ac9c0011c731abc03cbf629e119fa92beb890c25d816844387b1b6`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e883cf213509478e015ce4aa0ff9424c09be57076a594e864343e44f3680d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563be8fd3280cca027c0e1e93e4a924f6ace9be38d1554a41c381e965bdb25d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed1e2cc11fdf96325b3b89a6b4ffbe27fd46ad7f6c5087cbed8e04e8556d9b8`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b20c00eafedfd1c3d9bf6154cf13c4751b412355c218cbf60101f1a5a8b932f`  
		Last Modified: Fri, 27 Mar 2026 17:58:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d72e62e6c70a4e34df7446879716a7729a615eb704e5257aa32fcf6ab5d66341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcb9085196b45eaebd3bf71895096ba1724c0e4f4335bdb6f8d02ea411c22a6`

```dockerfile
```

-	Layers:
	-	`sha256:ad4a9b0386c977b1378aef99cdb337e47453ca849feb6666442c79a8e4b34939`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 26.9 KB (26886 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3-jammy`

```console
$ docker pull clickhouse@sha256:7209d66ea16d16bc5d8d8c0a2a5b712e033c7e54ec362cc0e26dfbb4e1ce6b8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8409fcc9907e4f3cd0795b93082d55698ada60016ac1d220efe92d6a49fa74cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262030105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f48d17d24002e2eabca736b57109b9ce6b627d3b0ccbf86f0ff6a08bd7c5df4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:58:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:58:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:58:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:58:25 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:58:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:54 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:55 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d29f5937d84999d6195496245f17e938228a9af026c18a41969460b1b4b29b`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 7.6 MB (7598282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac104939c93adbb5228f6bae54f43893b22d848054f4e9962cf34c0a3edf59`  
		Last Modified: Fri, 27 Mar 2026 17:59:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea22d985d102971c1bedbbf5ada05f171a2f9b3e6ef44e77ed14e55eed1725c7`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70823c1afc0ba2f0b238951412871ed6f3c8dde7e897364fa2870fef1e970377`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35450c5c524342b0eb8d68c1b61fbbefa57f586460a8c59aa3933ae2137d1fa1`  
		Last Modified: Fri, 27 Mar 2026 17:59:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b4377bbb40df44d2d2fccc0cf7b64c9754cbf352a7586ef9b83b9bd0d35ea4`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ec1feddf9084d1a4b55e8a04195232a4102c3436ad4b0a702ffa9d97dbdb5f`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b9b0ba74ca5ebacd9669e574e6777fa3da705009fe4700b4adaa87b95fa555a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbcd44178df178df8ca56fcc4d01d8c7cda2e362a3402873c036f1984c361e5`

```dockerfile
```

-	Layers:
	-	`sha256:5d918106d6b675c284342874c3aa752ac9dedddd9a3e24b8c3102a46d1c0d616`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9e68a86d90bd79882ee5a9b2bf968914a6c79e231276ec39921138bebb3a4d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244246448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353daa05b8234663d1dc5e1f7864b15bffe63eee1f5e1e421e7e3ebb13c3e668`
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
# Fri, 27 Mar 2026 17:57:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:56 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:57:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:27 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:28 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c85276d4b19814f6f44a62487af9f88b051491e4163a08a52cb92a69fa29174`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 7.6 MB (7577376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d7526c1c842a1243f1044e67e28bdf45261a25931e0e136ef46627aca1c27c`  
		Last Modified: Fri, 27 Mar 2026 17:58:54 GMT  
		Size: 208.4 MB (208409989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88ba8f294ac9c0011c731abc03cbf629e119fa92beb890c25d816844387b1b6`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e883cf213509478e015ce4aa0ff9424c09be57076a594e864343e44f3680d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563be8fd3280cca027c0e1e93e4a924f6ace9be38d1554a41c381e965bdb25d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed1e2cc11fdf96325b3b89a6b4ffbe27fd46ad7f6c5087cbed8e04e8556d9b8`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b20c00eafedfd1c3d9bf6154cf13c4751b412355c218cbf60101f1a5a8b932f`  
		Last Modified: Fri, 27 Mar 2026 17:58:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d72e62e6c70a4e34df7446879716a7729a615eb704e5257aa32fcf6ab5d66341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcb9085196b45eaebd3bf71895096ba1724c0e4f4335bdb6f8d02ea411c22a6`

```dockerfile
```

-	Layers:
	-	`sha256:ad4a9b0386c977b1378aef99cdb337e47453ca849feb6666442c79a8e4b34939`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 26.9 KB (26886 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.1`

```console
$ docker pull clickhouse@sha256:7209d66ea16d16bc5d8d8c0a2a5b712e033c7e54ec362cc0e26dfbb4e1ce6b8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:8409fcc9907e4f3cd0795b93082d55698ada60016ac1d220efe92d6a49fa74cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262030105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f48d17d24002e2eabca736b57109b9ce6b627d3b0ccbf86f0ff6a08bd7c5df4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:58:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:58:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:58:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:58:25 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:58:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:54 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:55 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d29f5937d84999d6195496245f17e938228a9af026c18a41969460b1b4b29b`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 7.6 MB (7598282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac104939c93adbb5228f6bae54f43893b22d848054f4e9962cf34c0a3edf59`  
		Last Modified: Fri, 27 Mar 2026 17:59:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea22d985d102971c1bedbbf5ada05f171a2f9b3e6ef44e77ed14e55eed1725c7`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70823c1afc0ba2f0b238951412871ed6f3c8dde7e897364fa2870fef1e970377`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35450c5c524342b0eb8d68c1b61fbbefa57f586460a8c59aa3933ae2137d1fa1`  
		Last Modified: Fri, 27 Mar 2026 17:59:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b4377bbb40df44d2d2fccc0cf7b64c9754cbf352a7586ef9b83b9bd0d35ea4`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ec1feddf9084d1a4b55e8a04195232a4102c3436ad4b0a702ffa9d97dbdb5f`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b9b0ba74ca5ebacd9669e574e6777fa3da705009fe4700b4adaa87b95fa555a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbcd44178df178df8ca56fcc4d01d8c7cda2e362a3402873c036f1984c361e5`

```dockerfile
```

-	Layers:
	-	`sha256:5d918106d6b675c284342874c3aa752ac9dedddd9a3e24b8c3102a46d1c0d616`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9e68a86d90bd79882ee5a9b2bf968914a6c79e231276ec39921138bebb3a4d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244246448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353daa05b8234663d1dc5e1f7864b15bffe63eee1f5e1e421e7e3ebb13c3e668`
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
# Fri, 27 Mar 2026 17:57:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:56 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:57:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:27 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:28 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c85276d4b19814f6f44a62487af9f88b051491e4163a08a52cb92a69fa29174`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 7.6 MB (7577376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d7526c1c842a1243f1044e67e28bdf45261a25931e0e136ef46627aca1c27c`  
		Last Modified: Fri, 27 Mar 2026 17:58:54 GMT  
		Size: 208.4 MB (208409989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88ba8f294ac9c0011c731abc03cbf629e119fa92beb890c25d816844387b1b6`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e883cf213509478e015ce4aa0ff9424c09be57076a594e864343e44f3680d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563be8fd3280cca027c0e1e93e4a924f6ace9be38d1554a41c381e965bdb25d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed1e2cc11fdf96325b3b89a6b4ffbe27fd46ad7f6c5087cbed8e04e8556d9b8`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b20c00eafedfd1c3d9bf6154cf13c4751b412355c218cbf60101f1a5a8b932f`  
		Last Modified: Fri, 27 Mar 2026 17:58:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d72e62e6c70a4e34df7446879716a7729a615eb704e5257aa32fcf6ab5d66341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcb9085196b45eaebd3bf71895096ba1724c0e4f4335bdb6f8d02ea411c22a6`

```dockerfile
```

-	Layers:
	-	`sha256:ad4a9b0386c977b1378aef99cdb337e47453ca849feb6666442c79a8e4b34939`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 26.9 KB (26886 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.1-jammy`

```console
$ docker pull clickhouse@sha256:7209d66ea16d16bc5d8d8c0a2a5b712e033c7e54ec362cc0e26dfbb4e1ce6b8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8409fcc9907e4f3cd0795b93082d55698ada60016ac1d220efe92d6a49fa74cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262030105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f48d17d24002e2eabca736b57109b9ce6b627d3b0ccbf86f0ff6a08bd7c5df4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:58:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:58:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:58:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:58:25 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:58:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:54 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:55 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d29f5937d84999d6195496245f17e938228a9af026c18a41969460b1b4b29b`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 7.6 MB (7598282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac104939c93adbb5228f6bae54f43893b22d848054f4e9962cf34c0a3edf59`  
		Last Modified: Fri, 27 Mar 2026 17:59:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea22d985d102971c1bedbbf5ada05f171a2f9b3e6ef44e77ed14e55eed1725c7`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70823c1afc0ba2f0b238951412871ed6f3c8dde7e897364fa2870fef1e970377`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35450c5c524342b0eb8d68c1b61fbbefa57f586460a8c59aa3933ae2137d1fa1`  
		Last Modified: Fri, 27 Mar 2026 17:59:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b4377bbb40df44d2d2fccc0cf7b64c9754cbf352a7586ef9b83b9bd0d35ea4`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ec1feddf9084d1a4b55e8a04195232a4102c3436ad4b0a702ffa9d97dbdb5f`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b9b0ba74ca5ebacd9669e574e6777fa3da705009fe4700b4adaa87b95fa555a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbcd44178df178df8ca56fcc4d01d8c7cda2e362a3402873c036f1984c361e5`

```dockerfile
```

-	Layers:
	-	`sha256:5d918106d6b675c284342874c3aa752ac9dedddd9a3e24b8c3102a46d1c0d616`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9e68a86d90bd79882ee5a9b2bf968914a6c79e231276ec39921138bebb3a4d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244246448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353daa05b8234663d1dc5e1f7864b15bffe63eee1f5e1e421e7e3ebb13c3e668`
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
# Fri, 27 Mar 2026 17:57:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:56 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:57:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:27 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:28 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c85276d4b19814f6f44a62487af9f88b051491e4163a08a52cb92a69fa29174`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 7.6 MB (7577376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d7526c1c842a1243f1044e67e28bdf45261a25931e0e136ef46627aca1c27c`  
		Last Modified: Fri, 27 Mar 2026 17:58:54 GMT  
		Size: 208.4 MB (208409989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88ba8f294ac9c0011c731abc03cbf629e119fa92beb890c25d816844387b1b6`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e883cf213509478e015ce4aa0ff9424c09be57076a594e864343e44f3680d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563be8fd3280cca027c0e1e93e4a924f6ace9be38d1554a41c381e965bdb25d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed1e2cc11fdf96325b3b89a6b4ffbe27fd46ad7f6c5087cbed8e04e8556d9b8`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b20c00eafedfd1c3d9bf6154cf13c4751b412355c218cbf60101f1a5a8b932f`  
		Last Modified: Fri, 27 Mar 2026 17:58:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d72e62e6c70a4e34df7446879716a7729a615eb704e5257aa32fcf6ab5d66341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcb9085196b45eaebd3bf71895096ba1724c0e4f4335bdb6f8d02ea411c22a6`

```dockerfile
```

-	Layers:
	-	`sha256:ad4a9b0386c977b1378aef99cdb337e47453ca849feb6666442c79a8e4b34939`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 26.9 KB (26886 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.1.896`

```console
$ docker pull clickhouse@sha256:7209d66ea16d16bc5d8d8c0a2a5b712e033c7e54ec362cc0e26dfbb4e1ce6b8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.1.896` - linux; amd64

```console
$ docker pull clickhouse@sha256:8409fcc9907e4f3cd0795b93082d55698ada60016ac1d220efe92d6a49fa74cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262030105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f48d17d24002e2eabca736b57109b9ce6b627d3b0ccbf86f0ff6a08bd7c5df4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:58:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:58:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:58:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:58:25 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:58:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:54 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:55 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d29f5937d84999d6195496245f17e938228a9af026c18a41969460b1b4b29b`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 7.6 MB (7598282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac104939c93adbb5228f6bae54f43893b22d848054f4e9962cf34c0a3edf59`  
		Last Modified: Fri, 27 Mar 2026 17:59:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea22d985d102971c1bedbbf5ada05f171a2f9b3e6ef44e77ed14e55eed1725c7`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70823c1afc0ba2f0b238951412871ed6f3c8dde7e897364fa2870fef1e970377`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35450c5c524342b0eb8d68c1b61fbbefa57f586460a8c59aa3933ae2137d1fa1`  
		Last Modified: Fri, 27 Mar 2026 17:59:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b4377bbb40df44d2d2fccc0cf7b64c9754cbf352a7586ef9b83b9bd0d35ea4`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ec1feddf9084d1a4b55e8a04195232a4102c3436ad4b0a702ffa9d97dbdb5f`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.1.896` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b9b0ba74ca5ebacd9669e574e6777fa3da705009fe4700b4adaa87b95fa555a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbcd44178df178df8ca56fcc4d01d8c7cda2e362a3402873c036f1984c361e5`

```dockerfile
```

-	Layers:
	-	`sha256:5d918106d6b675c284342874c3aa752ac9dedddd9a3e24b8c3102a46d1c0d616`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.1.896` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9e68a86d90bd79882ee5a9b2bf968914a6c79e231276ec39921138bebb3a4d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244246448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353daa05b8234663d1dc5e1f7864b15bffe63eee1f5e1e421e7e3ebb13c3e668`
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
# Fri, 27 Mar 2026 17:57:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:56 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:57:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:27 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:28 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c85276d4b19814f6f44a62487af9f88b051491e4163a08a52cb92a69fa29174`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 7.6 MB (7577376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d7526c1c842a1243f1044e67e28bdf45261a25931e0e136ef46627aca1c27c`  
		Last Modified: Fri, 27 Mar 2026 17:58:54 GMT  
		Size: 208.4 MB (208409989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88ba8f294ac9c0011c731abc03cbf629e119fa92beb890c25d816844387b1b6`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e883cf213509478e015ce4aa0ff9424c09be57076a594e864343e44f3680d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563be8fd3280cca027c0e1e93e4a924f6ace9be38d1554a41c381e965bdb25d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed1e2cc11fdf96325b3b89a6b4ffbe27fd46ad7f6c5087cbed8e04e8556d9b8`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b20c00eafedfd1c3d9bf6154cf13c4751b412355c218cbf60101f1a5a8b932f`  
		Last Modified: Fri, 27 Mar 2026 17:58:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.1.896` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d72e62e6c70a4e34df7446879716a7729a615eb704e5257aa32fcf6ab5d66341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcb9085196b45eaebd3bf71895096ba1724c0e4f4335bdb6f8d02ea411c22a6`

```dockerfile
```

-	Layers:
	-	`sha256:ad4a9b0386c977b1378aef99cdb337e47453ca849feb6666442c79a8e4b34939`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 26.9 KB (26886 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.1.896-jammy`

```console
$ docker pull clickhouse@sha256:7209d66ea16d16bc5d8d8c0a2a5b712e033c7e54ec362cc0e26dfbb4e1ce6b8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.1.896-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8409fcc9907e4f3cd0795b93082d55698ada60016ac1d220efe92d6a49fa74cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262030105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f48d17d24002e2eabca736b57109b9ce6b627d3b0ccbf86f0ff6a08bd7c5df4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:58:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:58:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:58:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:58:25 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:58:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:54 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:55 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d29f5937d84999d6195496245f17e938228a9af026c18a41969460b1b4b29b`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 7.6 MB (7598282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac104939c93adbb5228f6bae54f43893b22d848054f4e9962cf34c0a3edf59`  
		Last Modified: Fri, 27 Mar 2026 17:59:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea22d985d102971c1bedbbf5ada05f171a2f9b3e6ef44e77ed14e55eed1725c7`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70823c1afc0ba2f0b238951412871ed6f3c8dde7e897364fa2870fef1e970377`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35450c5c524342b0eb8d68c1b61fbbefa57f586460a8c59aa3933ae2137d1fa1`  
		Last Modified: Fri, 27 Mar 2026 17:59:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b4377bbb40df44d2d2fccc0cf7b64c9754cbf352a7586ef9b83b9bd0d35ea4`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ec1feddf9084d1a4b55e8a04195232a4102c3436ad4b0a702ffa9d97dbdb5f`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.1.896-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b9b0ba74ca5ebacd9669e574e6777fa3da705009fe4700b4adaa87b95fa555a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbcd44178df178df8ca56fcc4d01d8c7cda2e362a3402873c036f1984c361e5`

```dockerfile
```

-	Layers:
	-	`sha256:5d918106d6b675c284342874c3aa752ac9dedddd9a3e24b8c3102a46d1c0d616`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.1.896-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9e68a86d90bd79882ee5a9b2bf968914a6c79e231276ec39921138bebb3a4d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244246448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353daa05b8234663d1dc5e1f7864b15bffe63eee1f5e1e421e7e3ebb13c3e668`
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
# Fri, 27 Mar 2026 17:57:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:56 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:57:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:27 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:28 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c85276d4b19814f6f44a62487af9f88b051491e4163a08a52cb92a69fa29174`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 7.6 MB (7577376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d7526c1c842a1243f1044e67e28bdf45261a25931e0e136ef46627aca1c27c`  
		Last Modified: Fri, 27 Mar 2026 17:58:54 GMT  
		Size: 208.4 MB (208409989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88ba8f294ac9c0011c731abc03cbf629e119fa92beb890c25d816844387b1b6`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e883cf213509478e015ce4aa0ff9424c09be57076a594e864343e44f3680d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563be8fd3280cca027c0e1e93e4a924f6ace9be38d1554a41c381e965bdb25d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed1e2cc11fdf96325b3b89a6b4ffbe27fd46ad7f6c5087cbed8e04e8556d9b8`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b20c00eafedfd1c3d9bf6154cf13c4751b412355c218cbf60101f1a5a8b932f`  
		Last Modified: Fri, 27 Mar 2026 17:58:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.1.896-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d72e62e6c70a4e34df7446879716a7729a615eb704e5257aa32fcf6ab5d66341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcb9085196b45eaebd3bf71895096ba1724c0e4f4335bdb6f8d02ea411c22a6`

```dockerfile
```

-	Layers:
	-	`sha256:ad4a9b0386c977b1378aef99cdb337e47453ca849feb6666442c79a8e4b34939`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 26.9 KB (26886 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:7209d66ea16d16bc5d8d8c0a2a5b712e033c7e54ec362cc0e26dfbb4e1ce6b8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8409fcc9907e4f3cd0795b93082d55698ada60016ac1d220efe92d6a49fa74cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262030105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f48d17d24002e2eabca736b57109b9ce6b627d3b0ccbf86f0ff6a08bd7c5df4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:58:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:58:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:58:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:58:25 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:58:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:54 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:55 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d29f5937d84999d6195496245f17e938228a9af026c18a41969460b1b4b29b`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 7.6 MB (7598282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac104939c93adbb5228f6bae54f43893b22d848054f4e9962cf34c0a3edf59`  
		Last Modified: Fri, 27 Mar 2026 17:59:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea22d985d102971c1bedbbf5ada05f171a2f9b3e6ef44e77ed14e55eed1725c7`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70823c1afc0ba2f0b238951412871ed6f3c8dde7e897364fa2870fef1e970377`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35450c5c524342b0eb8d68c1b61fbbefa57f586460a8c59aa3933ae2137d1fa1`  
		Last Modified: Fri, 27 Mar 2026 17:59:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b4377bbb40df44d2d2fccc0cf7b64c9754cbf352a7586ef9b83b9bd0d35ea4`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ec1feddf9084d1a4b55e8a04195232a4102c3436ad4b0a702ffa9d97dbdb5f`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b9b0ba74ca5ebacd9669e574e6777fa3da705009fe4700b4adaa87b95fa555a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbcd44178df178df8ca56fcc4d01d8c7cda2e362a3402873c036f1984c361e5`

```dockerfile
```

-	Layers:
	-	`sha256:5d918106d6b675c284342874c3aa752ac9dedddd9a3e24b8c3102a46d1c0d616`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9e68a86d90bd79882ee5a9b2bf968914a6c79e231276ec39921138bebb3a4d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244246448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353daa05b8234663d1dc5e1f7864b15bffe63eee1f5e1e421e7e3ebb13c3e668`
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
# Fri, 27 Mar 2026 17:57:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:56 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:57:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:27 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:28 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c85276d4b19814f6f44a62487af9f88b051491e4163a08a52cb92a69fa29174`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 7.6 MB (7577376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d7526c1c842a1243f1044e67e28bdf45261a25931e0e136ef46627aca1c27c`  
		Last Modified: Fri, 27 Mar 2026 17:58:54 GMT  
		Size: 208.4 MB (208409989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88ba8f294ac9c0011c731abc03cbf629e119fa92beb890c25d816844387b1b6`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e883cf213509478e015ce4aa0ff9424c09be57076a594e864343e44f3680d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563be8fd3280cca027c0e1e93e4a924f6ace9be38d1554a41c381e965bdb25d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed1e2cc11fdf96325b3b89a6b4ffbe27fd46ad7f6c5087cbed8e04e8556d9b8`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b20c00eafedfd1c3d9bf6154cf13c4751b412355c218cbf60101f1a5a8b932f`  
		Last Modified: Fri, 27 Mar 2026 17:58:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d72e62e6c70a4e34df7446879716a7729a615eb704e5257aa32fcf6ab5d66341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcb9085196b45eaebd3bf71895096ba1724c0e4f4335bdb6f8d02ea411c22a6`

```dockerfile
```

-	Layers:
	-	`sha256:ad4a9b0386c977b1378aef99cdb337e47453ca849feb6666442c79a8e4b34939`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 26.9 KB (26886 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:7209d66ea16d16bc5d8d8c0a2a5b712e033c7e54ec362cc0e26dfbb4e1ce6b8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:8409fcc9907e4f3cd0795b93082d55698ada60016ac1d220efe92d6a49fa74cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262030105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f48d17d24002e2eabca736b57109b9ce6b627d3b0ccbf86f0ff6a08bd7c5df4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:58:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:58:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:58:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:58:25 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:58:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:54 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:55 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d29f5937d84999d6195496245f17e938228a9af026c18a41969460b1b4b29b`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 7.6 MB (7598282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac104939c93adbb5228f6bae54f43893b22d848054f4e9962cf34c0a3edf59`  
		Last Modified: Fri, 27 Mar 2026 17:59:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea22d985d102971c1bedbbf5ada05f171a2f9b3e6ef44e77ed14e55eed1725c7`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70823c1afc0ba2f0b238951412871ed6f3c8dde7e897364fa2870fef1e970377`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35450c5c524342b0eb8d68c1b61fbbefa57f586460a8c59aa3933ae2137d1fa1`  
		Last Modified: Fri, 27 Mar 2026 17:59:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b4377bbb40df44d2d2fccc0cf7b64c9754cbf352a7586ef9b83b9bd0d35ea4`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ec1feddf9084d1a4b55e8a04195232a4102c3436ad4b0a702ffa9d97dbdb5f`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b9b0ba74ca5ebacd9669e574e6777fa3da705009fe4700b4adaa87b95fa555a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbcd44178df178df8ca56fcc4d01d8c7cda2e362a3402873c036f1984c361e5`

```dockerfile
```

-	Layers:
	-	`sha256:5d918106d6b675c284342874c3aa752ac9dedddd9a3e24b8c3102a46d1c0d616`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9e68a86d90bd79882ee5a9b2bf968914a6c79e231276ec39921138bebb3a4d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244246448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353daa05b8234663d1dc5e1f7864b15bffe63eee1f5e1e421e7e3ebb13c3e668`
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
# Fri, 27 Mar 2026 17:57:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:56 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:57:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:27 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:28 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c85276d4b19814f6f44a62487af9f88b051491e4163a08a52cb92a69fa29174`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 7.6 MB (7577376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d7526c1c842a1243f1044e67e28bdf45261a25931e0e136ef46627aca1c27c`  
		Last Modified: Fri, 27 Mar 2026 17:58:54 GMT  
		Size: 208.4 MB (208409989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88ba8f294ac9c0011c731abc03cbf629e119fa92beb890c25d816844387b1b6`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e883cf213509478e015ce4aa0ff9424c09be57076a594e864343e44f3680d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563be8fd3280cca027c0e1e93e4a924f6ace9be38d1554a41c381e965bdb25d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed1e2cc11fdf96325b3b89a6b4ffbe27fd46ad7f6c5087cbed8e04e8556d9b8`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b20c00eafedfd1c3d9bf6154cf13c4751b412355c218cbf60101f1a5a8b932f`  
		Last Modified: Fri, 27 Mar 2026 17:58:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d72e62e6c70a4e34df7446879716a7729a615eb704e5257aa32fcf6ab5d66341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcb9085196b45eaebd3bf71895096ba1724c0e4f4335bdb6f8d02ea411c22a6`

```dockerfile
```

-	Layers:
	-	`sha256:ad4a9b0386c977b1378aef99cdb337e47453ca849feb6666442c79a8e4b34939`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 26.9 KB (26886 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:7209d66ea16d16bc5d8d8c0a2a5b712e033c7e54ec362cc0e26dfbb4e1ce6b8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:8409fcc9907e4f3cd0795b93082d55698ada60016ac1d220efe92d6a49fa74cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262030105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f48d17d24002e2eabca736b57109b9ce6b627d3b0ccbf86f0ff6a08bd7c5df4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:58:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:58:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:58:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:58:25 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:58:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:54 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:55 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d29f5937d84999d6195496245f17e938228a9af026c18a41969460b1b4b29b`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 7.6 MB (7598282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac104939c93adbb5228f6bae54f43893b22d848054f4e9962cf34c0a3edf59`  
		Last Modified: Fri, 27 Mar 2026 17:59:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea22d985d102971c1bedbbf5ada05f171a2f9b3e6ef44e77ed14e55eed1725c7`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70823c1afc0ba2f0b238951412871ed6f3c8dde7e897364fa2870fef1e970377`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35450c5c524342b0eb8d68c1b61fbbefa57f586460a8c59aa3933ae2137d1fa1`  
		Last Modified: Fri, 27 Mar 2026 17:59:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b4377bbb40df44d2d2fccc0cf7b64c9754cbf352a7586ef9b83b9bd0d35ea4`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ec1feddf9084d1a4b55e8a04195232a4102c3436ad4b0a702ffa9d97dbdb5f`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b9b0ba74ca5ebacd9669e574e6777fa3da705009fe4700b4adaa87b95fa555a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbcd44178df178df8ca56fcc4d01d8c7cda2e362a3402873c036f1984c361e5`

```dockerfile
```

-	Layers:
	-	`sha256:5d918106d6b675c284342874c3aa752ac9dedddd9a3e24b8c3102a46d1c0d616`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9e68a86d90bd79882ee5a9b2bf968914a6c79e231276ec39921138bebb3a4d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244246448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353daa05b8234663d1dc5e1f7864b15bffe63eee1f5e1e421e7e3ebb13c3e668`
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
# Fri, 27 Mar 2026 17:57:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:56 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:57:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:27 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:28 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c85276d4b19814f6f44a62487af9f88b051491e4163a08a52cb92a69fa29174`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 7.6 MB (7577376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d7526c1c842a1243f1044e67e28bdf45261a25931e0e136ef46627aca1c27c`  
		Last Modified: Fri, 27 Mar 2026 17:58:54 GMT  
		Size: 208.4 MB (208409989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88ba8f294ac9c0011c731abc03cbf629e119fa92beb890c25d816844387b1b6`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e883cf213509478e015ce4aa0ff9424c09be57076a594e864343e44f3680d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563be8fd3280cca027c0e1e93e4a924f6ace9be38d1554a41c381e965bdb25d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed1e2cc11fdf96325b3b89a6b4ffbe27fd46ad7f6c5087cbed8e04e8556d9b8`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b20c00eafedfd1c3d9bf6154cf13c4751b412355c218cbf60101f1a5a8b932f`  
		Last Modified: Fri, 27 Mar 2026 17:58:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d72e62e6c70a4e34df7446879716a7729a615eb704e5257aa32fcf6ab5d66341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcb9085196b45eaebd3bf71895096ba1724c0e4f4335bdb6f8d02ea411c22a6`

```dockerfile
```

-	Layers:
	-	`sha256:ad4a9b0386c977b1378aef99cdb337e47453ca849feb6666442c79a8e4b34939`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 26.9 KB (26886 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:7209d66ea16d16bc5d8d8c0a2a5b712e033c7e54ec362cc0e26dfbb4e1ce6b8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8409fcc9907e4f3cd0795b93082d55698ada60016ac1d220efe92d6a49fa74cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.0 MB (262030105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f48d17d24002e2eabca736b57109b9ce6b627d3b0ccbf86f0ff6a08bd7c5df4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Fri, 27 Mar 2026 17:58:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:58:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:58:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:58:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:58:25 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:58:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:54 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:55 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:55 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:55 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d29f5937d84999d6195496245f17e938228a9af026c18a41969460b1b4b29b`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 7.6 MB (7598282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ac104939c93adbb5228f6bae54f43893b22d848054f4e9962cf34c0a3edf59`  
		Last Modified: Fri, 27 Mar 2026 17:59:25 GMT  
		Size: 224.0 MB (224023254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea22d985d102971c1bedbbf5ada05f171a2f9b3e6ef44e77ed14e55eed1725c7`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70823c1afc0ba2f0b238951412871ed6f3c8dde7e897364fa2870fef1e970377`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35450c5c524342b0eb8d68c1b61fbbefa57f586460a8c59aa3933ae2137d1fa1`  
		Last Modified: Fri, 27 Mar 2026 17:59:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91b4377bbb40df44d2d2fccc0cf7b64c9754cbf352a7586ef9b83b9bd0d35ea4`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ec1feddf9084d1a4b55e8a04195232a4102c3436ad4b0a702ffa9d97dbdb5f`  
		Last Modified: Fri, 27 Mar 2026 17:59:22 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b9b0ba74ca5ebacd9669e574e6777fa3da705009fe4700b4adaa87b95fa555a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dbcd44178df178df8ca56fcc4d01d8c7cda2e362a3402873c036f1984c361e5`

```dockerfile
```

-	Layers:
	-	`sha256:5d918106d6b675c284342874c3aa752ac9dedddd9a3e24b8c3102a46d1c0d616`  
		Last Modified: Fri, 27 Mar 2026 17:59:20 GMT  
		Size: 26.7 KB (26651 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9e68a86d90bd79882ee5a9b2bf968914a6c79e231276ec39921138bebb3a4d47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244246448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:353daa05b8234663d1dc5e1f7864b15bffe63eee1f5e1e421e7e3ebb13c3e668`
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
# Fri, 27 Mar 2026 17:57:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Mar 2026 17:57:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Mar 2026 17:57:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Mar 2026 17:57:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Mar 2026 17:57:56 GMT
ARG VERSION=26.3.1.896
# Fri, 27 Mar 2026 17:57:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Mar 2026 17:58:27 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Mar 2026 17:58:27 GMT
ENV TZ=UTC
# Fri, 27 Mar 2026 17:58:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.1.896 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Mar 2026 17:58:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Mar 2026 17:58:28 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Mar 2026 17:58:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Mar 2026 17:58:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:cf67f3f0b7b3a837aac5c0be2974a3574a6b600345d9528def747c7e01fda2b8`  
		Last Modified: Tue, 24 Feb 2026 08:07:51 GMT  
		Size: 27.4 MB (27389025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c85276d4b19814f6f44a62487af9f88b051491e4163a08a52cb92a69fa29174`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 7.6 MB (7577376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d7526c1c842a1243f1044e67e28bdf45261a25931e0e136ef46627aca1c27c`  
		Last Modified: Fri, 27 Mar 2026 17:58:54 GMT  
		Size: 208.4 MB (208409989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88ba8f294ac9c0011c731abc03cbf629e119fa92beb890c25d816844387b1b6`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e883cf213509478e015ce4aa0ff9424c09be57076a594e864343e44f3680d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563be8fd3280cca027c0e1e93e4a924f6ace9be38d1554a41c381e965bdb25d4`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed1e2cc11fdf96325b3b89a6b4ffbe27fd46ad7f6c5087cbed8e04e8556d9b8`  
		Last Modified: Fri, 27 Mar 2026 17:58:51 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b20c00eafedfd1c3d9bf6154cf13c4751b412355c218cbf60101f1a5a8b932f`  
		Last Modified: Fri, 27 Mar 2026 17:58:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d72e62e6c70a4e34df7446879716a7729a615eb704e5257aa32fcf6ab5d66341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcb9085196b45eaebd3bf71895096ba1724c0e4f4335bdb6f8d02ea411c22a6`

```dockerfile
```

-	Layers:
	-	`sha256:ad4a9b0386c977b1378aef99cdb337e47453ca849feb6666442c79a8e4b34939`  
		Last Modified: Fri, 27 Mar 2026 17:58:50 GMT  
		Size: 26.9 KB (26886 bytes)  
		MIME: application/vnd.in-toto+json
