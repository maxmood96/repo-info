<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.4`](#clickhouse2534)
-	[`clickhouse:25.3.4-jammy`](#clickhouse2534-jammy)
-	[`clickhouse:25.3.4.190`](#clickhouse2534190)
-	[`clickhouse:25.3.4.190-jammy`](#clickhouse2534190-jammy)
-	[`clickhouse:25.4`](#clickhouse254)
-	[`clickhouse:25.4-jammy`](#clickhouse254-jammy)
-	[`clickhouse:25.4.7`](#clickhouse2547)
-	[`clickhouse:25.4.7-jammy`](#clickhouse2547-jammy)
-	[`clickhouse:25.4.7.66`](#clickhouse254766)
-	[`clickhouse:25.4.7.66-jammy`](#clickhouse254766-jammy)
-	[`clickhouse:25.5`](#clickhouse255)
-	[`clickhouse:25.5-jammy`](#clickhouse255-jammy)
-	[`clickhouse:25.5.4`](#clickhouse2554)
-	[`clickhouse:25.5.4-jammy`](#clickhouse2554-jammy)
-	[`clickhouse:25.5.4.38`](#clickhouse255438)
-	[`clickhouse:25.5.4.38-jammy`](#clickhouse255438-jammy)
-	[`clickhouse:25.6`](#clickhouse256)
-	[`clickhouse:25.6-jammy`](#clickhouse256-jammy)
-	[`clickhouse:25.6.1`](#clickhouse2561)
-	[`clickhouse:25.6.1-jammy`](#clickhouse2561-jammy)
-	[`clickhouse:25.6.1.3206`](#clickhouse25613206)
-	[`clickhouse:25.6.1.3206-jammy`](#clickhouse25613206-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:309b9238691234e4ebb554afa227c0c6b29f169b4e4ce9a68e621db170f964bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:14cd358b4321c90949bdb82ef783d415b288f9e92e594d986b68c46fd1a08a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204656901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faf232a4b6a79ac8955e52df456718817dbd3f2831f8e4c67ffaa276a98aaff`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a89521c1cddce9e2b92a7eea7e2e26f08d9644f8280c2ffabc687ba59a380`  
		Last Modified: Fri, 27 Jun 2025 21:49:38 GMT  
		Size: 7.2 MB (7151605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f97b7e7c107f81c005662fac120035c32226b53ea2f331be0b7d28153bf19b`  
		Last Modified: Fri, 27 Jun 2025 21:49:45 GMT  
		Size: 167.1 MB (167102045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd9e5194ca4898b9a81e75384174a506b3f40f52f3f9a199e61d0bf85ca90d`  
		Last Modified: Fri, 27 Jun 2025 19:03:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a196f26d3fcac6764f1e0cf39781226cf953be5d0859ae1bb2c0bf49dd8bce9e`  
		Last Modified: Fri, 27 Jun 2025 19:03:06 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5445346ace8b927a19dafce4f348e6c2e7eb73610a91488401afec069b151273`  
		Last Modified: Fri, 27 Jun 2025 19:03:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9903e3e75a91e7f238e84fedac46adf1fd322f6dc7d7e24848bdabcce95235f8`  
		Last Modified: Fri, 27 Jun 2025 19:03:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd49a017f1b4781b5e10d0db53ab4474bf9c9cc6736e3334f0324b86276b5421`  
		Last Modified: Fri, 27 Jun 2025 19:03:13 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9ba832181b9f6be8f5f217385d87d47835fd535412a917f140dc7d836051728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0e364a78dad8826a0d237b11ab93f52cdb6e29db46b4a8fd411e98d9115eae`

```dockerfile
```

-	Layers:
	-	`sha256:e65e118aeb542d30c362f3f00125c47cc357f7b682a949fa6a31c1a81aef9f24`  
		Last Modified: Fri, 27 Jun 2025 21:49:21 GMT  
		Size: 25.9 KB (25886 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:43fc7421731f68ef1f15e7c1cd4bd61b89cdef5b0993fbdbd9df1e7f1daf616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192176647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891f121ead07341bdb77db2b6669a46ac9e41676f06eda3133e8a6abc5549437`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a23662fc50e497af13cba7782f06ab2fa94fbce9a6a450a4599446a17c308`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24538160e575723afc9dba473de81c59b5c7b3bf95ff19c0c089485e11b6462`  
		Last Modified: Fri, 27 Jun 2025 21:49:44 GMT  
		Size: 156.8 MB (156822945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e291bf0ee5766818d7442c70ca06b7b7bf86fba4f0a30e2fe86f93975e05a037`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7c8e256097ad6fc4e0dfce399adae584bda2e2343d1086fb20e60d70ce9da8`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae1bee24f98056e82d5bdeaa1e269dcfb9e897edd988423740ca2134a29813`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e51fc7981aa274185d3cf9b17706bbf37b8d8ad2e3dfa2f59e3ad3b602abb7`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06a605c0c7f1af061896c9aa90bb26533052b7457a899fb8665f7ea011bba82`  
		Last Modified: Fri, 27 Jun 2025 18:52:14 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6d521afb29c0fd95122117051f94e14d57a940d3c044f6f052844dc703faea0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f1d21463d7b9c00ea7771697266590213c3e990f93b410feedacfa3af6ccb`

```dockerfile
```

-	Layers:
	-	`sha256:e9ba2be1ed520eb11683202ea13e7f9e33237bdfd211b0d1b3912ab3180dbcb7`  
		Last Modified: Fri, 27 Jun 2025 21:49:24 GMT  
		Size: 26.1 KB (26098 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:309b9238691234e4ebb554afa227c0c6b29f169b4e4ce9a68e621db170f964bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:14cd358b4321c90949bdb82ef783d415b288f9e92e594d986b68c46fd1a08a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204656901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faf232a4b6a79ac8955e52df456718817dbd3f2831f8e4c67ffaa276a98aaff`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a89521c1cddce9e2b92a7eea7e2e26f08d9644f8280c2ffabc687ba59a380`  
		Last Modified: Fri, 27 Jun 2025 21:49:38 GMT  
		Size: 7.2 MB (7151605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f97b7e7c107f81c005662fac120035c32226b53ea2f331be0b7d28153bf19b`  
		Last Modified: Fri, 27 Jun 2025 21:49:45 GMT  
		Size: 167.1 MB (167102045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd9e5194ca4898b9a81e75384174a506b3f40f52f3f9a199e61d0bf85ca90d`  
		Last Modified: Fri, 27 Jun 2025 19:03:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a196f26d3fcac6764f1e0cf39781226cf953be5d0859ae1bb2c0bf49dd8bce9e`  
		Last Modified: Fri, 27 Jun 2025 19:03:06 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5445346ace8b927a19dafce4f348e6c2e7eb73610a91488401afec069b151273`  
		Last Modified: Fri, 27 Jun 2025 19:03:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9903e3e75a91e7f238e84fedac46adf1fd322f6dc7d7e24848bdabcce95235f8`  
		Last Modified: Fri, 27 Jun 2025 19:03:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd49a017f1b4781b5e10d0db53ab4474bf9c9cc6736e3334f0324b86276b5421`  
		Last Modified: Fri, 27 Jun 2025 19:03:13 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9ba832181b9f6be8f5f217385d87d47835fd535412a917f140dc7d836051728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0e364a78dad8826a0d237b11ab93f52cdb6e29db46b4a8fd411e98d9115eae`

```dockerfile
```

-	Layers:
	-	`sha256:e65e118aeb542d30c362f3f00125c47cc357f7b682a949fa6a31c1a81aef9f24`  
		Last Modified: Fri, 27 Jun 2025 21:49:21 GMT  
		Size: 25.9 KB (25886 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:43fc7421731f68ef1f15e7c1cd4bd61b89cdef5b0993fbdbd9df1e7f1daf616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192176647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891f121ead07341bdb77db2b6669a46ac9e41676f06eda3133e8a6abc5549437`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a23662fc50e497af13cba7782f06ab2fa94fbce9a6a450a4599446a17c308`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24538160e575723afc9dba473de81c59b5c7b3bf95ff19c0c089485e11b6462`  
		Last Modified: Fri, 27 Jun 2025 21:49:44 GMT  
		Size: 156.8 MB (156822945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e291bf0ee5766818d7442c70ca06b7b7bf86fba4f0a30e2fe86f93975e05a037`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7c8e256097ad6fc4e0dfce399adae584bda2e2343d1086fb20e60d70ce9da8`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae1bee24f98056e82d5bdeaa1e269dcfb9e897edd988423740ca2134a29813`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e51fc7981aa274185d3cf9b17706bbf37b8d8ad2e3dfa2f59e3ad3b602abb7`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06a605c0c7f1af061896c9aa90bb26533052b7457a899fb8665f7ea011bba82`  
		Last Modified: Fri, 27 Jun 2025 18:52:14 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6d521afb29c0fd95122117051f94e14d57a940d3c044f6f052844dc703faea0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f1d21463d7b9c00ea7771697266590213c3e990f93b410feedacfa3af6ccb`

```dockerfile
```

-	Layers:
	-	`sha256:e9ba2be1ed520eb11683202ea13e7f9e33237bdfd211b0d1b3912ab3180dbcb7`  
		Last Modified: Fri, 27 Jun 2025 21:49:24 GMT  
		Size: 26.1 KB (26098 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.4`

```console
$ docker pull clickhouse@sha256:309b9238691234e4ebb554afa227c0c6b29f169b4e4ce9a68e621db170f964bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:14cd358b4321c90949bdb82ef783d415b288f9e92e594d986b68c46fd1a08a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204656901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faf232a4b6a79ac8955e52df456718817dbd3f2831f8e4c67ffaa276a98aaff`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a89521c1cddce9e2b92a7eea7e2e26f08d9644f8280c2ffabc687ba59a380`  
		Last Modified: Fri, 27 Jun 2025 21:49:38 GMT  
		Size: 7.2 MB (7151605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f97b7e7c107f81c005662fac120035c32226b53ea2f331be0b7d28153bf19b`  
		Last Modified: Fri, 27 Jun 2025 21:49:45 GMT  
		Size: 167.1 MB (167102045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd9e5194ca4898b9a81e75384174a506b3f40f52f3f9a199e61d0bf85ca90d`  
		Last Modified: Fri, 27 Jun 2025 19:03:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a196f26d3fcac6764f1e0cf39781226cf953be5d0859ae1bb2c0bf49dd8bce9e`  
		Last Modified: Fri, 27 Jun 2025 19:03:06 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5445346ace8b927a19dafce4f348e6c2e7eb73610a91488401afec069b151273`  
		Last Modified: Fri, 27 Jun 2025 19:03:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9903e3e75a91e7f238e84fedac46adf1fd322f6dc7d7e24848bdabcce95235f8`  
		Last Modified: Fri, 27 Jun 2025 19:03:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd49a017f1b4781b5e10d0db53ab4474bf9c9cc6736e3334f0324b86276b5421`  
		Last Modified: Fri, 27 Jun 2025 19:03:13 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9ba832181b9f6be8f5f217385d87d47835fd535412a917f140dc7d836051728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0e364a78dad8826a0d237b11ab93f52cdb6e29db46b4a8fd411e98d9115eae`

```dockerfile
```

-	Layers:
	-	`sha256:e65e118aeb542d30c362f3f00125c47cc357f7b682a949fa6a31c1a81aef9f24`  
		Last Modified: Fri, 27 Jun 2025 21:49:21 GMT  
		Size: 25.9 KB (25886 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:43fc7421731f68ef1f15e7c1cd4bd61b89cdef5b0993fbdbd9df1e7f1daf616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192176647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891f121ead07341bdb77db2b6669a46ac9e41676f06eda3133e8a6abc5549437`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a23662fc50e497af13cba7782f06ab2fa94fbce9a6a450a4599446a17c308`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24538160e575723afc9dba473de81c59b5c7b3bf95ff19c0c089485e11b6462`  
		Last Modified: Fri, 27 Jun 2025 21:49:44 GMT  
		Size: 156.8 MB (156822945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e291bf0ee5766818d7442c70ca06b7b7bf86fba4f0a30e2fe86f93975e05a037`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7c8e256097ad6fc4e0dfce399adae584bda2e2343d1086fb20e60d70ce9da8`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae1bee24f98056e82d5bdeaa1e269dcfb9e897edd988423740ca2134a29813`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e51fc7981aa274185d3cf9b17706bbf37b8d8ad2e3dfa2f59e3ad3b602abb7`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06a605c0c7f1af061896c9aa90bb26533052b7457a899fb8665f7ea011bba82`  
		Last Modified: Fri, 27 Jun 2025 18:52:14 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6d521afb29c0fd95122117051f94e14d57a940d3c044f6f052844dc703faea0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f1d21463d7b9c00ea7771697266590213c3e990f93b410feedacfa3af6ccb`

```dockerfile
```

-	Layers:
	-	`sha256:e9ba2be1ed520eb11683202ea13e7f9e33237bdfd211b0d1b3912ab3180dbcb7`  
		Last Modified: Fri, 27 Jun 2025 21:49:24 GMT  
		Size: 26.1 KB (26098 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.4-jammy`

```console
$ docker pull clickhouse@sha256:309b9238691234e4ebb554afa227c0c6b29f169b4e4ce9a68e621db170f964bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:14cd358b4321c90949bdb82ef783d415b288f9e92e594d986b68c46fd1a08a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204656901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faf232a4b6a79ac8955e52df456718817dbd3f2831f8e4c67ffaa276a98aaff`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a89521c1cddce9e2b92a7eea7e2e26f08d9644f8280c2ffabc687ba59a380`  
		Last Modified: Fri, 27 Jun 2025 21:49:38 GMT  
		Size: 7.2 MB (7151605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f97b7e7c107f81c005662fac120035c32226b53ea2f331be0b7d28153bf19b`  
		Last Modified: Fri, 27 Jun 2025 21:49:45 GMT  
		Size: 167.1 MB (167102045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd9e5194ca4898b9a81e75384174a506b3f40f52f3f9a199e61d0bf85ca90d`  
		Last Modified: Fri, 27 Jun 2025 19:03:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a196f26d3fcac6764f1e0cf39781226cf953be5d0859ae1bb2c0bf49dd8bce9e`  
		Last Modified: Fri, 27 Jun 2025 19:03:06 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5445346ace8b927a19dafce4f348e6c2e7eb73610a91488401afec069b151273`  
		Last Modified: Fri, 27 Jun 2025 19:03:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9903e3e75a91e7f238e84fedac46adf1fd322f6dc7d7e24848bdabcce95235f8`  
		Last Modified: Fri, 27 Jun 2025 19:03:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd49a017f1b4781b5e10d0db53ab4474bf9c9cc6736e3334f0324b86276b5421`  
		Last Modified: Fri, 27 Jun 2025 19:03:13 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9ba832181b9f6be8f5f217385d87d47835fd535412a917f140dc7d836051728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0e364a78dad8826a0d237b11ab93f52cdb6e29db46b4a8fd411e98d9115eae`

```dockerfile
```

-	Layers:
	-	`sha256:e65e118aeb542d30c362f3f00125c47cc357f7b682a949fa6a31c1a81aef9f24`  
		Last Modified: Fri, 27 Jun 2025 21:49:21 GMT  
		Size: 25.9 KB (25886 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:43fc7421731f68ef1f15e7c1cd4bd61b89cdef5b0993fbdbd9df1e7f1daf616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192176647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891f121ead07341bdb77db2b6669a46ac9e41676f06eda3133e8a6abc5549437`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a23662fc50e497af13cba7782f06ab2fa94fbce9a6a450a4599446a17c308`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24538160e575723afc9dba473de81c59b5c7b3bf95ff19c0c089485e11b6462`  
		Last Modified: Fri, 27 Jun 2025 21:49:44 GMT  
		Size: 156.8 MB (156822945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e291bf0ee5766818d7442c70ca06b7b7bf86fba4f0a30e2fe86f93975e05a037`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7c8e256097ad6fc4e0dfce399adae584bda2e2343d1086fb20e60d70ce9da8`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae1bee24f98056e82d5bdeaa1e269dcfb9e897edd988423740ca2134a29813`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e51fc7981aa274185d3cf9b17706bbf37b8d8ad2e3dfa2f59e3ad3b602abb7`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06a605c0c7f1af061896c9aa90bb26533052b7457a899fb8665f7ea011bba82`  
		Last Modified: Fri, 27 Jun 2025 18:52:14 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6d521afb29c0fd95122117051f94e14d57a940d3c044f6f052844dc703faea0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f1d21463d7b9c00ea7771697266590213c3e990f93b410feedacfa3af6ccb`

```dockerfile
```

-	Layers:
	-	`sha256:e9ba2be1ed520eb11683202ea13e7f9e33237bdfd211b0d1b3912ab3180dbcb7`  
		Last Modified: Fri, 27 Jun 2025 21:49:24 GMT  
		Size: 26.1 KB (26098 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.4.190`

```console
$ docker pull clickhouse@sha256:309b9238691234e4ebb554afa227c0c6b29f169b4e4ce9a68e621db170f964bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.4.190` - linux; amd64

```console
$ docker pull clickhouse@sha256:14cd358b4321c90949bdb82ef783d415b288f9e92e594d986b68c46fd1a08a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204656901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faf232a4b6a79ac8955e52df456718817dbd3f2831f8e4c67ffaa276a98aaff`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a89521c1cddce9e2b92a7eea7e2e26f08d9644f8280c2ffabc687ba59a380`  
		Last Modified: Fri, 27 Jun 2025 21:49:38 GMT  
		Size: 7.2 MB (7151605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f97b7e7c107f81c005662fac120035c32226b53ea2f331be0b7d28153bf19b`  
		Last Modified: Fri, 27 Jun 2025 21:49:45 GMT  
		Size: 167.1 MB (167102045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd9e5194ca4898b9a81e75384174a506b3f40f52f3f9a199e61d0bf85ca90d`  
		Last Modified: Fri, 27 Jun 2025 19:03:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a196f26d3fcac6764f1e0cf39781226cf953be5d0859ae1bb2c0bf49dd8bce9e`  
		Last Modified: Fri, 27 Jun 2025 19:03:06 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5445346ace8b927a19dafce4f348e6c2e7eb73610a91488401afec069b151273`  
		Last Modified: Fri, 27 Jun 2025 19:03:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9903e3e75a91e7f238e84fedac46adf1fd322f6dc7d7e24848bdabcce95235f8`  
		Last Modified: Fri, 27 Jun 2025 19:03:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd49a017f1b4781b5e10d0db53ab4474bf9c9cc6736e3334f0324b86276b5421`  
		Last Modified: Fri, 27 Jun 2025 19:03:13 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.4.190` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9ba832181b9f6be8f5f217385d87d47835fd535412a917f140dc7d836051728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0e364a78dad8826a0d237b11ab93f52cdb6e29db46b4a8fd411e98d9115eae`

```dockerfile
```

-	Layers:
	-	`sha256:e65e118aeb542d30c362f3f00125c47cc357f7b682a949fa6a31c1a81aef9f24`  
		Last Modified: Fri, 27 Jun 2025 21:49:21 GMT  
		Size: 25.9 KB (25886 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.4.190` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:43fc7421731f68ef1f15e7c1cd4bd61b89cdef5b0993fbdbd9df1e7f1daf616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192176647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891f121ead07341bdb77db2b6669a46ac9e41676f06eda3133e8a6abc5549437`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a23662fc50e497af13cba7782f06ab2fa94fbce9a6a450a4599446a17c308`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24538160e575723afc9dba473de81c59b5c7b3bf95ff19c0c089485e11b6462`  
		Last Modified: Fri, 27 Jun 2025 21:49:44 GMT  
		Size: 156.8 MB (156822945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e291bf0ee5766818d7442c70ca06b7b7bf86fba4f0a30e2fe86f93975e05a037`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7c8e256097ad6fc4e0dfce399adae584bda2e2343d1086fb20e60d70ce9da8`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae1bee24f98056e82d5bdeaa1e269dcfb9e897edd988423740ca2134a29813`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e51fc7981aa274185d3cf9b17706bbf37b8d8ad2e3dfa2f59e3ad3b602abb7`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06a605c0c7f1af061896c9aa90bb26533052b7457a899fb8665f7ea011bba82`  
		Last Modified: Fri, 27 Jun 2025 18:52:14 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.4.190` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6d521afb29c0fd95122117051f94e14d57a940d3c044f6f052844dc703faea0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f1d21463d7b9c00ea7771697266590213c3e990f93b410feedacfa3af6ccb`

```dockerfile
```

-	Layers:
	-	`sha256:e9ba2be1ed520eb11683202ea13e7f9e33237bdfd211b0d1b3912ab3180dbcb7`  
		Last Modified: Fri, 27 Jun 2025 21:49:24 GMT  
		Size: 26.1 KB (26098 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.4.190-jammy`

```console
$ docker pull clickhouse@sha256:309b9238691234e4ebb554afa227c0c6b29f169b4e4ce9a68e621db170f964bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.4.190-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:14cd358b4321c90949bdb82ef783d415b288f9e92e594d986b68c46fd1a08a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204656901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faf232a4b6a79ac8955e52df456718817dbd3f2831f8e4c67ffaa276a98aaff`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a89521c1cddce9e2b92a7eea7e2e26f08d9644f8280c2ffabc687ba59a380`  
		Last Modified: Fri, 27 Jun 2025 21:49:38 GMT  
		Size: 7.2 MB (7151605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f97b7e7c107f81c005662fac120035c32226b53ea2f331be0b7d28153bf19b`  
		Last Modified: Fri, 27 Jun 2025 21:49:45 GMT  
		Size: 167.1 MB (167102045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd9e5194ca4898b9a81e75384174a506b3f40f52f3f9a199e61d0bf85ca90d`  
		Last Modified: Fri, 27 Jun 2025 19:03:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a196f26d3fcac6764f1e0cf39781226cf953be5d0859ae1bb2c0bf49dd8bce9e`  
		Last Modified: Fri, 27 Jun 2025 19:03:06 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5445346ace8b927a19dafce4f348e6c2e7eb73610a91488401afec069b151273`  
		Last Modified: Fri, 27 Jun 2025 19:03:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9903e3e75a91e7f238e84fedac46adf1fd322f6dc7d7e24848bdabcce95235f8`  
		Last Modified: Fri, 27 Jun 2025 19:03:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd49a017f1b4781b5e10d0db53ab4474bf9c9cc6736e3334f0324b86276b5421`  
		Last Modified: Fri, 27 Jun 2025 19:03:13 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.4.190-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9ba832181b9f6be8f5f217385d87d47835fd535412a917f140dc7d836051728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0e364a78dad8826a0d237b11ab93f52cdb6e29db46b4a8fd411e98d9115eae`

```dockerfile
```

-	Layers:
	-	`sha256:e65e118aeb542d30c362f3f00125c47cc357f7b682a949fa6a31c1a81aef9f24`  
		Last Modified: Fri, 27 Jun 2025 21:49:21 GMT  
		Size: 25.9 KB (25886 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.4.190-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:43fc7421731f68ef1f15e7c1cd4bd61b89cdef5b0993fbdbd9df1e7f1daf616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192176647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891f121ead07341bdb77db2b6669a46ac9e41676f06eda3133e8a6abc5549437`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a23662fc50e497af13cba7782f06ab2fa94fbce9a6a450a4599446a17c308`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24538160e575723afc9dba473de81c59b5c7b3bf95ff19c0c089485e11b6462`  
		Last Modified: Fri, 27 Jun 2025 21:49:44 GMT  
		Size: 156.8 MB (156822945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e291bf0ee5766818d7442c70ca06b7b7bf86fba4f0a30e2fe86f93975e05a037`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7c8e256097ad6fc4e0dfce399adae584bda2e2343d1086fb20e60d70ce9da8`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae1bee24f98056e82d5bdeaa1e269dcfb9e897edd988423740ca2134a29813`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e51fc7981aa274185d3cf9b17706bbf37b8d8ad2e3dfa2f59e3ad3b602abb7`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06a605c0c7f1af061896c9aa90bb26533052b7457a899fb8665f7ea011bba82`  
		Last Modified: Fri, 27 Jun 2025 18:52:14 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.4.190-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6d521afb29c0fd95122117051f94e14d57a940d3c044f6f052844dc703faea0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f1d21463d7b9c00ea7771697266590213c3e990f93b410feedacfa3af6ccb`

```dockerfile
```

-	Layers:
	-	`sha256:e9ba2be1ed520eb11683202ea13e7f9e33237bdfd211b0d1b3912ab3180dbcb7`  
		Last Modified: Fri, 27 Jun 2025 21:49:24 GMT  
		Size: 26.1 KB (26098 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4`

```console
$ docker pull clickhouse@sha256:7d941fcb6a417f4592f2e62608fcca16cdaf1976a9c0de70fd2df5a2f2a79a45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:ef305e871379c505f6547a6a20e4dbd6fd1daaa8ca0bafb47312a0e3746a010c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202672712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ac0e57ad5b0775eec31e913117a7418cdce48fcdd5c2bffb497cefe49107ec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90db45ca630b32c1aee394afef6af6b4bdceef25c9cd42caba5a75a4e914350f`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 7.2 MB (7151691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116d84072a7b4ee7ff0fc9f87ec7e8b668e4c09b10bbd94e96eaabef8a56aabe`  
		Last Modified: Fri, 20 Jun 2025 21:49:53 GMT  
		Size: 165.1 MB (165117772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cb5b06c09f47c1a0c1aab91b853679f8a9d6b86eaa1d2c1dbf85f55dde98e6`  
		Last Modified: Fri, 20 Jun 2025 19:28:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e276434535f5fb973c3ed3680efa66ff4d275ccaa8341ed898e3bc104ff2423`  
		Last Modified: Fri, 20 Jun 2025 19:10:02 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6bafc5ede62a1c9775a8ffb194b7a4dbbcce115cfb42163ccfe23e1de53f2d`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1528e9b1b42881df91ac080dd8b1acb6a79f828a18d0717926d07e48c72fa7a6`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff35cda4c1602192a0a12932c818329a1281582ec5db0de8e21825bc5693d2e`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56002d3df07b508f81e4cec7712921585a9c07369f83bb8a4ec528dfef20e8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadd3364fc9419203d16dc794876535acda759b473880be4e27df2c89f6683fe`

```dockerfile
```

-	Layers:
	-	`sha256:2dea52c158192579ab3c2b28d0060d6f48b85e84de802fff4d92dcfdd431f5c0`  
		Last Modified: Fri, 20 Jun 2025 21:49:27 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c981f4aaa340c5e2e928a78e6bb03b3bf1fdcf61e781cf42666e639e4f77d5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190018693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbfa8bdb5c59d0d688ca20088e62ca1a6bf01822fb5593e6faa0bd90ac0199c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb668d033b9955e1146ceea6fd1adb67975022b500848472d75f5cc3449dc4f3`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f4bf25386c0616266474dc4db6173d60a3f277972248c168f300587b33bf7`  
		Last Modified: Fri, 20 Jun 2025 21:49:57 GMT  
		Size: 154.7 MB (154664981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e2426bb3f6229d3c8c01c2515a6364206d27d8b964efd240143786cdf0cde2`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c135f71abe52d3527d1cbebd5d50939fb235df24539ad9ee8cb2a4e41560c27`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c9a5208efe41733ace31fc44d930d5ba8a22a292cde556c79f21936614971c`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de909ad28ad42028bde7fba8e37fa4da16279d835540b4961dcc444b7d70ff0`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599cf6a55cc0b2a63d706202561889d78b7810a3d24aaddc92861fe80f0a742e`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f8b17bc70a387b63fbe9328058424fd0b6d26c96a9a91816a93e104242bb2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8108bca16ceb7a689424217c4a1b93c4c659ec8bbd466fd06efaedfd5048418d`

```dockerfile
```

-	Layers:
	-	`sha256:0dc69bf1c4d172a2009a150da6135c9bc06c24422a6d9fb2e7ad3b2269b03fb5`  
		Last Modified: Fri, 20 Jun 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4-jammy`

```console
$ docker pull clickhouse@sha256:7d941fcb6a417f4592f2e62608fcca16cdaf1976a9c0de70fd2df5a2f2a79a45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ef305e871379c505f6547a6a20e4dbd6fd1daaa8ca0bafb47312a0e3746a010c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202672712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ac0e57ad5b0775eec31e913117a7418cdce48fcdd5c2bffb497cefe49107ec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90db45ca630b32c1aee394afef6af6b4bdceef25c9cd42caba5a75a4e914350f`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 7.2 MB (7151691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116d84072a7b4ee7ff0fc9f87ec7e8b668e4c09b10bbd94e96eaabef8a56aabe`  
		Last Modified: Fri, 20 Jun 2025 21:49:53 GMT  
		Size: 165.1 MB (165117772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cb5b06c09f47c1a0c1aab91b853679f8a9d6b86eaa1d2c1dbf85f55dde98e6`  
		Last Modified: Fri, 20 Jun 2025 19:28:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e276434535f5fb973c3ed3680efa66ff4d275ccaa8341ed898e3bc104ff2423`  
		Last Modified: Fri, 20 Jun 2025 19:10:02 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6bafc5ede62a1c9775a8ffb194b7a4dbbcce115cfb42163ccfe23e1de53f2d`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1528e9b1b42881df91ac080dd8b1acb6a79f828a18d0717926d07e48c72fa7a6`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff35cda4c1602192a0a12932c818329a1281582ec5db0de8e21825bc5693d2e`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56002d3df07b508f81e4cec7712921585a9c07369f83bb8a4ec528dfef20e8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadd3364fc9419203d16dc794876535acda759b473880be4e27df2c89f6683fe`

```dockerfile
```

-	Layers:
	-	`sha256:2dea52c158192579ab3c2b28d0060d6f48b85e84de802fff4d92dcfdd431f5c0`  
		Last Modified: Fri, 20 Jun 2025 21:49:27 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c981f4aaa340c5e2e928a78e6bb03b3bf1fdcf61e781cf42666e639e4f77d5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190018693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbfa8bdb5c59d0d688ca20088e62ca1a6bf01822fb5593e6faa0bd90ac0199c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb668d033b9955e1146ceea6fd1adb67975022b500848472d75f5cc3449dc4f3`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f4bf25386c0616266474dc4db6173d60a3f277972248c168f300587b33bf7`  
		Last Modified: Fri, 20 Jun 2025 21:49:57 GMT  
		Size: 154.7 MB (154664981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e2426bb3f6229d3c8c01c2515a6364206d27d8b964efd240143786cdf0cde2`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c135f71abe52d3527d1cbebd5d50939fb235df24539ad9ee8cb2a4e41560c27`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c9a5208efe41733ace31fc44d930d5ba8a22a292cde556c79f21936614971c`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de909ad28ad42028bde7fba8e37fa4da16279d835540b4961dcc444b7d70ff0`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599cf6a55cc0b2a63d706202561889d78b7810a3d24aaddc92861fe80f0a742e`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f8b17bc70a387b63fbe9328058424fd0b6d26c96a9a91816a93e104242bb2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8108bca16ceb7a689424217c4a1b93c4c659ec8bbd466fd06efaedfd5048418d`

```dockerfile
```

-	Layers:
	-	`sha256:0dc69bf1c4d172a2009a150da6135c9bc06c24422a6d9fb2e7ad3b2269b03fb5`  
		Last Modified: Fri, 20 Jun 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.7`

```console
$ docker pull clickhouse@sha256:7d941fcb6a417f4592f2e62608fcca16cdaf1976a9c0de70fd2df5a2f2a79a45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:ef305e871379c505f6547a6a20e4dbd6fd1daaa8ca0bafb47312a0e3746a010c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202672712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ac0e57ad5b0775eec31e913117a7418cdce48fcdd5c2bffb497cefe49107ec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90db45ca630b32c1aee394afef6af6b4bdceef25c9cd42caba5a75a4e914350f`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 7.2 MB (7151691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116d84072a7b4ee7ff0fc9f87ec7e8b668e4c09b10bbd94e96eaabef8a56aabe`  
		Last Modified: Fri, 20 Jun 2025 21:49:53 GMT  
		Size: 165.1 MB (165117772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cb5b06c09f47c1a0c1aab91b853679f8a9d6b86eaa1d2c1dbf85f55dde98e6`  
		Last Modified: Fri, 20 Jun 2025 19:28:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e276434535f5fb973c3ed3680efa66ff4d275ccaa8341ed898e3bc104ff2423`  
		Last Modified: Fri, 20 Jun 2025 19:10:02 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6bafc5ede62a1c9775a8ffb194b7a4dbbcce115cfb42163ccfe23e1de53f2d`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1528e9b1b42881df91ac080dd8b1acb6a79f828a18d0717926d07e48c72fa7a6`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff35cda4c1602192a0a12932c818329a1281582ec5db0de8e21825bc5693d2e`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56002d3df07b508f81e4cec7712921585a9c07369f83bb8a4ec528dfef20e8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadd3364fc9419203d16dc794876535acda759b473880be4e27df2c89f6683fe`

```dockerfile
```

-	Layers:
	-	`sha256:2dea52c158192579ab3c2b28d0060d6f48b85e84de802fff4d92dcfdd431f5c0`  
		Last Modified: Fri, 20 Jun 2025 21:49:27 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c981f4aaa340c5e2e928a78e6bb03b3bf1fdcf61e781cf42666e639e4f77d5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190018693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbfa8bdb5c59d0d688ca20088e62ca1a6bf01822fb5593e6faa0bd90ac0199c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb668d033b9955e1146ceea6fd1adb67975022b500848472d75f5cc3449dc4f3`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f4bf25386c0616266474dc4db6173d60a3f277972248c168f300587b33bf7`  
		Last Modified: Fri, 20 Jun 2025 21:49:57 GMT  
		Size: 154.7 MB (154664981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e2426bb3f6229d3c8c01c2515a6364206d27d8b964efd240143786cdf0cde2`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c135f71abe52d3527d1cbebd5d50939fb235df24539ad9ee8cb2a4e41560c27`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c9a5208efe41733ace31fc44d930d5ba8a22a292cde556c79f21936614971c`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de909ad28ad42028bde7fba8e37fa4da16279d835540b4961dcc444b7d70ff0`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599cf6a55cc0b2a63d706202561889d78b7810a3d24aaddc92861fe80f0a742e`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f8b17bc70a387b63fbe9328058424fd0b6d26c96a9a91816a93e104242bb2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8108bca16ceb7a689424217c4a1b93c4c659ec8bbd466fd06efaedfd5048418d`

```dockerfile
```

-	Layers:
	-	`sha256:0dc69bf1c4d172a2009a150da6135c9bc06c24422a6d9fb2e7ad3b2269b03fb5`  
		Last Modified: Fri, 20 Jun 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.7-jammy`

```console
$ docker pull clickhouse@sha256:7d941fcb6a417f4592f2e62608fcca16cdaf1976a9c0de70fd2df5a2f2a79a45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ef305e871379c505f6547a6a20e4dbd6fd1daaa8ca0bafb47312a0e3746a010c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202672712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ac0e57ad5b0775eec31e913117a7418cdce48fcdd5c2bffb497cefe49107ec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90db45ca630b32c1aee394afef6af6b4bdceef25c9cd42caba5a75a4e914350f`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 7.2 MB (7151691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116d84072a7b4ee7ff0fc9f87ec7e8b668e4c09b10bbd94e96eaabef8a56aabe`  
		Last Modified: Fri, 20 Jun 2025 21:49:53 GMT  
		Size: 165.1 MB (165117772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cb5b06c09f47c1a0c1aab91b853679f8a9d6b86eaa1d2c1dbf85f55dde98e6`  
		Last Modified: Fri, 20 Jun 2025 19:28:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e276434535f5fb973c3ed3680efa66ff4d275ccaa8341ed898e3bc104ff2423`  
		Last Modified: Fri, 20 Jun 2025 19:10:02 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6bafc5ede62a1c9775a8ffb194b7a4dbbcce115cfb42163ccfe23e1de53f2d`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1528e9b1b42881df91ac080dd8b1acb6a79f828a18d0717926d07e48c72fa7a6`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff35cda4c1602192a0a12932c818329a1281582ec5db0de8e21825bc5693d2e`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56002d3df07b508f81e4cec7712921585a9c07369f83bb8a4ec528dfef20e8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadd3364fc9419203d16dc794876535acda759b473880be4e27df2c89f6683fe`

```dockerfile
```

-	Layers:
	-	`sha256:2dea52c158192579ab3c2b28d0060d6f48b85e84de802fff4d92dcfdd431f5c0`  
		Last Modified: Fri, 20 Jun 2025 21:49:27 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c981f4aaa340c5e2e928a78e6bb03b3bf1fdcf61e781cf42666e639e4f77d5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190018693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbfa8bdb5c59d0d688ca20088e62ca1a6bf01822fb5593e6faa0bd90ac0199c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb668d033b9955e1146ceea6fd1adb67975022b500848472d75f5cc3449dc4f3`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f4bf25386c0616266474dc4db6173d60a3f277972248c168f300587b33bf7`  
		Last Modified: Fri, 20 Jun 2025 21:49:57 GMT  
		Size: 154.7 MB (154664981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e2426bb3f6229d3c8c01c2515a6364206d27d8b964efd240143786cdf0cde2`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c135f71abe52d3527d1cbebd5d50939fb235df24539ad9ee8cb2a4e41560c27`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c9a5208efe41733ace31fc44d930d5ba8a22a292cde556c79f21936614971c`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de909ad28ad42028bde7fba8e37fa4da16279d835540b4961dcc444b7d70ff0`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599cf6a55cc0b2a63d706202561889d78b7810a3d24aaddc92861fe80f0a742e`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f8b17bc70a387b63fbe9328058424fd0b6d26c96a9a91816a93e104242bb2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8108bca16ceb7a689424217c4a1b93c4c659ec8bbd466fd06efaedfd5048418d`

```dockerfile
```

-	Layers:
	-	`sha256:0dc69bf1c4d172a2009a150da6135c9bc06c24422a6d9fb2e7ad3b2269b03fb5`  
		Last Modified: Fri, 20 Jun 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.7.66`

```console
$ docker pull clickhouse@sha256:7d941fcb6a417f4592f2e62608fcca16cdaf1976a9c0de70fd2df5a2f2a79a45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.7.66` - linux; amd64

```console
$ docker pull clickhouse@sha256:ef305e871379c505f6547a6a20e4dbd6fd1daaa8ca0bafb47312a0e3746a010c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202672712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ac0e57ad5b0775eec31e913117a7418cdce48fcdd5c2bffb497cefe49107ec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90db45ca630b32c1aee394afef6af6b4bdceef25c9cd42caba5a75a4e914350f`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 7.2 MB (7151691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116d84072a7b4ee7ff0fc9f87ec7e8b668e4c09b10bbd94e96eaabef8a56aabe`  
		Last Modified: Fri, 20 Jun 2025 21:49:53 GMT  
		Size: 165.1 MB (165117772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cb5b06c09f47c1a0c1aab91b853679f8a9d6b86eaa1d2c1dbf85f55dde98e6`  
		Last Modified: Fri, 20 Jun 2025 19:28:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e276434535f5fb973c3ed3680efa66ff4d275ccaa8341ed898e3bc104ff2423`  
		Last Modified: Fri, 20 Jun 2025 19:10:02 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6bafc5ede62a1c9775a8ffb194b7a4dbbcce115cfb42163ccfe23e1de53f2d`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1528e9b1b42881df91ac080dd8b1acb6a79f828a18d0717926d07e48c72fa7a6`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff35cda4c1602192a0a12932c818329a1281582ec5db0de8e21825bc5693d2e`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.7.66` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56002d3df07b508f81e4cec7712921585a9c07369f83bb8a4ec528dfef20e8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadd3364fc9419203d16dc794876535acda759b473880be4e27df2c89f6683fe`

```dockerfile
```

-	Layers:
	-	`sha256:2dea52c158192579ab3c2b28d0060d6f48b85e84de802fff4d92dcfdd431f5c0`  
		Last Modified: Fri, 20 Jun 2025 21:49:27 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.7.66` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c981f4aaa340c5e2e928a78e6bb03b3bf1fdcf61e781cf42666e639e4f77d5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190018693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbfa8bdb5c59d0d688ca20088e62ca1a6bf01822fb5593e6faa0bd90ac0199c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb668d033b9955e1146ceea6fd1adb67975022b500848472d75f5cc3449dc4f3`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f4bf25386c0616266474dc4db6173d60a3f277972248c168f300587b33bf7`  
		Last Modified: Fri, 20 Jun 2025 21:49:57 GMT  
		Size: 154.7 MB (154664981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e2426bb3f6229d3c8c01c2515a6364206d27d8b964efd240143786cdf0cde2`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c135f71abe52d3527d1cbebd5d50939fb235df24539ad9ee8cb2a4e41560c27`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c9a5208efe41733ace31fc44d930d5ba8a22a292cde556c79f21936614971c`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de909ad28ad42028bde7fba8e37fa4da16279d835540b4961dcc444b7d70ff0`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599cf6a55cc0b2a63d706202561889d78b7810a3d24aaddc92861fe80f0a742e`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.7.66` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f8b17bc70a387b63fbe9328058424fd0b6d26c96a9a91816a93e104242bb2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8108bca16ceb7a689424217c4a1b93c4c659ec8bbd466fd06efaedfd5048418d`

```dockerfile
```

-	Layers:
	-	`sha256:0dc69bf1c4d172a2009a150da6135c9bc06c24422a6d9fb2e7ad3b2269b03fb5`  
		Last Modified: Fri, 20 Jun 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.7.66-jammy`

```console
$ docker pull clickhouse@sha256:7d941fcb6a417f4592f2e62608fcca16cdaf1976a9c0de70fd2df5a2f2a79a45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.7.66-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ef305e871379c505f6547a6a20e4dbd6fd1daaa8ca0bafb47312a0e3746a010c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202672712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ac0e57ad5b0775eec31e913117a7418cdce48fcdd5c2bffb497cefe49107ec`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90db45ca630b32c1aee394afef6af6b4bdceef25c9cd42caba5a75a4e914350f`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 7.2 MB (7151691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:116d84072a7b4ee7ff0fc9f87ec7e8b668e4c09b10bbd94e96eaabef8a56aabe`  
		Last Modified: Fri, 20 Jun 2025 21:49:53 GMT  
		Size: 165.1 MB (165117772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1cb5b06c09f47c1a0c1aab91b853679f8a9d6b86eaa1d2c1dbf85f55dde98e6`  
		Last Modified: Fri, 20 Jun 2025 19:28:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e276434535f5fb973c3ed3680efa66ff4d275ccaa8341ed898e3bc104ff2423`  
		Last Modified: Fri, 20 Jun 2025 19:10:02 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6bafc5ede62a1c9775a8ffb194b7a4dbbcce115cfb42163ccfe23e1de53f2d`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1528e9b1b42881df91ac080dd8b1acb6a79f828a18d0717926d07e48c72fa7a6`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff35cda4c1602192a0a12932c818329a1281582ec5db0de8e21825bc5693d2e`  
		Last Modified: Fri, 20 Jun 2025 19:10:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.7.66-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:56002d3df07b508f81e4cec7712921585a9c07369f83bb8a4ec528dfef20e8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fadd3364fc9419203d16dc794876535acda759b473880be4e27df2c89f6683fe`

```dockerfile
```

-	Layers:
	-	`sha256:2dea52c158192579ab3c2b28d0060d6f48b85e84de802fff4d92dcfdd431f5c0`  
		Last Modified: Fri, 20 Jun 2025 21:49:27 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.7.66-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:c981f4aaa340c5e2e928a78e6bb03b3bf1fdcf61e781cf42666e639e4f77d5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190018693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acbfa8bdb5c59d0d688ca20088e62ca1a6bf01822fb5593e6faa0bd90ac0199c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 20 Jun 2025 10:04:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 20 Jun 2025 10:04:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 20 Jun 2025 10:04:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 20 Jun 2025 10:04:10 GMT
ARG VERSION=25.4.7.66
# Fri, 20 Jun 2025 10:04:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
ENV LANG=en_US.UTF-8
# Fri, 20 Jun 2025 10:04:10 GMT
ENV TZ=UTC
# Fri, 20 Jun 2025 10:04:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.7.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 20 Jun 2025 10:04:10 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 20 Jun 2025 10:04:10 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 20 Jun 2025 10:04:10 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 20 Jun 2025 10:04:10 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb668d033b9955e1146ceea6fd1adb67975022b500848472d75f5cc3449dc4f3`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33f4bf25386c0616266474dc4db6173d60a3f277972248c168f300587b33bf7`  
		Last Modified: Fri, 20 Jun 2025 21:49:57 GMT  
		Size: 154.7 MB (154664981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e2426bb3f6229d3c8c01c2515a6364206d27d8b964efd240143786cdf0cde2`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c135f71abe52d3527d1cbebd5d50939fb235df24539ad9ee8cb2a4e41560c27`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c9a5208efe41733ace31fc44d930d5ba8a22a292cde556c79f21936614971c`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de909ad28ad42028bde7fba8e37fa4da16279d835540b4961dcc444b7d70ff0`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599cf6a55cc0b2a63d706202561889d78b7810a3d24aaddc92861fe80f0a742e`  
		Last Modified: Fri, 20 Jun 2025 21:49:48 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.7.66-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f8b17bc70a387b63fbe9328058424fd0b6d26c96a9a91816a93e104242bb2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8108bca16ceb7a689424217c4a1b93c4c659ec8bbd466fd06efaedfd5048418d`

```dockerfile
```

-	Layers:
	-	`sha256:0dc69bf1c4d172a2009a150da6135c9bc06c24422a6d9fb2e7ad3b2269b03fb5`  
		Last Modified: Fri, 20 Jun 2025 21:49:36 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5`

```console
$ docker pull clickhouse@sha256:976a87b43b93ee9a57274300e9bdcb8aca40e33f3153a0285e16b835e4af7237
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:4cfa64eee53cd83746444d308daf7d195fe13b0a10bb87dd124389849b17d427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204925366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ccbb5afcc107eec5ea013360bfb8e00307a9b682378d281440e3d75f59e00a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.5.4.38
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566bb5305f1ad530116b3d87aef49f9c9285be8efc8b4ee589521fd6a890c926`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 7.2 MB (7151703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab249ebf6595eb4c777726f438316ce6d6f047eef8d7b1582914266ad523ad21`  
		Last Modified: Fri, 27 Jun 2025 21:49:57 GMT  
		Size: 167.4 MB (167370411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f3884935fe25d86737352a1d65a0159a3c336ec68be36e6a303ba62357f7a9`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d79771ae5550a8d3b6db26b0c500829b466951e01a53881a92894492b2ebb65`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd10851e3462f8d5b64dc30c65d245b95f1a86cf87f347e8cf0d8d9554f9924f`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f20a0138f6c07af47ae0a24abdcd60cd56cde7fc11a6318e6d83bbee2ca2f0`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82912db37c2e5044c9d13a9dbbd3bb06d23c507152c22444327cc17d073c85b5`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:780c69edaeafef43fc4dff9e6331109ad097efb8ceffa47d0ea0c650ba92e62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e269b7df1f9ab1b7c9a530e18d2c85a932200881b3418e374ae91233d9f42ea`

```dockerfile
```

-	Layers:
	-	`sha256:81dd76ba77ac4686a5d0c1bb5b27a1d5469e543bf808b3fdd15f161368913118`  
		Last Modified: Fri, 27 Jun 2025 21:49:36 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1b584caa772022abc093e5fb7f9a659737848f71f16fb53263a449e46fb4e60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191498689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff8492b23c38f0c70b3f0c08b0cd4c680e3097f2c4e3686c9d1d19106af89e9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.5.4.38
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a23662fc50e497af13cba7782f06ab2fa94fbce9a6a450a4599446a17c308`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b787bf45549031cf5fd67d27c5c27f2b5ffc1e42937525cbf567fd28d58402`  
		Last Modified: Fri, 27 Jun 2025 21:49:57 GMT  
		Size: 156.1 MB (156144987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d96597c07858324dcb0dca879763024909cfb82b400f632adbcfb7d231816a9`  
		Last Modified: Fri, 27 Jun 2025 18:51:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085971706f494387be02045cb8557c22ee8db89820676c866e73113d18f96190`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdc5a9ef40188972e6405398cd83343004093bba9366b8c3717823c04f78b8c`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3f21e988cecec54e423de032ff28e427e9d4fd9227ca7e9725c5c76fd992af`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1414ea3cf5e1053fa4476294561b8370bd1e1669cab5b44b519b967c94209d22`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:025448e9040e9eee2f2d52ba663099cdf9bbdc0d604409f530ae9cf0f4127a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e508646942141e611337d5994d21a09cf7ef8a2e8758b679168135afd5f57470`

```dockerfile
```

-	Layers:
	-	`sha256:286031c4818828028980b463d4f7af149d43296b7aea3ecced9e349d38bc7496`  
		Last Modified: Fri, 27 Jun 2025 21:49:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5-jammy`

```console
$ docker pull clickhouse@sha256:976a87b43b93ee9a57274300e9bdcb8aca40e33f3153a0285e16b835e4af7237
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:4cfa64eee53cd83746444d308daf7d195fe13b0a10bb87dd124389849b17d427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204925366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ccbb5afcc107eec5ea013360bfb8e00307a9b682378d281440e3d75f59e00a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.5.4.38
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566bb5305f1ad530116b3d87aef49f9c9285be8efc8b4ee589521fd6a890c926`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 7.2 MB (7151703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab249ebf6595eb4c777726f438316ce6d6f047eef8d7b1582914266ad523ad21`  
		Last Modified: Fri, 27 Jun 2025 21:49:57 GMT  
		Size: 167.4 MB (167370411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f3884935fe25d86737352a1d65a0159a3c336ec68be36e6a303ba62357f7a9`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d79771ae5550a8d3b6db26b0c500829b466951e01a53881a92894492b2ebb65`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd10851e3462f8d5b64dc30c65d245b95f1a86cf87f347e8cf0d8d9554f9924f`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f20a0138f6c07af47ae0a24abdcd60cd56cde7fc11a6318e6d83bbee2ca2f0`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82912db37c2e5044c9d13a9dbbd3bb06d23c507152c22444327cc17d073c85b5`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:780c69edaeafef43fc4dff9e6331109ad097efb8ceffa47d0ea0c650ba92e62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e269b7df1f9ab1b7c9a530e18d2c85a932200881b3418e374ae91233d9f42ea`

```dockerfile
```

-	Layers:
	-	`sha256:81dd76ba77ac4686a5d0c1bb5b27a1d5469e543bf808b3fdd15f161368913118`  
		Last Modified: Fri, 27 Jun 2025 21:49:36 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1b584caa772022abc093e5fb7f9a659737848f71f16fb53263a449e46fb4e60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191498689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff8492b23c38f0c70b3f0c08b0cd4c680e3097f2c4e3686c9d1d19106af89e9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.5.4.38
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a23662fc50e497af13cba7782f06ab2fa94fbce9a6a450a4599446a17c308`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b787bf45549031cf5fd67d27c5c27f2b5ffc1e42937525cbf567fd28d58402`  
		Last Modified: Fri, 27 Jun 2025 21:49:57 GMT  
		Size: 156.1 MB (156144987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d96597c07858324dcb0dca879763024909cfb82b400f632adbcfb7d231816a9`  
		Last Modified: Fri, 27 Jun 2025 18:51:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085971706f494387be02045cb8557c22ee8db89820676c866e73113d18f96190`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdc5a9ef40188972e6405398cd83343004093bba9366b8c3717823c04f78b8c`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3f21e988cecec54e423de032ff28e427e9d4fd9227ca7e9725c5c76fd992af`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1414ea3cf5e1053fa4476294561b8370bd1e1669cab5b44b519b967c94209d22`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:025448e9040e9eee2f2d52ba663099cdf9bbdc0d604409f530ae9cf0f4127a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e508646942141e611337d5994d21a09cf7ef8a2e8758b679168135afd5f57470`

```dockerfile
```

-	Layers:
	-	`sha256:286031c4818828028980b463d4f7af149d43296b7aea3ecced9e349d38bc7496`  
		Last Modified: Fri, 27 Jun 2025 21:49:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.4`

```console
$ docker pull clickhouse@sha256:976a87b43b93ee9a57274300e9bdcb8aca40e33f3153a0285e16b835e4af7237
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:4cfa64eee53cd83746444d308daf7d195fe13b0a10bb87dd124389849b17d427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204925366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ccbb5afcc107eec5ea013360bfb8e00307a9b682378d281440e3d75f59e00a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.5.4.38
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566bb5305f1ad530116b3d87aef49f9c9285be8efc8b4ee589521fd6a890c926`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 7.2 MB (7151703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab249ebf6595eb4c777726f438316ce6d6f047eef8d7b1582914266ad523ad21`  
		Last Modified: Fri, 27 Jun 2025 21:49:57 GMT  
		Size: 167.4 MB (167370411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f3884935fe25d86737352a1d65a0159a3c336ec68be36e6a303ba62357f7a9`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d79771ae5550a8d3b6db26b0c500829b466951e01a53881a92894492b2ebb65`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd10851e3462f8d5b64dc30c65d245b95f1a86cf87f347e8cf0d8d9554f9924f`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f20a0138f6c07af47ae0a24abdcd60cd56cde7fc11a6318e6d83bbee2ca2f0`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82912db37c2e5044c9d13a9dbbd3bb06d23c507152c22444327cc17d073c85b5`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:780c69edaeafef43fc4dff9e6331109ad097efb8ceffa47d0ea0c650ba92e62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e269b7df1f9ab1b7c9a530e18d2c85a932200881b3418e374ae91233d9f42ea`

```dockerfile
```

-	Layers:
	-	`sha256:81dd76ba77ac4686a5d0c1bb5b27a1d5469e543bf808b3fdd15f161368913118`  
		Last Modified: Fri, 27 Jun 2025 21:49:36 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1b584caa772022abc093e5fb7f9a659737848f71f16fb53263a449e46fb4e60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191498689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff8492b23c38f0c70b3f0c08b0cd4c680e3097f2c4e3686c9d1d19106af89e9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.5.4.38
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a23662fc50e497af13cba7782f06ab2fa94fbce9a6a450a4599446a17c308`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b787bf45549031cf5fd67d27c5c27f2b5ffc1e42937525cbf567fd28d58402`  
		Last Modified: Fri, 27 Jun 2025 21:49:57 GMT  
		Size: 156.1 MB (156144987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d96597c07858324dcb0dca879763024909cfb82b400f632adbcfb7d231816a9`  
		Last Modified: Fri, 27 Jun 2025 18:51:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085971706f494387be02045cb8557c22ee8db89820676c866e73113d18f96190`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdc5a9ef40188972e6405398cd83343004093bba9366b8c3717823c04f78b8c`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3f21e988cecec54e423de032ff28e427e9d4fd9227ca7e9725c5c76fd992af`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1414ea3cf5e1053fa4476294561b8370bd1e1669cab5b44b519b967c94209d22`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:025448e9040e9eee2f2d52ba663099cdf9bbdc0d604409f530ae9cf0f4127a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e508646942141e611337d5994d21a09cf7ef8a2e8758b679168135afd5f57470`

```dockerfile
```

-	Layers:
	-	`sha256:286031c4818828028980b463d4f7af149d43296b7aea3ecced9e349d38bc7496`  
		Last Modified: Fri, 27 Jun 2025 21:49:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.4-jammy`

```console
$ docker pull clickhouse@sha256:976a87b43b93ee9a57274300e9bdcb8aca40e33f3153a0285e16b835e4af7237
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:4cfa64eee53cd83746444d308daf7d195fe13b0a10bb87dd124389849b17d427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204925366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ccbb5afcc107eec5ea013360bfb8e00307a9b682378d281440e3d75f59e00a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.5.4.38
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566bb5305f1ad530116b3d87aef49f9c9285be8efc8b4ee589521fd6a890c926`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 7.2 MB (7151703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab249ebf6595eb4c777726f438316ce6d6f047eef8d7b1582914266ad523ad21`  
		Last Modified: Fri, 27 Jun 2025 21:49:57 GMT  
		Size: 167.4 MB (167370411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f3884935fe25d86737352a1d65a0159a3c336ec68be36e6a303ba62357f7a9`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d79771ae5550a8d3b6db26b0c500829b466951e01a53881a92894492b2ebb65`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd10851e3462f8d5b64dc30c65d245b95f1a86cf87f347e8cf0d8d9554f9924f`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f20a0138f6c07af47ae0a24abdcd60cd56cde7fc11a6318e6d83bbee2ca2f0`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82912db37c2e5044c9d13a9dbbd3bb06d23c507152c22444327cc17d073c85b5`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:780c69edaeafef43fc4dff9e6331109ad097efb8ceffa47d0ea0c650ba92e62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e269b7df1f9ab1b7c9a530e18d2c85a932200881b3418e374ae91233d9f42ea`

```dockerfile
```

-	Layers:
	-	`sha256:81dd76ba77ac4686a5d0c1bb5b27a1d5469e543bf808b3fdd15f161368913118`  
		Last Modified: Fri, 27 Jun 2025 21:49:36 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1b584caa772022abc093e5fb7f9a659737848f71f16fb53263a449e46fb4e60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191498689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff8492b23c38f0c70b3f0c08b0cd4c680e3097f2c4e3686c9d1d19106af89e9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.5.4.38
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a23662fc50e497af13cba7782f06ab2fa94fbce9a6a450a4599446a17c308`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b787bf45549031cf5fd67d27c5c27f2b5ffc1e42937525cbf567fd28d58402`  
		Last Modified: Fri, 27 Jun 2025 21:49:57 GMT  
		Size: 156.1 MB (156144987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d96597c07858324dcb0dca879763024909cfb82b400f632adbcfb7d231816a9`  
		Last Modified: Fri, 27 Jun 2025 18:51:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085971706f494387be02045cb8557c22ee8db89820676c866e73113d18f96190`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdc5a9ef40188972e6405398cd83343004093bba9366b8c3717823c04f78b8c`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3f21e988cecec54e423de032ff28e427e9d4fd9227ca7e9725c5c76fd992af`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1414ea3cf5e1053fa4476294561b8370bd1e1669cab5b44b519b967c94209d22`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:025448e9040e9eee2f2d52ba663099cdf9bbdc0d604409f530ae9cf0f4127a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e508646942141e611337d5994d21a09cf7ef8a2e8758b679168135afd5f57470`

```dockerfile
```

-	Layers:
	-	`sha256:286031c4818828028980b463d4f7af149d43296b7aea3ecced9e349d38bc7496`  
		Last Modified: Fri, 27 Jun 2025 21:49:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.4.38`

```console
$ docker pull clickhouse@sha256:976a87b43b93ee9a57274300e9bdcb8aca40e33f3153a0285e16b835e4af7237
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.4.38` - linux; amd64

```console
$ docker pull clickhouse@sha256:4cfa64eee53cd83746444d308daf7d195fe13b0a10bb87dd124389849b17d427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204925366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ccbb5afcc107eec5ea013360bfb8e00307a9b682378d281440e3d75f59e00a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.5.4.38
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566bb5305f1ad530116b3d87aef49f9c9285be8efc8b4ee589521fd6a890c926`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 7.2 MB (7151703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab249ebf6595eb4c777726f438316ce6d6f047eef8d7b1582914266ad523ad21`  
		Last Modified: Fri, 27 Jun 2025 21:49:57 GMT  
		Size: 167.4 MB (167370411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f3884935fe25d86737352a1d65a0159a3c336ec68be36e6a303ba62357f7a9`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d79771ae5550a8d3b6db26b0c500829b466951e01a53881a92894492b2ebb65`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd10851e3462f8d5b64dc30c65d245b95f1a86cf87f347e8cf0d8d9554f9924f`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f20a0138f6c07af47ae0a24abdcd60cd56cde7fc11a6318e6d83bbee2ca2f0`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82912db37c2e5044c9d13a9dbbd3bb06d23c507152c22444327cc17d073c85b5`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.4.38` - unknown; unknown

```console
$ docker pull clickhouse@sha256:780c69edaeafef43fc4dff9e6331109ad097efb8ceffa47d0ea0c650ba92e62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e269b7df1f9ab1b7c9a530e18d2c85a932200881b3418e374ae91233d9f42ea`

```dockerfile
```

-	Layers:
	-	`sha256:81dd76ba77ac4686a5d0c1bb5b27a1d5469e543bf808b3fdd15f161368913118`  
		Last Modified: Fri, 27 Jun 2025 21:49:36 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.4.38` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1b584caa772022abc093e5fb7f9a659737848f71f16fb53263a449e46fb4e60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191498689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff8492b23c38f0c70b3f0c08b0cd4c680e3097f2c4e3686c9d1d19106af89e9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.5.4.38
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a23662fc50e497af13cba7782f06ab2fa94fbce9a6a450a4599446a17c308`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b787bf45549031cf5fd67d27c5c27f2b5ffc1e42937525cbf567fd28d58402`  
		Last Modified: Fri, 27 Jun 2025 21:49:57 GMT  
		Size: 156.1 MB (156144987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d96597c07858324dcb0dca879763024909cfb82b400f632adbcfb7d231816a9`  
		Last Modified: Fri, 27 Jun 2025 18:51:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085971706f494387be02045cb8557c22ee8db89820676c866e73113d18f96190`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdc5a9ef40188972e6405398cd83343004093bba9366b8c3717823c04f78b8c`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3f21e988cecec54e423de032ff28e427e9d4fd9227ca7e9725c5c76fd992af`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1414ea3cf5e1053fa4476294561b8370bd1e1669cab5b44b519b967c94209d22`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.4.38` - unknown; unknown

```console
$ docker pull clickhouse@sha256:025448e9040e9eee2f2d52ba663099cdf9bbdc0d604409f530ae9cf0f4127a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e508646942141e611337d5994d21a09cf7ef8a2e8758b679168135afd5f57470`

```dockerfile
```

-	Layers:
	-	`sha256:286031c4818828028980b463d4f7af149d43296b7aea3ecced9e349d38bc7496`  
		Last Modified: Fri, 27 Jun 2025 21:49:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.4.38-jammy`

```console
$ docker pull clickhouse@sha256:976a87b43b93ee9a57274300e9bdcb8aca40e33f3153a0285e16b835e4af7237
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.4.38-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:4cfa64eee53cd83746444d308daf7d195fe13b0a10bb87dd124389849b17d427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204925366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60ccbb5afcc107eec5ea013360bfb8e00307a9b682378d281440e3d75f59e00a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.5.4.38
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566bb5305f1ad530116b3d87aef49f9c9285be8efc8b4ee589521fd6a890c926`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 7.2 MB (7151703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab249ebf6595eb4c777726f438316ce6d6f047eef8d7b1582914266ad523ad21`  
		Last Modified: Fri, 27 Jun 2025 21:49:57 GMT  
		Size: 167.4 MB (167370411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f3884935fe25d86737352a1d65a0159a3c336ec68be36e6a303ba62357f7a9`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d79771ae5550a8d3b6db26b0c500829b466951e01a53881a92894492b2ebb65`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd10851e3462f8d5b64dc30c65d245b95f1a86cf87f347e8cf0d8d9554f9924f`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f20a0138f6c07af47ae0a24abdcd60cd56cde7fc11a6318e6d83bbee2ca2f0`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82912db37c2e5044c9d13a9dbbd3bb06d23c507152c22444327cc17d073c85b5`  
		Last Modified: Fri, 27 Jun 2025 18:51:32 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.4.38-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:780c69edaeafef43fc4dff9e6331109ad097efb8ceffa47d0ea0c650ba92e62f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e269b7df1f9ab1b7c9a530e18d2c85a932200881b3418e374ae91233d9f42ea`

```dockerfile
```

-	Layers:
	-	`sha256:81dd76ba77ac4686a5d0c1bb5b27a1d5469e543bf808b3fdd15f161368913118`  
		Last Modified: Fri, 27 Jun 2025 21:49:36 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.4.38-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1b584caa772022abc093e5fb7f9a659737848f71f16fb53263a449e46fb4e60e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 MB (191498689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff8492b23c38f0c70b3f0c08b0cd4c680e3097f2c4e3686c9d1d19106af89e9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.5.4.38
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a23662fc50e497af13cba7782f06ab2fa94fbce9a6a450a4599446a17c308`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b787bf45549031cf5fd67d27c5c27f2b5ffc1e42937525cbf567fd28d58402`  
		Last Modified: Fri, 27 Jun 2025 21:49:57 GMT  
		Size: 156.1 MB (156144987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d96597c07858324dcb0dca879763024909cfb82b400f632adbcfb7d231816a9`  
		Last Modified: Fri, 27 Jun 2025 18:51:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085971706f494387be02045cb8557c22ee8db89820676c866e73113d18f96190`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdc5a9ef40188972e6405398cd83343004093bba9366b8c3717823c04f78b8c`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3f21e988cecec54e423de032ff28e427e9d4fd9227ca7e9725c5c76fd992af`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1414ea3cf5e1053fa4476294561b8370bd1e1669cab5b44b519b967c94209d22`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.4.38-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:025448e9040e9eee2f2d52ba663099cdf9bbdc0d604409f530ae9cf0f4127a08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e508646942141e611337d5994d21a09cf7ef8a2e8758b679168135afd5f57470`

```dockerfile
```

-	Layers:
	-	`sha256:286031c4818828028980b463d4f7af149d43296b7aea3ecced9e349d38bc7496`  
		Last Modified: Fri, 27 Jun 2025 21:49:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6`

```console
$ docker pull clickhouse@sha256:df49bca2d1688a5af1c3aeab30d2c38862cefd070dac22c97718c9bf7aedfa5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:99ed2b1dba4cc9734d8dee76d79f87bc8a3e21de5061d18330eef1ac6878ede2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211940872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53127eee9288c417f444212309f298f8a4d370a8ff4387cb3c455ea8082c9c07`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dfab5ffcdbd95d204bf6b0c80675c87106d65bb71de3c9238de91c40653cb7`  
		Last Modified: Fri, 27 Jun 2025 18:50:44 GMT  
		Size: 7.2 MB (7151713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f1eb8cfe1176a0c07d1652c7f046eaab4eae9fd070ec710382d1c9f9365592`  
		Last Modified: Fri, 27 Jun 2025 21:50:12 GMT  
		Size: 174.4 MB (174386128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cbf3424a2be88498dbc14f956dc243226a5dd23390f72f2e5d601198ed6d1d`  
		Last Modified: Fri, 27 Jun 2025 18:50:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb07ee1d4a69d341e3cd307048abe6afc9fbca4c908aa58b582dd8cfcdbb102`  
		Last Modified: Fri, 27 Jun 2025 18:50:48 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1215c6aa95a58eadc45ba360ed40b2582b2a6b27aa30007c8e36080ab3c664`  
		Last Modified: Fri, 27 Jun 2025 18:50:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71182a3098e14a40071601be4dcdec0cae88166d0da749a7b68d8f06eccb5b3`  
		Last Modified: Fri, 27 Jun 2025 18:50:50 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcb0d241f708312ca9f96bb05eb80bf1f37451489cf787c81a4e9794126c970`  
		Last Modified: Fri, 27 Jun 2025 18:50:51 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b6328412ec06d3ad804cb46359a4f6283b084659f40aaa67fe81697c8b127dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2956d2381c0038947b19306c3753514c86a9d021a7c67bcc8126717f53c22f7a`

```dockerfile
```

-	Layers:
	-	`sha256:df18c2664ab153a1631da1c1a4988aa20b448a28edee768fa0737ab06c2e6e1e`  
		Last Modified: Fri, 27 Jun 2025 21:49:48 GMT  
		Size: 25.9 KB (25899 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f450cd04fb9fd08fcdac7c8ee07934702d900e7f581e04b3bb53815fd1fc0a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198098606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552e1cc653076f052f6facd2a387f4a3b2f40d2fb9e90fc968dc8969b53979d0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb00be261dc49fdcd62ac41ed9430b9ee0f6690f5260504a62274f45722d8c8`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da9bf2cb5a2d06588595b87ea23dc0d4117a30d4136939e1835f62053599693`  
		Last Modified: Fri, 27 Jun 2025 21:50:05 GMT  
		Size: 162.7 MB (162745108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae9656ff9be3cf66263560f8c5ac009aa607951d89f4dd3b8f0047374e06974`  
		Last Modified: Fri, 27 Jun 2025 18:50:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6edf34796e4c16289b66e937e1d3c119270da713f41e6c06493973c95421837`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d943ca5af40e7591490c1b20621a39f7d6877f7a1681399d99949baa07dd766`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fc9024c03c4dfd5e538377d5034046f0c26bc120ddad806a88ab22bce839b0`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc4608669d6cefb7b892b0906d5abab8574ad2b775a54b5db710cadbb8afeb`  
		Last Modified: Fri, 27 Jun 2025 18:50:53 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:101c9469dde845c11b31be9321002444305fbbdf54ac4cba0e788539db5b8389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85e51f6259463822ccf7640e0c6288657bd756a03c7304748adf126201ddcb1`

```dockerfile
```

-	Layers:
	-	`sha256:c9a46f7ce9c1cd71db98d1d4752bc9c192e6aeb447b5d07058ef989dea936933`  
		Last Modified: Fri, 27 Jun 2025 21:49:51 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6-jammy`

```console
$ docker pull clickhouse@sha256:df49bca2d1688a5af1c3aeab30d2c38862cefd070dac22c97718c9bf7aedfa5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:99ed2b1dba4cc9734d8dee76d79f87bc8a3e21de5061d18330eef1ac6878ede2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211940872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53127eee9288c417f444212309f298f8a4d370a8ff4387cb3c455ea8082c9c07`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dfab5ffcdbd95d204bf6b0c80675c87106d65bb71de3c9238de91c40653cb7`  
		Last Modified: Fri, 27 Jun 2025 18:50:44 GMT  
		Size: 7.2 MB (7151713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f1eb8cfe1176a0c07d1652c7f046eaab4eae9fd070ec710382d1c9f9365592`  
		Last Modified: Fri, 27 Jun 2025 21:50:12 GMT  
		Size: 174.4 MB (174386128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cbf3424a2be88498dbc14f956dc243226a5dd23390f72f2e5d601198ed6d1d`  
		Last Modified: Fri, 27 Jun 2025 18:50:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb07ee1d4a69d341e3cd307048abe6afc9fbca4c908aa58b582dd8cfcdbb102`  
		Last Modified: Fri, 27 Jun 2025 18:50:48 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1215c6aa95a58eadc45ba360ed40b2582b2a6b27aa30007c8e36080ab3c664`  
		Last Modified: Fri, 27 Jun 2025 18:50:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71182a3098e14a40071601be4dcdec0cae88166d0da749a7b68d8f06eccb5b3`  
		Last Modified: Fri, 27 Jun 2025 18:50:50 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcb0d241f708312ca9f96bb05eb80bf1f37451489cf787c81a4e9794126c970`  
		Last Modified: Fri, 27 Jun 2025 18:50:51 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b6328412ec06d3ad804cb46359a4f6283b084659f40aaa67fe81697c8b127dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2956d2381c0038947b19306c3753514c86a9d021a7c67bcc8126717f53c22f7a`

```dockerfile
```

-	Layers:
	-	`sha256:df18c2664ab153a1631da1c1a4988aa20b448a28edee768fa0737ab06c2e6e1e`  
		Last Modified: Fri, 27 Jun 2025 21:49:48 GMT  
		Size: 25.9 KB (25899 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f450cd04fb9fd08fcdac7c8ee07934702d900e7f581e04b3bb53815fd1fc0a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198098606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552e1cc653076f052f6facd2a387f4a3b2f40d2fb9e90fc968dc8969b53979d0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb00be261dc49fdcd62ac41ed9430b9ee0f6690f5260504a62274f45722d8c8`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da9bf2cb5a2d06588595b87ea23dc0d4117a30d4136939e1835f62053599693`  
		Last Modified: Fri, 27 Jun 2025 21:50:05 GMT  
		Size: 162.7 MB (162745108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae9656ff9be3cf66263560f8c5ac009aa607951d89f4dd3b8f0047374e06974`  
		Last Modified: Fri, 27 Jun 2025 18:50:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6edf34796e4c16289b66e937e1d3c119270da713f41e6c06493973c95421837`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d943ca5af40e7591490c1b20621a39f7d6877f7a1681399d99949baa07dd766`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fc9024c03c4dfd5e538377d5034046f0c26bc120ddad806a88ab22bce839b0`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc4608669d6cefb7b892b0906d5abab8574ad2b775a54b5db710cadbb8afeb`  
		Last Modified: Fri, 27 Jun 2025 18:50:53 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:101c9469dde845c11b31be9321002444305fbbdf54ac4cba0e788539db5b8389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85e51f6259463822ccf7640e0c6288657bd756a03c7304748adf126201ddcb1`

```dockerfile
```

-	Layers:
	-	`sha256:c9a46f7ce9c1cd71db98d1d4752bc9c192e6aeb447b5d07058ef989dea936933`  
		Last Modified: Fri, 27 Jun 2025 21:49:51 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.1`

```console
$ docker pull clickhouse@sha256:df49bca2d1688a5af1c3aeab30d2c38862cefd070dac22c97718c9bf7aedfa5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:99ed2b1dba4cc9734d8dee76d79f87bc8a3e21de5061d18330eef1ac6878ede2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211940872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53127eee9288c417f444212309f298f8a4d370a8ff4387cb3c455ea8082c9c07`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dfab5ffcdbd95d204bf6b0c80675c87106d65bb71de3c9238de91c40653cb7`  
		Last Modified: Fri, 27 Jun 2025 18:50:44 GMT  
		Size: 7.2 MB (7151713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f1eb8cfe1176a0c07d1652c7f046eaab4eae9fd070ec710382d1c9f9365592`  
		Last Modified: Fri, 27 Jun 2025 21:50:12 GMT  
		Size: 174.4 MB (174386128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cbf3424a2be88498dbc14f956dc243226a5dd23390f72f2e5d601198ed6d1d`  
		Last Modified: Fri, 27 Jun 2025 18:50:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb07ee1d4a69d341e3cd307048abe6afc9fbca4c908aa58b582dd8cfcdbb102`  
		Last Modified: Fri, 27 Jun 2025 18:50:48 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1215c6aa95a58eadc45ba360ed40b2582b2a6b27aa30007c8e36080ab3c664`  
		Last Modified: Fri, 27 Jun 2025 18:50:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71182a3098e14a40071601be4dcdec0cae88166d0da749a7b68d8f06eccb5b3`  
		Last Modified: Fri, 27 Jun 2025 18:50:50 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcb0d241f708312ca9f96bb05eb80bf1f37451489cf787c81a4e9794126c970`  
		Last Modified: Fri, 27 Jun 2025 18:50:51 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b6328412ec06d3ad804cb46359a4f6283b084659f40aaa67fe81697c8b127dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2956d2381c0038947b19306c3753514c86a9d021a7c67bcc8126717f53c22f7a`

```dockerfile
```

-	Layers:
	-	`sha256:df18c2664ab153a1631da1c1a4988aa20b448a28edee768fa0737ab06c2e6e1e`  
		Last Modified: Fri, 27 Jun 2025 21:49:48 GMT  
		Size: 25.9 KB (25899 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f450cd04fb9fd08fcdac7c8ee07934702d900e7f581e04b3bb53815fd1fc0a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198098606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552e1cc653076f052f6facd2a387f4a3b2f40d2fb9e90fc968dc8969b53979d0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb00be261dc49fdcd62ac41ed9430b9ee0f6690f5260504a62274f45722d8c8`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da9bf2cb5a2d06588595b87ea23dc0d4117a30d4136939e1835f62053599693`  
		Last Modified: Fri, 27 Jun 2025 21:50:05 GMT  
		Size: 162.7 MB (162745108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae9656ff9be3cf66263560f8c5ac009aa607951d89f4dd3b8f0047374e06974`  
		Last Modified: Fri, 27 Jun 2025 18:50:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6edf34796e4c16289b66e937e1d3c119270da713f41e6c06493973c95421837`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d943ca5af40e7591490c1b20621a39f7d6877f7a1681399d99949baa07dd766`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fc9024c03c4dfd5e538377d5034046f0c26bc120ddad806a88ab22bce839b0`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc4608669d6cefb7b892b0906d5abab8574ad2b775a54b5db710cadbb8afeb`  
		Last Modified: Fri, 27 Jun 2025 18:50:53 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:101c9469dde845c11b31be9321002444305fbbdf54ac4cba0e788539db5b8389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85e51f6259463822ccf7640e0c6288657bd756a03c7304748adf126201ddcb1`

```dockerfile
```

-	Layers:
	-	`sha256:c9a46f7ce9c1cd71db98d1d4752bc9c192e6aeb447b5d07058ef989dea936933`  
		Last Modified: Fri, 27 Jun 2025 21:49:51 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.1-jammy`

```console
$ docker pull clickhouse@sha256:df49bca2d1688a5af1c3aeab30d2c38862cefd070dac22c97718c9bf7aedfa5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:99ed2b1dba4cc9734d8dee76d79f87bc8a3e21de5061d18330eef1ac6878ede2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211940872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53127eee9288c417f444212309f298f8a4d370a8ff4387cb3c455ea8082c9c07`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dfab5ffcdbd95d204bf6b0c80675c87106d65bb71de3c9238de91c40653cb7`  
		Last Modified: Fri, 27 Jun 2025 18:50:44 GMT  
		Size: 7.2 MB (7151713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f1eb8cfe1176a0c07d1652c7f046eaab4eae9fd070ec710382d1c9f9365592`  
		Last Modified: Fri, 27 Jun 2025 21:50:12 GMT  
		Size: 174.4 MB (174386128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cbf3424a2be88498dbc14f956dc243226a5dd23390f72f2e5d601198ed6d1d`  
		Last Modified: Fri, 27 Jun 2025 18:50:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb07ee1d4a69d341e3cd307048abe6afc9fbca4c908aa58b582dd8cfcdbb102`  
		Last Modified: Fri, 27 Jun 2025 18:50:48 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1215c6aa95a58eadc45ba360ed40b2582b2a6b27aa30007c8e36080ab3c664`  
		Last Modified: Fri, 27 Jun 2025 18:50:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71182a3098e14a40071601be4dcdec0cae88166d0da749a7b68d8f06eccb5b3`  
		Last Modified: Fri, 27 Jun 2025 18:50:50 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcb0d241f708312ca9f96bb05eb80bf1f37451489cf787c81a4e9794126c970`  
		Last Modified: Fri, 27 Jun 2025 18:50:51 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b6328412ec06d3ad804cb46359a4f6283b084659f40aaa67fe81697c8b127dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2956d2381c0038947b19306c3753514c86a9d021a7c67bcc8126717f53c22f7a`

```dockerfile
```

-	Layers:
	-	`sha256:df18c2664ab153a1631da1c1a4988aa20b448a28edee768fa0737ab06c2e6e1e`  
		Last Modified: Fri, 27 Jun 2025 21:49:48 GMT  
		Size: 25.9 KB (25899 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f450cd04fb9fd08fcdac7c8ee07934702d900e7f581e04b3bb53815fd1fc0a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198098606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552e1cc653076f052f6facd2a387f4a3b2f40d2fb9e90fc968dc8969b53979d0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb00be261dc49fdcd62ac41ed9430b9ee0f6690f5260504a62274f45722d8c8`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da9bf2cb5a2d06588595b87ea23dc0d4117a30d4136939e1835f62053599693`  
		Last Modified: Fri, 27 Jun 2025 21:50:05 GMT  
		Size: 162.7 MB (162745108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae9656ff9be3cf66263560f8c5ac009aa607951d89f4dd3b8f0047374e06974`  
		Last Modified: Fri, 27 Jun 2025 18:50:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6edf34796e4c16289b66e937e1d3c119270da713f41e6c06493973c95421837`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d943ca5af40e7591490c1b20621a39f7d6877f7a1681399d99949baa07dd766`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fc9024c03c4dfd5e538377d5034046f0c26bc120ddad806a88ab22bce839b0`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc4608669d6cefb7b892b0906d5abab8574ad2b775a54b5db710cadbb8afeb`  
		Last Modified: Fri, 27 Jun 2025 18:50:53 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:101c9469dde845c11b31be9321002444305fbbdf54ac4cba0e788539db5b8389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85e51f6259463822ccf7640e0c6288657bd756a03c7304748adf126201ddcb1`

```dockerfile
```

-	Layers:
	-	`sha256:c9a46f7ce9c1cd71db98d1d4752bc9c192e6aeb447b5d07058ef989dea936933`  
		Last Modified: Fri, 27 Jun 2025 21:49:51 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.1.3206`

```console
$ docker pull clickhouse@sha256:df49bca2d1688a5af1c3aeab30d2c38862cefd070dac22c97718c9bf7aedfa5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.1.3206` - linux; amd64

```console
$ docker pull clickhouse@sha256:99ed2b1dba4cc9734d8dee76d79f87bc8a3e21de5061d18330eef1ac6878ede2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211940872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53127eee9288c417f444212309f298f8a4d370a8ff4387cb3c455ea8082c9c07`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dfab5ffcdbd95d204bf6b0c80675c87106d65bb71de3c9238de91c40653cb7`  
		Last Modified: Fri, 27 Jun 2025 18:50:44 GMT  
		Size: 7.2 MB (7151713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f1eb8cfe1176a0c07d1652c7f046eaab4eae9fd070ec710382d1c9f9365592`  
		Last Modified: Fri, 27 Jun 2025 21:50:12 GMT  
		Size: 174.4 MB (174386128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cbf3424a2be88498dbc14f956dc243226a5dd23390f72f2e5d601198ed6d1d`  
		Last Modified: Fri, 27 Jun 2025 18:50:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb07ee1d4a69d341e3cd307048abe6afc9fbca4c908aa58b582dd8cfcdbb102`  
		Last Modified: Fri, 27 Jun 2025 18:50:48 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1215c6aa95a58eadc45ba360ed40b2582b2a6b27aa30007c8e36080ab3c664`  
		Last Modified: Fri, 27 Jun 2025 18:50:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71182a3098e14a40071601be4dcdec0cae88166d0da749a7b68d8f06eccb5b3`  
		Last Modified: Fri, 27 Jun 2025 18:50:50 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcb0d241f708312ca9f96bb05eb80bf1f37451489cf787c81a4e9794126c970`  
		Last Modified: Fri, 27 Jun 2025 18:50:51 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.1.3206` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b6328412ec06d3ad804cb46359a4f6283b084659f40aaa67fe81697c8b127dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2956d2381c0038947b19306c3753514c86a9d021a7c67bcc8126717f53c22f7a`

```dockerfile
```

-	Layers:
	-	`sha256:df18c2664ab153a1631da1c1a4988aa20b448a28edee768fa0737ab06c2e6e1e`  
		Last Modified: Fri, 27 Jun 2025 21:49:48 GMT  
		Size: 25.9 KB (25899 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.1.3206` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f450cd04fb9fd08fcdac7c8ee07934702d900e7f581e04b3bb53815fd1fc0a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198098606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552e1cc653076f052f6facd2a387f4a3b2f40d2fb9e90fc968dc8969b53979d0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb00be261dc49fdcd62ac41ed9430b9ee0f6690f5260504a62274f45722d8c8`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da9bf2cb5a2d06588595b87ea23dc0d4117a30d4136939e1835f62053599693`  
		Last Modified: Fri, 27 Jun 2025 21:50:05 GMT  
		Size: 162.7 MB (162745108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae9656ff9be3cf66263560f8c5ac009aa607951d89f4dd3b8f0047374e06974`  
		Last Modified: Fri, 27 Jun 2025 18:50:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6edf34796e4c16289b66e937e1d3c119270da713f41e6c06493973c95421837`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d943ca5af40e7591490c1b20621a39f7d6877f7a1681399d99949baa07dd766`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fc9024c03c4dfd5e538377d5034046f0c26bc120ddad806a88ab22bce839b0`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc4608669d6cefb7b892b0906d5abab8574ad2b775a54b5db710cadbb8afeb`  
		Last Modified: Fri, 27 Jun 2025 18:50:53 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.1.3206` - unknown; unknown

```console
$ docker pull clickhouse@sha256:101c9469dde845c11b31be9321002444305fbbdf54ac4cba0e788539db5b8389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85e51f6259463822ccf7640e0c6288657bd756a03c7304748adf126201ddcb1`

```dockerfile
```

-	Layers:
	-	`sha256:c9a46f7ce9c1cd71db98d1d4752bc9c192e6aeb447b5d07058ef989dea936933`  
		Last Modified: Fri, 27 Jun 2025 21:49:51 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.1.3206-jammy`

```console
$ docker pull clickhouse@sha256:df49bca2d1688a5af1c3aeab30d2c38862cefd070dac22c97718c9bf7aedfa5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.1.3206-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:99ed2b1dba4cc9734d8dee76d79f87bc8a3e21de5061d18330eef1ac6878ede2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211940872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53127eee9288c417f444212309f298f8a4d370a8ff4387cb3c455ea8082c9c07`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dfab5ffcdbd95d204bf6b0c80675c87106d65bb71de3c9238de91c40653cb7`  
		Last Modified: Fri, 27 Jun 2025 18:50:44 GMT  
		Size: 7.2 MB (7151713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f1eb8cfe1176a0c07d1652c7f046eaab4eae9fd070ec710382d1c9f9365592`  
		Last Modified: Fri, 27 Jun 2025 21:50:12 GMT  
		Size: 174.4 MB (174386128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cbf3424a2be88498dbc14f956dc243226a5dd23390f72f2e5d601198ed6d1d`  
		Last Modified: Fri, 27 Jun 2025 18:50:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb07ee1d4a69d341e3cd307048abe6afc9fbca4c908aa58b582dd8cfcdbb102`  
		Last Modified: Fri, 27 Jun 2025 18:50:48 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1215c6aa95a58eadc45ba360ed40b2582b2a6b27aa30007c8e36080ab3c664`  
		Last Modified: Fri, 27 Jun 2025 18:50:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71182a3098e14a40071601be4dcdec0cae88166d0da749a7b68d8f06eccb5b3`  
		Last Modified: Fri, 27 Jun 2025 18:50:50 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcb0d241f708312ca9f96bb05eb80bf1f37451489cf787c81a4e9794126c970`  
		Last Modified: Fri, 27 Jun 2025 18:50:51 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.1.3206-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b6328412ec06d3ad804cb46359a4f6283b084659f40aaa67fe81697c8b127dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2956d2381c0038947b19306c3753514c86a9d021a7c67bcc8126717f53c22f7a`

```dockerfile
```

-	Layers:
	-	`sha256:df18c2664ab153a1631da1c1a4988aa20b448a28edee768fa0737ab06c2e6e1e`  
		Last Modified: Fri, 27 Jun 2025 21:49:48 GMT  
		Size: 25.9 KB (25899 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.1.3206-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f450cd04fb9fd08fcdac7c8ee07934702d900e7f581e04b3bb53815fd1fc0a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198098606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552e1cc653076f052f6facd2a387f4a3b2f40d2fb9e90fc968dc8969b53979d0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb00be261dc49fdcd62ac41ed9430b9ee0f6690f5260504a62274f45722d8c8`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da9bf2cb5a2d06588595b87ea23dc0d4117a30d4136939e1835f62053599693`  
		Last Modified: Fri, 27 Jun 2025 21:50:05 GMT  
		Size: 162.7 MB (162745108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae9656ff9be3cf66263560f8c5ac009aa607951d89f4dd3b8f0047374e06974`  
		Last Modified: Fri, 27 Jun 2025 18:50:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6edf34796e4c16289b66e937e1d3c119270da713f41e6c06493973c95421837`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d943ca5af40e7591490c1b20621a39f7d6877f7a1681399d99949baa07dd766`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fc9024c03c4dfd5e538377d5034046f0c26bc120ddad806a88ab22bce839b0`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc4608669d6cefb7b892b0906d5abab8574ad2b775a54b5db710cadbb8afeb`  
		Last Modified: Fri, 27 Jun 2025 18:50:53 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.1.3206-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:101c9469dde845c11b31be9321002444305fbbdf54ac4cba0e788539db5b8389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85e51f6259463822ccf7640e0c6288657bd756a03c7304748adf126201ddcb1`

```dockerfile
```

-	Layers:
	-	`sha256:c9a46f7ce9c1cd71db98d1d4752bc9c192e6aeb447b5d07058ef989dea936933`  
		Last Modified: Fri, 27 Jun 2025 21:49:51 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:df49bca2d1688a5af1c3aeab30d2c38862cefd070dac22c97718c9bf7aedfa5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:99ed2b1dba4cc9734d8dee76d79f87bc8a3e21de5061d18330eef1ac6878ede2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211940872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53127eee9288c417f444212309f298f8a4d370a8ff4387cb3c455ea8082c9c07`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dfab5ffcdbd95d204bf6b0c80675c87106d65bb71de3c9238de91c40653cb7`  
		Last Modified: Fri, 27 Jun 2025 18:50:44 GMT  
		Size: 7.2 MB (7151713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f1eb8cfe1176a0c07d1652c7f046eaab4eae9fd070ec710382d1c9f9365592`  
		Last Modified: Fri, 27 Jun 2025 21:50:12 GMT  
		Size: 174.4 MB (174386128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cbf3424a2be88498dbc14f956dc243226a5dd23390f72f2e5d601198ed6d1d`  
		Last Modified: Fri, 27 Jun 2025 18:50:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb07ee1d4a69d341e3cd307048abe6afc9fbca4c908aa58b582dd8cfcdbb102`  
		Last Modified: Fri, 27 Jun 2025 18:50:48 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1215c6aa95a58eadc45ba360ed40b2582b2a6b27aa30007c8e36080ab3c664`  
		Last Modified: Fri, 27 Jun 2025 18:50:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71182a3098e14a40071601be4dcdec0cae88166d0da749a7b68d8f06eccb5b3`  
		Last Modified: Fri, 27 Jun 2025 18:50:50 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcb0d241f708312ca9f96bb05eb80bf1f37451489cf787c81a4e9794126c970`  
		Last Modified: Fri, 27 Jun 2025 18:50:51 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b6328412ec06d3ad804cb46359a4f6283b084659f40aaa67fe81697c8b127dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2956d2381c0038947b19306c3753514c86a9d021a7c67bcc8126717f53c22f7a`

```dockerfile
```

-	Layers:
	-	`sha256:df18c2664ab153a1631da1c1a4988aa20b448a28edee768fa0737ab06c2e6e1e`  
		Last Modified: Fri, 27 Jun 2025 21:49:48 GMT  
		Size: 25.9 KB (25899 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f450cd04fb9fd08fcdac7c8ee07934702d900e7f581e04b3bb53815fd1fc0a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198098606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552e1cc653076f052f6facd2a387f4a3b2f40d2fb9e90fc968dc8969b53979d0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb00be261dc49fdcd62ac41ed9430b9ee0f6690f5260504a62274f45722d8c8`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da9bf2cb5a2d06588595b87ea23dc0d4117a30d4136939e1835f62053599693`  
		Last Modified: Fri, 27 Jun 2025 21:50:05 GMT  
		Size: 162.7 MB (162745108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae9656ff9be3cf66263560f8c5ac009aa607951d89f4dd3b8f0047374e06974`  
		Last Modified: Fri, 27 Jun 2025 18:50:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6edf34796e4c16289b66e937e1d3c119270da713f41e6c06493973c95421837`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d943ca5af40e7591490c1b20621a39f7d6877f7a1681399d99949baa07dd766`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fc9024c03c4dfd5e538377d5034046f0c26bc120ddad806a88ab22bce839b0`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc4608669d6cefb7b892b0906d5abab8574ad2b775a54b5db710cadbb8afeb`  
		Last Modified: Fri, 27 Jun 2025 18:50:53 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:101c9469dde845c11b31be9321002444305fbbdf54ac4cba0e788539db5b8389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85e51f6259463822ccf7640e0c6288657bd756a03c7304748adf126201ddcb1`

```dockerfile
```

-	Layers:
	-	`sha256:c9a46f7ce9c1cd71db98d1d4752bc9c192e6aeb447b5d07058ef989dea936933`  
		Last Modified: Fri, 27 Jun 2025 21:49:51 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:df49bca2d1688a5af1c3aeab30d2c38862cefd070dac22c97718c9bf7aedfa5f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:99ed2b1dba4cc9734d8dee76d79f87bc8a3e21de5061d18330eef1ac6878ede2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.9 MB (211940872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53127eee9288c417f444212309f298f8a4d370a8ff4387cb3c455ea8082c9c07`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dfab5ffcdbd95d204bf6b0c80675c87106d65bb71de3c9238de91c40653cb7`  
		Last Modified: Fri, 27 Jun 2025 18:50:44 GMT  
		Size: 7.2 MB (7151713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f1eb8cfe1176a0c07d1652c7f046eaab4eae9fd070ec710382d1c9f9365592`  
		Last Modified: Fri, 27 Jun 2025 21:50:12 GMT  
		Size: 174.4 MB (174386128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cbf3424a2be88498dbc14f956dc243226a5dd23390f72f2e5d601198ed6d1d`  
		Last Modified: Fri, 27 Jun 2025 18:50:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb07ee1d4a69d341e3cd307048abe6afc9fbca4c908aa58b582dd8cfcdbb102`  
		Last Modified: Fri, 27 Jun 2025 18:50:48 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1215c6aa95a58eadc45ba360ed40b2582b2a6b27aa30007c8e36080ab3c664`  
		Last Modified: Fri, 27 Jun 2025 18:50:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e71182a3098e14a40071601be4dcdec0cae88166d0da749a7b68d8f06eccb5b3`  
		Last Modified: Fri, 27 Jun 2025 18:50:50 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcb0d241f708312ca9f96bb05eb80bf1f37451489cf787c81a4e9794126c970`  
		Last Modified: Fri, 27 Jun 2025 18:50:51 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b6328412ec06d3ad804cb46359a4f6283b084659f40aaa67fe81697c8b127dbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2956d2381c0038947b19306c3753514c86a9d021a7c67bcc8126717f53c22f7a`

```dockerfile
```

-	Layers:
	-	`sha256:df18c2664ab153a1631da1c1a4988aa20b448a28edee768fa0737ab06c2e6e1e`  
		Last Modified: Fri, 27 Jun 2025 21:49:48 GMT  
		Size: 25.9 KB (25899 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f450cd04fb9fd08fcdac7c8ee07934702d900e7f581e04b3bb53815fd1fc0a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.1 MB (198098606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552e1cc653076f052f6facd2a387f4a3b2f40d2fb9e90fc968dc8969b53979d0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.6.1.3206
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.1.3206 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb00be261dc49fdcd62ac41ed9430b9ee0f6690f5260504a62274f45722d8c8`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 7.1 MB (7127897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da9bf2cb5a2d06588595b87ea23dc0d4117a30d4136939e1835f62053599693`  
		Last Modified: Fri, 27 Jun 2025 21:50:05 GMT  
		Size: 162.7 MB (162745108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae9656ff9be3cf66263560f8c5ac009aa607951d89f4dd3b8f0047374e06974`  
		Last Modified: Fri, 27 Jun 2025 18:50:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6edf34796e4c16289b66e937e1d3c119270da713f41e6c06493973c95421837`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d943ca5af40e7591490c1b20621a39f7d6877f7a1681399d99949baa07dd766`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fc9024c03c4dfd5e538377d5034046f0c26bc120ddad806a88ab22bce839b0`  
		Last Modified: Fri, 27 Jun 2025 18:50:52 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87fc4608669d6cefb7b892b0906d5abab8574ad2b775a54b5db710cadbb8afeb`  
		Last Modified: Fri, 27 Jun 2025 18:50:53 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:101c9469dde845c11b31be9321002444305fbbdf54ac4cba0e788539db5b8389
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c85e51f6259463822ccf7640e0c6288657bd756a03c7304748adf126201ddcb1`

```dockerfile
```

-	Layers:
	-	`sha256:c9a46f7ce9c1cd71db98d1d4752bc9c192e6aeb447b5d07058ef989dea936933`  
		Last Modified: Fri, 27 Jun 2025 21:49:51 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:309b9238691234e4ebb554afa227c0c6b29f169b4e4ce9a68e621db170f964bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:14cd358b4321c90949bdb82ef783d415b288f9e92e594d986b68c46fd1a08a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204656901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faf232a4b6a79ac8955e52df456718817dbd3f2831f8e4c67ffaa276a98aaff`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a89521c1cddce9e2b92a7eea7e2e26f08d9644f8280c2ffabc687ba59a380`  
		Last Modified: Fri, 27 Jun 2025 21:49:38 GMT  
		Size: 7.2 MB (7151605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f97b7e7c107f81c005662fac120035c32226b53ea2f331be0b7d28153bf19b`  
		Last Modified: Fri, 27 Jun 2025 21:49:45 GMT  
		Size: 167.1 MB (167102045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd9e5194ca4898b9a81e75384174a506b3f40f52f3f9a199e61d0bf85ca90d`  
		Last Modified: Fri, 27 Jun 2025 19:03:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a196f26d3fcac6764f1e0cf39781226cf953be5d0859ae1bb2c0bf49dd8bce9e`  
		Last Modified: Fri, 27 Jun 2025 19:03:06 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5445346ace8b927a19dafce4f348e6c2e7eb73610a91488401afec069b151273`  
		Last Modified: Fri, 27 Jun 2025 19:03:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9903e3e75a91e7f238e84fedac46adf1fd322f6dc7d7e24848bdabcce95235f8`  
		Last Modified: Fri, 27 Jun 2025 19:03:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd49a017f1b4781b5e10d0db53ab4474bf9c9cc6736e3334f0324b86276b5421`  
		Last Modified: Fri, 27 Jun 2025 19:03:13 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9ba832181b9f6be8f5f217385d87d47835fd535412a917f140dc7d836051728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0e364a78dad8826a0d237b11ab93f52cdb6e29db46b4a8fd411e98d9115eae`

```dockerfile
```

-	Layers:
	-	`sha256:e65e118aeb542d30c362f3f00125c47cc357f7b682a949fa6a31c1a81aef9f24`  
		Last Modified: Fri, 27 Jun 2025 21:49:21 GMT  
		Size: 25.9 KB (25886 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:43fc7421731f68ef1f15e7c1cd4bd61b89cdef5b0993fbdbd9df1e7f1daf616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192176647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891f121ead07341bdb77db2b6669a46ac9e41676f06eda3133e8a6abc5549437`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a23662fc50e497af13cba7782f06ab2fa94fbce9a6a450a4599446a17c308`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24538160e575723afc9dba473de81c59b5c7b3bf95ff19c0c089485e11b6462`  
		Last Modified: Fri, 27 Jun 2025 21:49:44 GMT  
		Size: 156.8 MB (156822945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e291bf0ee5766818d7442c70ca06b7b7bf86fba4f0a30e2fe86f93975e05a037`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7c8e256097ad6fc4e0dfce399adae584bda2e2343d1086fb20e60d70ce9da8`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae1bee24f98056e82d5bdeaa1e269dcfb9e897edd988423740ca2134a29813`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e51fc7981aa274185d3cf9b17706bbf37b8d8ad2e3dfa2f59e3ad3b602abb7`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06a605c0c7f1af061896c9aa90bb26533052b7457a899fb8665f7ea011bba82`  
		Last Modified: Fri, 27 Jun 2025 18:52:14 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6d521afb29c0fd95122117051f94e14d57a940d3c044f6f052844dc703faea0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f1d21463d7b9c00ea7771697266590213c3e990f93b410feedacfa3af6ccb`

```dockerfile
```

-	Layers:
	-	`sha256:e9ba2be1ed520eb11683202ea13e7f9e33237bdfd211b0d1b3912ab3180dbcb7`  
		Last Modified: Fri, 27 Jun 2025 21:49:24 GMT  
		Size: 26.1 KB (26098 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:309b9238691234e4ebb554afa227c0c6b29f169b4e4ce9a68e621db170f964bb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:14cd358b4321c90949bdb82ef783d415b288f9e92e594d986b68c46fd1a08a4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204656901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3faf232a4b6a79ac8955e52df456718817dbd3f2831f8e4c67ffaa276a98aaff`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:30:42 GMT
ARG RELEASE
# Fri, 30 May 2025 22:30:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:30:42 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:30:45 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 30 May 2025 22:30:45 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752a89521c1cddce9e2b92a7eea7e2e26f08d9644f8280c2ffabc687ba59a380`  
		Last Modified: Fri, 27 Jun 2025 21:49:38 GMT  
		Size: 7.2 MB (7151605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f97b7e7c107f81c005662fac120035c32226b53ea2f331be0b7d28153bf19b`  
		Last Modified: Fri, 27 Jun 2025 21:49:45 GMT  
		Size: 167.1 MB (167102045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bd9e5194ca4898b9a81e75384174a506b3f40f52f3f9a199e61d0bf85ca90d`  
		Last Modified: Fri, 27 Jun 2025 19:03:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a196f26d3fcac6764f1e0cf39781226cf953be5d0859ae1bb2c0bf49dd8bce9e`  
		Last Modified: Fri, 27 Jun 2025 19:03:06 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5445346ace8b927a19dafce4f348e6c2e7eb73610a91488401afec069b151273`  
		Last Modified: Fri, 27 Jun 2025 19:03:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9903e3e75a91e7f238e84fedac46adf1fd322f6dc7d7e24848bdabcce95235f8`  
		Last Modified: Fri, 27 Jun 2025 19:03:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd49a017f1b4781b5e10d0db53ab4474bf9c9cc6736e3334f0324b86276b5421`  
		Last Modified: Fri, 27 Jun 2025 19:03:13 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f9ba832181b9f6be8f5f217385d87d47835fd535412a917f140dc7d836051728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f0e364a78dad8826a0d237b11ab93f52cdb6e29db46b4a8fd411e98d9115eae`

```dockerfile
```

-	Layers:
	-	`sha256:e65e118aeb542d30c362f3f00125c47cc357f7b682a949fa6a31c1a81aef9f24`  
		Last Modified: Fri, 27 Jun 2025 21:49:21 GMT  
		Size: 25.9 KB (25886 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:43fc7421731f68ef1f15e7c1cd4bd61b89cdef5b0993fbdbd9df1e7f1daf616f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192176647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891f121ead07341bdb77db2b6669a46ac9e41676f06eda3133e8a6abc5549437`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 22:33:12 GMT
ARG RELEASE
# Fri, 30 May 2025 22:33:12 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 30 May 2025 22:33:12 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 30 May 2025 22:33:15 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 30 May 2025 22:33:15 GMT
CMD ["/bin/bash"]
# Fri, 27 Jun 2025 18:14:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 27 Jun 2025 18:14:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 27 Jun 2025 18:14:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 27 Jun 2025 18:14:04 GMT
ARG VERSION=25.3.4.190
# Fri, 27 Jun 2025 18:14:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 27 Jun 2025 18:14:04 GMT
ENV TZ=UTC
# Fri, 27 Jun 2025 18:14:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.4.190 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 27 Jun 2025 18:14:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 27 Jun 2025 18:14:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 27 Jun 2025 18:14:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 27 Jun 2025 18:14:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8a23662fc50e497af13cba7782f06ab2fa94fbce9a6a450a4599446a17c308`  
		Last Modified: Fri, 27 Jun 2025 18:51:24 GMT  
		Size: 7.1 MB (7127880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24538160e575723afc9dba473de81c59b5c7b3bf95ff19c0c089485e11b6462`  
		Last Modified: Fri, 27 Jun 2025 21:49:44 GMT  
		Size: 156.8 MB (156822945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e291bf0ee5766818d7442c70ca06b7b7bf86fba4f0a30e2fe86f93975e05a037`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7c8e256097ad6fc4e0dfce399adae584bda2e2343d1086fb20e60d70ce9da8`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ae1bee24f98056e82d5bdeaa1e269dcfb9e897edd988423740ca2134a29813`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e51fc7981aa274185d3cf9b17706bbf37b8d8ad2e3dfa2f59e3ad3b602abb7`  
		Last Modified: Fri, 27 Jun 2025 18:52:13 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06a605c0c7f1af061896c9aa90bb26533052b7457a899fb8665f7ea011bba82`  
		Last Modified: Fri, 27 Jun 2025 18:52:14 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6d521afb29c0fd95122117051f94e14d57a940d3c044f6f052844dc703faea0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5f1d21463d7b9c00ea7771697266590213c3e990f93b410feedacfa3af6ccb`

```dockerfile
```

-	Layers:
	-	`sha256:e9ba2be1ed520eb11683202ea13e7f9e33237bdfd211b0d1b3912ab3180dbcb7`  
		Last Modified: Fri, 27 Jun 2025 21:49:24 GMT  
		Size: 26.1 KB (26098 bytes)  
		MIME: application/vnd.in-toto+json
