<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:24`](#clickhouse24)
-	[`clickhouse:24-focal`](#clickhouse24-focal)
-	[`clickhouse:24.10`](#clickhouse2410)
-	[`clickhouse:24.10-focal`](#clickhouse2410-focal)
-	[`clickhouse:24.10.1`](#clickhouse24101)
-	[`clickhouse:24.10.1-focal`](#clickhouse24101-focal)
-	[`clickhouse:24.10.1.2812`](#clickhouse241012812)
-	[`clickhouse:24.10.1.2812-focal`](#clickhouse241012812-focal)
-	[`clickhouse:24.3`](#clickhouse243)
-	[`clickhouse:24.3-focal`](#clickhouse243-focal)
-	[`clickhouse:24.3.13`](#clickhouse24313)
-	[`clickhouse:24.3.13-focal`](#clickhouse24313-focal)
-	[`clickhouse:24.3.13.40`](#clickhouse2431340)
-	[`clickhouse:24.3.13.40-focal`](#clickhouse2431340-focal)
-	[`clickhouse:24.8`](#clickhouse248)
-	[`clickhouse:24.8-focal`](#clickhouse248-focal)
-	[`clickhouse:24.8.6`](#clickhouse2486)
-	[`clickhouse:24.8.6-focal`](#clickhouse2486-focal)
-	[`clickhouse:24.8.6.70`](#clickhouse248670)
-	[`clickhouse:24.8.6.70-focal`](#clickhouse248670-focal)
-	[`clickhouse:24.9`](#clickhouse249)
-	[`clickhouse:24.9-focal`](#clickhouse249-focal)
-	[`clickhouse:24.9.2`](#clickhouse2492)
-	[`clickhouse:24.9.2-focal`](#clickhouse2492-focal)
-	[`clickhouse:24.9.2.42`](#clickhouse249242)
-	[`clickhouse:24.9.2.42-focal`](#clickhouse249242-focal)
-	[`clickhouse:focal`](#clickhousefocal)
-	[`clickhouse:focal-lts`](#clickhousefocal-lts)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)

## `clickhouse:24`

```console
$ docker pull clickhouse@sha256:7bc9fa5ec703a95ffd5a2c6a271dab034aa0637dbc2fefbd5fc57e3283bec064
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24` - linux; amd64

```console
$ docker pull clickhouse@sha256:be2eb6602bb634c641a26de50062bc6db4a413fc5f8e2d30d69e63ae218c9300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180502273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780779b097fba8e76a39d39f0f34ce2e5bd628429919a69180f6c2f235a7e799`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111f8833bc453e9ec8c2ebf32ac32b825681a3b9b8e372c9e3398f52bb2d7bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 8.8 MB (8802605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c21f8f8706bb6e315bd1248a431189fb5403141581d2dd8c747495194028dc0`  
		Last Modified: Tue, 12 Nov 2024 00:55:36 GMT  
		Size: 143.3 MB (143321321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4048caa8e9536cbc81bd812da3ddbfcf0c242bc84e0aae8e5b62218311ada6f`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cef3cb7c9b8b7831050f192376fb3ec2e596319cbb7f00ab13fac740d9b429`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7326086bcd43354f495c22f41a1362e035b86efb1231658cc777d828e06c09b5`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0c972525eaadda0b5d220a60713fe6ae4aed202d0ce097494dd54d4cbddf88`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab0e4e89c886c68156494d0d15588424bdb261b6c099366489de19a967e3ea`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30fec73f163c700239a92f41e19b9f40da215af99c5ca19bc44ce23749fe999b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c0598285c843a368616c4153906d3ac3f653d3bfb236c35369f61c93ff8f72`

```dockerfile
```

-	Layers:
	-	`sha256:1e1412d68f0c82d49f7df302740602685430eae38a51dff2f5622494b8ef7716`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 26.5 KB (26526 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6eae6f07acede5586409eb0529970b5e8bbb650dbaf17e39c4efbb144757a6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174163120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d854e5fd0220b4126259e851b7ba390e22ab2b139704525b4329d29c0a7db8e3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f0a0c59e6c74754aaf916f8b6df9f98cffb99cb60e3ff6958bfafbe40c7254`  
		Last Modified: Tue, 12 Nov 2024 01:06:54 GMT  
		Size: 138.7 MB (138659691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adb863b4b4c69d8d08447ff2f92bde3bf58985fd69c6d0272273bfe6c682c8a`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d046b9b6fb2887e045118fa7b549f271dd6834e27a1a81bec062a420becc2333`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79602d6db082d0d6dd1cc2f9451cf185d6d2ae4746da01fcbbddfe11250b70ce`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9521f306a3451bfc3d658df655e47b14b6dfe1fa8a4ee01fa7239d256513d150`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7419c1b0b1b714719c8c0457161ee358c44e630ee2c264733dad78f1f666faa`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24` - unknown; unknown

```console
$ docker pull clickhouse@sha256:53da8ae3932d2be58b4497df239aa92f12380d79a3046061686fb1473f1c482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c2a42d0eb4773da3eb4d1f61c94f4652b79ba86145e6503c285a87d063c446`

```dockerfile
```

-	Layers:
	-	`sha256:8a15f595e98190849d608ae4aaf07c44b896636f633ab5818e0c64c15671d1a2`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 26.8 KB (26762 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24-focal`

```console
$ docker pull clickhouse@sha256:7bc9fa5ec703a95ffd5a2c6a271dab034aa0637dbc2fefbd5fc57e3283bec064
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:be2eb6602bb634c641a26de50062bc6db4a413fc5f8e2d30d69e63ae218c9300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180502273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780779b097fba8e76a39d39f0f34ce2e5bd628429919a69180f6c2f235a7e799`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111f8833bc453e9ec8c2ebf32ac32b825681a3b9b8e372c9e3398f52bb2d7bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 8.8 MB (8802605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c21f8f8706bb6e315bd1248a431189fb5403141581d2dd8c747495194028dc0`  
		Last Modified: Tue, 12 Nov 2024 00:55:36 GMT  
		Size: 143.3 MB (143321321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4048caa8e9536cbc81bd812da3ddbfcf0c242bc84e0aae8e5b62218311ada6f`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cef3cb7c9b8b7831050f192376fb3ec2e596319cbb7f00ab13fac740d9b429`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7326086bcd43354f495c22f41a1362e035b86efb1231658cc777d828e06c09b5`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0c972525eaadda0b5d220a60713fe6ae4aed202d0ce097494dd54d4cbddf88`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab0e4e89c886c68156494d0d15588424bdb261b6c099366489de19a967e3ea`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30fec73f163c700239a92f41e19b9f40da215af99c5ca19bc44ce23749fe999b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c0598285c843a368616c4153906d3ac3f653d3bfb236c35369f61c93ff8f72`

```dockerfile
```

-	Layers:
	-	`sha256:1e1412d68f0c82d49f7df302740602685430eae38a51dff2f5622494b8ef7716`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 26.5 KB (26526 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6eae6f07acede5586409eb0529970b5e8bbb650dbaf17e39c4efbb144757a6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174163120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d854e5fd0220b4126259e851b7ba390e22ab2b139704525b4329d29c0a7db8e3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f0a0c59e6c74754aaf916f8b6df9f98cffb99cb60e3ff6958bfafbe40c7254`  
		Last Modified: Tue, 12 Nov 2024 01:06:54 GMT  
		Size: 138.7 MB (138659691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adb863b4b4c69d8d08447ff2f92bde3bf58985fd69c6d0272273bfe6c682c8a`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d046b9b6fb2887e045118fa7b549f271dd6834e27a1a81bec062a420becc2333`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79602d6db082d0d6dd1cc2f9451cf185d6d2ae4746da01fcbbddfe11250b70ce`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9521f306a3451bfc3d658df655e47b14b6dfe1fa8a4ee01fa7239d256513d150`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7419c1b0b1b714719c8c0457161ee358c44e630ee2c264733dad78f1f666faa`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:53da8ae3932d2be58b4497df239aa92f12380d79a3046061686fb1473f1c482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c2a42d0eb4773da3eb4d1f61c94f4652b79ba86145e6503c285a87d063c446`

```dockerfile
```

-	Layers:
	-	`sha256:8a15f595e98190849d608ae4aaf07c44b896636f633ab5818e0c64c15671d1a2`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 26.8 KB (26762 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.10`

```console
$ docker pull clickhouse@sha256:7bc9fa5ec703a95ffd5a2c6a271dab034aa0637dbc2fefbd5fc57e3283bec064
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:be2eb6602bb634c641a26de50062bc6db4a413fc5f8e2d30d69e63ae218c9300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180502273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780779b097fba8e76a39d39f0f34ce2e5bd628429919a69180f6c2f235a7e799`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111f8833bc453e9ec8c2ebf32ac32b825681a3b9b8e372c9e3398f52bb2d7bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 8.8 MB (8802605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c21f8f8706bb6e315bd1248a431189fb5403141581d2dd8c747495194028dc0`  
		Last Modified: Tue, 12 Nov 2024 00:55:36 GMT  
		Size: 143.3 MB (143321321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4048caa8e9536cbc81bd812da3ddbfcf0c242bc84e0aae8e5b62218311ada6f`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cef3cb7c9b8b7831050f192376fb3ec2e596319cbb7f00ab13fac740d9b429`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7326086bcd43354f495c22f41a1362e035b86efb1231658cc777d828e06c09b5`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0c972525eaadda0b5d220a60713fe6ae4aed202d0ce097494dd54d4cbddf88`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab0e4e89c886c68156494d0d15588424bdb261b6c099366489de19a967e3ea`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30fec73f163c700239a92f41e19b9f40da215af99c5ca19bc44ce23749fe999b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c0598285c843a368616c4153906d3ac3f653d3bfb236c35369f61c93ff8f72`

```dockerfile
```

-	Layers:
	-	`sha256:1e1412d68f0c82d49f7df302740602685430eae38a51dff2f5622494b8ef7716`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 26.5 KB (26526 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6eae6f07acede5586409eb0529970b5e8bbb650dbaf17e39c4efbb144757a6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174163120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d854e5fd0220b4126259e851b7ba390e22ab2b139704525b4329d29c0a7db8e3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f0a0c59e6c74754aaf916f8b6df9f98cffb99cb60e3ff6958bfafbe40c7254`  
		Last Modified: Tue, 12 Nov 2024 01:06:54 GMT  
		Size: 138.7 MB (138659691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adb863b4b4c69d8d08447ff2f92bde3bf58985fd69c6d0272273bfe6c682c8a`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d046b9b6fb2887e045118fa7b549f271dd6834e27a1a81bec062a420becc2333`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79602d6db082d0d6dd1cc2f9451cf185d6d2ae4746da01fcbbddfe11250b70ce`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9521f306a3451bfc3d658df655e47b14b6dfe1fa8a4ee01fa7239d256513d150`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7419c1b0b1b714719c8c0457161ee358c44e630ee2c264733dad78f1f666faa`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:53da8ae3932d2be58b4497df239aa92f12380d79a3046061686fb1473f1c482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c2a42d0eb4773da3eb4d1f61c94f4652b79ba86145e6503c285a87d063c446`

```dockerfile
```

-	Layers:
	-	`sha256:8a15f595e98190849d608ae4aaf07c44b896636f633ab5818e0c64c15671d1a2`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 26.8 KB (26762 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.10-focal`

```console
$ docker pull clickhouse@sha256:7bc9fa5ec703a95ffd5a2c6a271dab034aa0637dbc2fefbd5fc57e3283bec064
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:be2eb6602bb634c641a26de50062bc6db4a413fc5f8e2d30d69e63ae218c9300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180502273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780779b097fba8e76a39d39f0f34ce2e5bd628429919a69180f6c2f235a7e799`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111f8833bc453e9ec8c2ebf32ac32b825681a3b9b8e372c9e3398f52bb2d7bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 8.8 MB (8802605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c21f8f8706bb6e315bd1248a431189fb5403141581d2dd8c747495194028dc0`  
		Last Modified: Tue, 12 Nov 2024 00:55:36 GMT  
		Size: 143.3 MB (143321321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4048caa8e9536cbc81bd812da3ddbfcf0c242bc84e0aae8e5b62218311ada6f`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cef3cb7c9b8b7831050f192376fb3ec2e596319cbb7f00ab13fac740d9b429`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7326086bcd43354f495c22f41a1362e035b86efb1231658cc777d828e06c09b5`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0c972525eaadda0b5d220a60713fe6ae4aed202d0ce097494dd54d4cbddf88`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab0e4e89c886c68156494d0d15588424bdb261b6c099366489de19a967e3ea`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30fec73f163c700239a92f41e19b9f40da215af99c5ca19bc44ce23749fe999b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c0598285c843a368616c4153906d3ac3f653d3bfb236c35369f61c93ff8f72`

```dockerfile
```

-	Layers:
	-	`sha256:1e1412d68f0c82d49f7df302740602685430eae38a51dff2f5622494b8ef7716`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 26.5 KB (26526 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6eae6f07acede5586409eb0529970b5e8bbb650dbaf17e39c4efbb144757a6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174163120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d854e5fd0220b4126259e851b7ba390e22ab2b139704525b4329d29c0a7db8e3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f0a0c59e6c74754aaf916f8b6df9f98cffb99cb60e3ff6958bfafbe40c7254`  
		Last Modified: Tue, 12 Nov 2024 01:06:54 GMT  
		Size: 138.7 MB (138659691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adb863b4b4c69d8d08447ff2f92bde3bf58985fd69c6d0272273bfe6c682c8a`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d046b9b6fb2887e045118fa7b549f271dd6834e27a1a81bec062a420becc2333`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79602d6db082d0d6dd1cc2f9451cf185d6d2ae4746da01fcbbddfe11250b70ce`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9521f306a3451bfc3d658df655e47b14b6dfe1fa8a4ee01fa7239d256513d150`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7419c1b0b1b714719c8c0457161ee358c44e630ee2c264733dad78f1f666faa`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:53da8ae3932d2be58b4497df239aa92f12380d79a3046061686fb1473f1c482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c2a42d0eb4773da3eb4d1f61c94f4652b79ba86145e6503c285a87d063c446`

```dockerfile
```

-	Layers:
	-	`sha256:8a15f595e98190849d608ae4aaf07c44b896636f633ab5818e0c64c15671d1a2`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 26.8 KB (26762 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.10.1`

```console
$ docker pull clickhouse@sha256:7bc9fa5ec703a95ffd5a2c6a271dab034aa0637dbc2fefbd5fc57e3283bec064
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:be2eb6602bb634c641a26de50062bc6db4a413fc5f8e2d30d69e63ae218c9300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180502273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780779b097fba8e76a39d39f0f34ce2e5bd628429919a69180f6c2f235a7e799`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111f8833bc453e9ec8c2ebf32ac32b825681a3b9b8e372c9e3398f52bb2d7bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 8.8 MB (8802605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c21f8f8706bb6e315bd1248a431189fb5403141581d2dd8c747495194028dc0`  
		Last Modified: Tue, 12 Nov 2024 00:55:36 GMT  
		Size: 143.3 MB (143321321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4048caa8e9536cbc81bd812da3ddbfcf0c242bc84e0aae8e5b62218311ada6f`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cef3cb7c9b8b7831050f192376fb3ec2e596319cbb7f00ab13fac740d9b429`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7326086bcd43354f495c22f41a1362e035b86efb1231658cc777d828e06c09b5`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0c972525eaadda0b5d220a60713fe6ae4aed202d0ce097494dd54d4cbddf88`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab0e4e89c886c68156494d0d15588424bdb261b6c099366489de19a967e3ea`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30fec73f163c700239a92f41e19b9f40da215af99c5ca19bc44ce23749fe999b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c0598285c843a368616c4153906d3ac3f653d3bfb236c35369f61c93ff8f72`

```dockerfile
```

-	Layers:
	-	`sha256:1e1412d68f0c82d49f7df302740602685430eae38a51dff2f5622494b8ef7716`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 26.5 KB (26526 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6eae6f07acede5586409eb0529970b5e8bbb650dbaf17e39c4efbb144757a6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174163120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d854e5fd0220b4126259e851b7ba390e22ab2b139704525b4329d29c0a7db8e3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f0a0c59e6c74754aaf916f8b6df9f98cffb99cb60e3ff6958bfafbe40c7254`  
		Last Modified: Tue, 12 Nov 2024 01:06:54 GMT  
		Size: 138.7 MB (138659691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adb863b4b4c69d8d08447ff2f92bde3bf58985fd69c6d0272273bfe6c682c8a`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d046b9b6fb2887e045118fa7b549f271dd6834e27a1a81bec062a420becc2333`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79602d6db082d0d6dd1cc2f9451cf185d6d2ae4746da01fcbbddfe11250b70ce`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9521f306a3451bfc3d658df655e47b14b6dfe1fa8a4ee01fa7239d256513d150`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7419c1b0b1b714719c8c0457161ee358c44e630ee2c264733dad78f1f666faa`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:53da8ae3932d2be58b4497df239aa92f12380d79a3046061686fb1473f1c482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c2a42d0eb4773da3eb4d1f61c94f4652b79ba86145e6503c285a87d063c446`

```dockerfile
```

-	Layers:
	-	`sha256:8a15f595e98190849d608ae4aaf07c44b896636f633ab5818e0c64c15671d1a2`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 26.8 KB (26762 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.10.1-focal`

```console
$ docker pull clickhouse@sha256:7bc9fa5ec703a95ffd5a2c6a271dab034aa0637dbc2fefbd5fc57e3283bec064
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10.1-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:be2eb6602bb634c641a26de50062bc6db4a413fc5f8e2d30d69e63ae218c9300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180502273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780779b097fba8e76a39d39f0f34ce2e5bd628429919a69180f6c2f235a7e799`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111f8833bc453e9ec8c2ebf32ac32b825681a3b9b8e372c9e3398f52bb2d7bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 8.8 MB (8802605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c21f8f8706bb6e315bd1248a431189fb5403141581d2dd8c747495194028dc0`  
		Last Modified: Tue, 12 Nov 2024 00:55:36 GMT  
		Size: 143.3 MB (143321321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4048caa8e9536cbc81bd812da3ddbfcf0c242bc84e0aae8e5b62218311ada6f`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cef3cb7c9b8b7831050f192376fb3ec2e596319cbb7f00ab13fac740d9b429`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7326086bcd43354f495c22f41a1362e035b86efb1231658cc777d828e06c09b5`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0c972525eaadda0b5d220a60713fe6ae4aed202d0ce097494dd54d4cbddf88`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab0e4e89c886c68156494d0d15588424bdb261b6c099366489de19a967e3ea`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.1-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30fec73f163c700239a92f41e19b9f40da215af99c5ca19bc44ce23749fe999b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c0598285c843a368616c4153906d3ac3f653d3bfb236c35369f61c93ff8f72`

```dockerfile
```

-	Layers:
	-	`sha256:1e1412d68f0c82d49f7df302740602685430eae38a51dff2f5622494b8ef7716`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 26.5 KB (26526 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10.1-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6eae6f07acede5586409eb0529970b5e8bbb650dbaf17e39c4efbb144757a6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174163120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d854e5fd0220b4126259e851b7ba390e22ab2b139704525b4329d29c0a7db8e3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f0a0c59e6c74754aaf916f8b6df9f98cffb99cb60e3ff6958bfafbe40c7254`  
		Last Modified: Tue, 12 Nov 2024 01:06:54 GMT  
		Size: 138.7 MB (138659691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adb863b4b4c69d8d08447ff2f92bde3bf58985fd69c6d0272273bfe6c682c8a`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d046b9b6fb2887e045118fa7b549f271dd6834e27a1a81bec062a420becc2333`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79602d6db082d0d6dd1cc2f9451cf185d6d2ae4746da01fcbbddfe11250b70ce`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9521f306a3451bfc3d658df655e47b14b6dfe1fa8a4ee01fa7239d256513d150`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7419c1b0b1b714719c8c0457161ee358c44e630ee2c264733dad78f1f666faa`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.1-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:53da8ae3932d2be58b4497df239aa92f12380d79a3046061686fb1473f1c482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c2a42d0eb4773da3eb4d1f61c94f4652b79ba86145e6503c285a87d063c446`

```dockerfile
```

-	Layers:
	-	`sha256:8a15f595e98190849d608ae4aaf07c44b896636f633ab5818e0c64c15671d1a2`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 26.8 KB (26762 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.10.1.2812`

```console
$ docker pull clickhouse@sha256:7bc9fa5ec703a95ffd5a2c6a271dab034aa0637dbc2fefbd5fc57e3283bec064
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10.1.2812` - linux; amd64

```console
$ docker pull clickhouse@sha256:be2eb6602bb634c641a26de50062bc6db4a413fc5f8e2d30d69e63ae218c9300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180502273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780779b097fba8e76a39d39f0f34ce2e5bd628429919a69180f6c2f235a7e799`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111f8833bc453e9ec8c2ebf32ac32b825681a3b9b8e372c9e3398f52bb2d7bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 8.8 MB (8802605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c21f8f8706bb6e315bd1248a431189fb5403141581d2dd8c747495194028dc0`  
		Last Modified: Tue, 12 Nov 2024 00:55:36 GMT  
		Size: 143.3 MB (143321321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4048caa8e9536cbc81bd812da3ddbfcf0c242bc84e0aae8e5b62218311ada6f`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cef3cb7c9b8b7831050f192376fb3ec2e596319cbb7f00ab13fac740d9b429`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7326086bcd43354f495c22f41a1362e035b86efb1231658cc777d828e06c09b5`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0c972525eaadda0b5d220a60713fe6ae4aed202d0ce097494dd54d4cbddf88`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab0e4e89c886c68156494d0d15588424bdb261b6c099366489de19a967e3ea`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.1.2812` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30fec73f163c700239a92f41e19b9f40da215af99c5ca19bc44ce23749fe999b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c0598285c843a368616c4153906d3ac3f653d3bfb236c35369f61c93ff8f72`

```dockerfile
```

-	Layers:
	-	`sha256:1e1412d68f0c82d49f7df302740602685430eae38a51dff2f5622494b8ef7716`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 26.5 KB (26526 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10.1.2812` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6eae6f07acede5586409eb0529970b5e8bbb650dbaf17e39c4efbb144757a6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174163120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d854e5fd0220b4126259e851b7ba390e22ab2b139704525b4329d29c0a7db8e3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f0a0c59e6c74754aaf916f8b6df9f98cffb99cb60e3ff6958bfafbe40c7254`  
		Last Modified: Tue, 12 Nov 2024 01:06:54 GMT  
		Size: 138.7 MB (138659691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adb863b4b4c69d8d08447ff2f92bde3bf58985fd69c6d0272273bfe6c682c8a`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d046b9b6fb2887e045118fa7b549f271dd6834e27a1a81bec062a420becc2333`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79602d6db082d0d6dd1cc2f9451cf185d6d2ae4746da01fcbbddfe11250b70ce`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9521f306a3451bfc3d658df655e47b14b6dfe1fa8a4ee01fa7239d256513d150`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7419c1b0b1b714719c8c0457161ee358c44e630ee2c264733dad78f1f666faa`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.1.2812` - unknown; unknown

```console
$ docker pull clickhouse@sha256:53da8ae3932d2be58b4497df239aa92f12380d79a3046061686fb1473f1c482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c2a42d0eb4773da3eb4d1f61c94f4652b79ba86145e6503c285a87d063c446`

```dockerfile
```

-	Layers:
	-	`sha256:8a15f595e98190849d608ae4aaf07c44b896636f633ab5818e0c64c15671d1a2`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 26.8 KB (26762 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.10.1.2812-focal`

```console
$ docker pull clickhouse@sha256:7bc9fa5ec703a95ffd5a2c6a271dab034aa0637dbc2fefbd5fc57e3283bec064
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10.1.2812-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:be2eb6602bb634c641a26de50062bc6db4a413fc5f8e2d30d69e63ae218c9300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180502273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780779b097fba8e76a39d39f0f34ce2e5bd628429919a69180f6c2f235a7e799`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111f8833bc453e9ec8c2ebf32ac32b825681a3b9b8e372c9e3398f52bb2d7bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 8.8 MB (8802605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c21f8f8706bb6e315bd1248a431189fb5403141581d2dd8c747495194028dc0`  
		Last Modified: Tue, 12 Nov 2024 00:55:36 GMT  
		Size: 143.3 MB (143321321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4048caa8e9536cbc81bd812da3ddbfcf0c242bc84e0aae8e5b62218311ada6f`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cef3cb7c9b8b7831050f192376fb3ec2e596319cbb7f00ab13fac740d9b429`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7326086bcd43354f495c22f41a1362e035b86efb1231658cc777d828e06c09b5`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0c972525eaadda0b5d220a60713fe6ae4aed202d0ce097494dd54d4cbddf88`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab0e4e89c886c68156494d0d15588424bdb261b6c099366489de19a967e3ea`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.1.2812-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30fec73f163c700239a92f41e19b9f40da215af99c5ca19bc44ce23749fe999b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c0598285c843a368616c4153906d3ac3f653d3bfb236c35369f61c93ff8f72`

```dockerfile
```

-	Layers:
	-	`sha256:1e1412d68f0c82d49f7df302740602685430eae38a51dff2f5622494b8ef7716`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 26.5 KB (26526 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10.1.2812-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6eae6f07acede5586409eb0529970b5e8bbb650dbaf17e39c4efbb144757a6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174163120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d854e5fd0220b4126259e851b7ba390e22ab2b139704525b4329d29c0a7db8e3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f0a0c59e6c74754aaf916f8b6df9f98cffb99cb60e3ff6958bfafbe40c7254`  
		Last Modified: Tue, 12 Nov 2024 01:06:54 GMT  
		Size: 138.7 MB (138659691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adb863b4b4c69d8d08447ff2f92bde3bf58985fd69c6d0272273bfe6c682c8a`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d046b9b6fb2887e045118fa7b549f271dd6834e27a1a81bec062a420becc2333`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79602d6db082d0d6dd1cc2f9451cf185d6d2ae4746da01fcbbddfe11250b70ce`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9521f306a3451bfc3d658df655e47b14b6dfe1fa8a4ee01fa7239d256513d150`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7419c1b0b1b714719c8c0457161ee358c44e630ee2c264733dad78f1f666faa`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.1.2812-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:53da8ae3932d2be58b4497df239aa92f12380d79a3046061686fb1473f1c482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c2a42d0eb4773da3eb4d1f61c94f4652b79ba86145e6503c285a87d063c446`

```dockerfile
```

-	Layers:
	-	`sha256:8a15f595e98190849d608ae4aaf07c44b896636f633ab5818e0c64c15671d1a2`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 26.8 KB (26762 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3`

```console
$ docker pull clickhouse@sha256:65cc866aac0e00a6b0f47015f504cba9d3b3a3cc906f5b4e52d71d9a13707295
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:c289f3357934a59c8df32e38f46717666ef48fb22f16ba88504842ad9ab55057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297511750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2cd2e0d4d0268fad64fc1d15db2246633f2ed80b2530426737584fe9866e92d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.3.13.40
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c55cd1d667adb252a4d6747dd3ff98c2e5fd8ec94b8e8a853c71d48ac7f53`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 8.8 MB (8802650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6db53e848773ac965d917ff203b5173c8151e03138f5b7acc2bf32dd9ab870`  
		Last Modified: Tue, 12 Nov 2024 00:55:57 GMT  
		Size: 260.3 MB (260330598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddfab2ae361ce2d2db63312a3e93a526b702cf3e4e10a018b410fe2147b0826`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8aa72042ed8e0be5a3920224242fc7cdcafbfeb7280218c8439d0ba150f809`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f9db3a285345521ed70deb53a73153e353715e2e8e4976e0ffa97c236c296a`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0f5857dc58d47020d0d4bec291ddfdba3d1c0259e54e83c255b98e09cad68b`  
		Last Modified: Tue, 12 Nov 2024 00:55:55 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9028d92b314d2596e2d3f5ce617257a35c38a1d2e79ba962357a2741963df81a`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b888d927481b1d47d60c9f5ef1191f6a487995c84264cae7cbd37966e7214c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d54f21a541c83c6cb2b6586615cfec4346f71de467d49d46d2a6c5b683238b`

```dockerfile
```

-	Layers:
	-	`sha256:f042d19fd7edc8c5a3ff4a042dd521d7eb65727bb779b73b14f1dda5b0cf7aff`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0f15c044786702dc99e19e911749b23d2edd2dbbc6c158eacf46e05ff7e7f176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (284991050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af05545f78127ee0804f1c557139fd211cb28905bd930c0ab44a85ec759b486`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.3.13.40
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97834f7eecadf60bfb24081933e8084f7861371bef3882bcc30642f4062ae788`  
		Last Modified: Tue, 12 Nov 2024 01:09:51 GMT  
		Size: 249.5 MB (249487447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a7242804b913aae26afac636978a9c1ae85309eb029039badba64bdf4f5b9`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7867f5d53eaedd052d0e6b5499d54fe22e0975c8b57cd61ba5b8768749d20bee`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 863.5 KB (863479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00beda7972859546008c521ae79b8e2bbdc0bd502ba8620805495f46b4b0d62d`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeb399d8db934dfd23e431b496a19a67aab69041474ae6a8b97ec7afe4dd060`  
		Last Modified: Tue, 12 Nov 2024 01:09:47 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaabf091eea37629b46996cab18b80152dea41dc6a9678f770cfb3eacff3d2a6`  
		Last Modified: Tue, 12 Nov 2024 01:09:47 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:45a3695cf706dae86c5e1192847ecefcd476942243c961d39e3d69dbd14dbe30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f514b9242e91460d0f52e90f29854c31118ca4474f8012fbf9ad6c7550cca4`

```dockerfile
```

-	Layers:
	-	`sha256:a1754f2703abef646e101fafb62d9eebb84e74c87c621f25677c3213519479e7`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3-focal`

```console
$ docker pull clickhouse@sha256:65cc866aac0e00a6b0f47015f504cba9d3b3a3cc906f5b4e52d71d9a13707295
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:c289f3357934a59c8df32e38f46717666ef48fb22f16ba88504842ad9ab55057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297511750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2cd2e0d4d0268fad64fc1d15db2246633f2ed80b2530426737584fe9866e92d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.3.13.40
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c55cd1d667adb252a4d6747dd3ff98c2e5fd8ec94b8e8a853c71d48ac7f53`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 8.8 MB (8802650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6db53e848773ac965d917ff203b5173c8151e03138f5b7acc2bf32dd9ab870`  
		Last Modified: Tue, 12 Nov 2024 00:55:57 GMT  
		Size: 260.3 MB (260330598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddfab2ae361ce2d2db63312a3e93a526b702cf3e4e10a018b410fe2147b0826`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8aa72042ed8e0be5a3920224242fc7cdcafbfeb7280218c8439d0ba150f809`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f9db3a285345521ed70deb53a73153e353715e2e8e4976e0ffa97c236c296a`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0f5857dc58d47020d0d4bec291ddfdba3d1c0259e54e83c255b98e09cad68b`  
		Last Modified: Tue, 12 Nov 2024 00:55:55 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9028d92b314d2596e2d3f5ce617257a35c38a1d2e79ba962357a2741963df81a`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b888d927481b1d47d60c9f5ef1191f6a487995c84264cae7cbd37966e7214c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d54f21a541c83c6cb2b6586615cfec4346f71de467d49d46d2a6c5b683238b`

```dockerfile
```

-	Layers:
	-	`sha256:f042d19fd7edc8c5a3ff4a042dd521d7eb65727bb779b73b14f1dda5b0cf7aff`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0f15c044786702dc99e19e911749b23d2edd2dbbc6c158eacf46e05ff7e7f176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (284991050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af05545f78127ee0804f1c557139fd211cb28905bd930c0ab44a85ec759b486`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.3.13.40
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97834f7eecadf60bfb24081933e8084f7861371bef3882bcc30642f4062ae788`  
		Last Modified: Tue, 12 Nov 2024 01:09:51 GMT  
		Size: 249.5 MB (249487447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a7242804b913aae26afac636978a9c1ae85309eb029039badba64bdf4f5b9`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7867f5d53eaedd052d0e6b5499d54fe22e0975c8b57cd61ba5b8768749d20bee`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 863.5 KB (863479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00beda7972859546008c521ae79b8e2bbdc0bd502ba8620805495f46b4b0d62d`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeb399d8db934dfd23e431b496a19a67aab69041474ae6a8b97ec7afe4dd060`  
		Last Modified: Tue, 12 Nov 2024 01:09:47 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaabf091eea37629b46996cab18b80152dea41dc6a9678f770cfb3eacff3d2a6`  
		Last Modified: Tue, 12 Nov 2024 01:09:47 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:45a3695cf706dae86c5e1192847ecefcd476942243c961d39e3d69dbd14dbe30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f514b9242e91460d0f52e90f29854c31118ca4474f8012fbf9ad6c7550cca4`

```dockerfile
```

-	Layers:
	-	`sha256:a1754f2703abef646e101fafb62d9eebb84e74c87c621f25677c3213519479e7`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3.13`

```console
$ docker pull clickhouse@sha256:65cc866aac0e00a6b0f47015f504cba9d3b3a3cc906f5b4e52d71d9a13707295
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3.13` - linux; amd64

```console
$ docker pull clickhouse@sha256:c289f3357934a59c8df32e38f46717666ef48fb22f16ba88504842ad9ab55057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297511750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2cd2e0d4d0268fad64fc1d15db2246633f2ed80b2530426737584fe9866e92d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.3.13.40
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c55cd1d667adb252a4d6747dd3ff98c2e5fd8ec94b8e8a853c71d48ac7f53`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 8.8 MB (8802650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6db53e848773ac965d917ff203b5173c8151e03138f5b7acc2bf32dd9ab870`  
		Last Modified: Tue, 12 Nov 2024 00:55:57 GMT  
		Size: 260.3 MB (260330598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddfab2ae361ce2d2db63312a3e93a526b702cf3e4e10a018b410fe2147b0826`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8aa72042ed8e0be5a3920224242fc7cdcafbfeb7280218c8439d0ba150f809`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f9db3a285345521ed70deb53a73153e353715e2e8e4976e0ffa97c236c296a`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0f5857dc58d47020d0d4bec291ddfdba3d1c0259e54e83c255b98e09cad68b`  
		Last Modified: Tue, 12 Nov 2024 00:55:55 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9028d92b314d2596e2d3f5ce617257a35c38a1d2e79ba962357a2741963df81a`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.13` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b888d927481b1d47d60c9f5ef1191f6a487995c84264cae7cbd37966e7214c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d54f21a541c83c6cb2b6586615cfec4346f71de467d49d46d2a6c5b683238b`

```dockerfile
```

-	Layers:
	-	`sha256:f042d19fd7edc8c5a3ff4a042dd521d7eb65727bb779b73b14f1dda5b0cf7aff`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3.13` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0f15c044786702dc99e19e911749b23d2edd2dbbc6c158eacf46e05ff7e7f176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (284991050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af05545f78127ee0804f1c557139fd211cb28905bd930c0ab44a85ec759b486`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.3.13.40
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97834f7eecadf60bfb24081933e8084f7861371bef3882bcc30642f4062ae788`  
		Last Modified: Tue, 12 Nov 2024 01:09:51 GMT  
		Size: 249.5 MB (249487447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a7242804b913aae26afac636978a9c1ae85309eb029039badba64bdf4f5b9`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7867f5d53eaedd052d0e6b5499d54fe22e0975c8b57cd61ba5b8768749d20bee`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 863.5 KB (863479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00beda7972859546008c521ae79b8e2bbdc0bd502ba8620805495f46b4b0d62d`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeb399d8db934dfd23e431b496a19a67aab69041474ae6a8b97ec7afe4dd060`  
		Last Modified: Tue, 12 Nov 2024 01:09:47 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaabf091eea37629b46996cab18b80152dea41dc6a9678f770cfb3eacff3d2a6`  
		Last Modified: Tue, 12 Nov 2024 01:09:47 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.13` - unknown; unknown

```console
$ docker pull clickhouse@sha256:45a3695cf706dae86c5e1192847ecefcd476942243c961d39e3d69dbd14dbe30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f514b9242e91460d0f52e90f29854c31118ca4474f8012fbf9ad6c7550cca4`

```dockerfile
```

-	Layers:
	-	`sha256:a1754f2703abef646e101fafb62d9eebb84e74c87c621f25677c3213519479e7`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3.13-focal`

```console
$ docker pull clickhouse@sha256:65cc866aac0e00a6b0f47015f504cba9d3b3a3cc906f5b4e52d71d9a13707295
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3.13-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:c289f3357934a59c8df32e38f46717666ef48fb22f16ba88504842ad9ab55057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297511750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2cd2e0d4d0268fad64fc1d15db2246633f2ed80b2530426737584fe9866e92d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.3.13.40
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c55cd1d667adb252a4d6747dd3ff98c2e5fd8ec94b8e8a853c71d48ac7f53`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 8.8 MB (8802650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6db53e848773ac965d917ff203b5173c8151e03138f5b7acc2bf32dd9ab870`  
		Last Modified: Tue, 12 Nov 2024 00:55:57 GMT  
		Size: 260.3 MB (260330598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddfab2ae361ce2d2db63312a3e93a526b702cf3e4e10a018b410fe2147b0826`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8aa72042ed8e0be5a3920224242fc7cdcafbfeb7280218c8439d0ba150f809`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f9db3a285345521ed70deb53a73153e353715e2e8e4976e0ffa97c236c296a`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0f5857dc58d47020d0d4bec291ddfdba3d1c0259e54e83c255b98e09cad68b`  
		Last Modified: Tue, 12 Nov 2024 00:55:55 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9028d92b314d2596e2d3f5ce617257a35c38a1d2e79ba962357a2741963df81a`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.13-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b888d927481b1d47d60c9f5ef1191f6a487995c84264cae7cbd37966e7214c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d54f21a541c83c6cb2b6586615cfec4346f71de467d49d46d2a6c5b683238b`

```dockerfile
```

-	Layers:
	-	`sha256:f042d19fd7edc8c5a3ff4a042dd521d7eb65727bb779b73b14f1dda5b0cf7aff`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3.13-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0f15c044786702dc99e19e911749b23d2edd2dbbc6c158eacf46e05ff7e7f176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (284991050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af05545f78127ee0804f1c557139fd211cb28905bd930c0ab44a85ec759b486`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.3.13.40
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97834f7eecadf60bfb24081933e8084f7861371bef3882bcc30642f4062ae788`  
		Last Modified: Tue, 12 Nov 2024 01:09:51 GMT  
		Size: 249.5 MB (249487447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a7242804b913aae26afac636978a9c1ae85309eb029039badba64bdf4f5b9`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7867f5d53eaedd052d0e6b5499d54fe22e0975c8b57cd61ba5b8768749d20bee`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 863.5 KB (863479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00beda7972859546008c521ae79b8e2bbdc0bd502ba8620805495f46b4b0d62d`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeb399d8db934dfd23e431b496a19a67aab69041474ae6a8b97ec7afe4dd060`  
		Last Modified: Tue, 12 Nov 2024 01:09:47 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaabf091eea37629b46996cab18b80152dea41dc6a9678f770cfb3eacff3d2a6`  
		Last Modified: Tue, 12 Nov 2024 01:09:47 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.13-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:45a3695cf706dae86c5e1192847ecefcd476942243c961d39e3d69dbd14dbe30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f514b9242e91460d0f52e90f29854c31118ca4474f8012fbf9ad6c7550cca4`

```dockerfile
```

-	Layers:
	-	`sha256:a1754f2703abef646e101fafb62d9eebb84e74c87c621f25677c3213519479e7`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3.13.40`

```console
$ docker pull clickhouse@sha256:65cc866aac0e00a6b0f47015f504cba9d3b3a3cc906f5b4e52d71d9a13707295
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3.13.40` - linux; amd64

```console
$ docker pull clickhouse@sha256:c289f3357934a59c8df32e38f46717666ef48fb22f16ba88504842ad9ab55057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297511750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2cd2e0d4d0268fad64fc1d15db2246633f2ed80b2530426737584fe9866e92d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.3.13.40
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c55cd1d667adb252a4d6747dd3ff98c2e5fd8ec94b8e8a853c71d48ac7f53`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 8.8 MB (8802650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6db53e848773ac965d917ff203b5173c8151e03138f5b7acc2bf32dd9ab870`  
		Last Modified: Tue, 12 Nov 2024 00:55:57 GMT  
		Size: 260.3 MB (260330598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddfab2ae361ce2d2db63312a3e93a526b702cf3e4e10a018b410fe2147b0826`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8aa72042ed8e0be5a3920224242fc7cdcafbfeb7280218c8439d0ba150f809`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f9db3a285345521ed70deb53a73153e353715e2e8e4976e0ffa97c236c296a`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0f5857dc58d47020d0d4bec291ddfdba3d1c0259e54e83c255b98e09cad68b`  
		Last Modified: Tue, 12 Nov 2024 00:55:55 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9028d92b314d2596e2d3f5ce617257a35c38a1d2e79ba962357a2741963df81a`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.13.40` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b888d927481b1d47d60c9f5ef1191f6a487995c84264cae7cbd37966e7214c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d54f21a541c83c6cb2b6586615cfec4346f71de467d49d46d2a6c5b683238b`

```dockerfile
```

-	Layers:
	-	`sha256:f042d19fd7edc8c5a3ff4a042dd521d7eb65727bb779b73b14f1dda5b0cf7aff`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3.13.40` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0f15c044786702dc99e19e911749b23d2edd2dbbc6c158eacf46e05ff7e7f176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (284991050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af05545f78127ee0804f1c557139fd211cb28905bd930c0ab44a85ec759b486`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.3.13.40
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97834f7eecadf60bfb24081933e8084f7861371bef3882bcc30642f4062ae788`  
		Last Modified: Tue, 12 Nov 2024 01:09:51 GMT  
		Size: 249.5 MB (249487447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a7242804b913aae26afac636978a9c1ae85309eb029039badba64bdf4f5b9`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7867f5d53eaedd052d0e6b5499d54fe22e0975c8b57cd61ba5b8768749d20bee`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 863.5 KB (863479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00beda7972859546008c521ae79b8e2bbdc0bd502ba8620805495f46b4b0d62d`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeb399d8db934dfd23e431b496a19a67aab69041474ae6a8b97ec7afe4dd060`  
		Last Modified: Tue, 12 Nov 2024 01:09:47 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaabf091eea37629b46996cab18b80152dea41dc6a9678f770cfb3eacff3d2a6`  
		Last Modified: Tue, 12 Nov 2024 01:09:47 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.13.40` - unknown; unknown

```console
$ docker pull clickhouse@sha256:45a3695cf706dae86c5e1192847ecefcd476942243c961d39e3d69dbd14dbe30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f514b9242e91460d0f52e90f29854c31118ca4474f8012fbf9ad6c7550cca4`

```dockerfile
```

-	Layers:
	-	`sha256:a1754f2703abef646e101fafb62d9eebb84e74c87c621f25677c3213519479e7`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3.13.40-focal`

```console
$ docker pull clickhouse@sha256:65cc866aac0e00a6b0f47015f504cba9d3b3a3cc906f5b4e52d71d9a13707295
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3.13.40-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:c289f3357934a59c8df32e38f46717666ef48fb22f16ba88504842ad9ab55057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297511750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2cd2e0d4d0268fad64fc1d15db2246633f2ed80b2530426737584fe9866e92d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.3.13.40
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10c55cd1d667adb252a4d6747dd3ff98c2e5fd8ec94b8e8a853c71d48ac7f53`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 8.8 MB (8802650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6db53e848773ac965d917ff203b5173c8151e03138f5b7acc2bf32dd9ab870`  
		Last Modified: Tue, 12 Nov 2024 00:55:57 GMT  
		Size: 260.3 MB (260330598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ddfab2ae361ce2d2db63312a3e93a526b702cf3e4e10a018b410fe2147b0826`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 346.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8aa72042ed8e0be5a3920224242fc7cdcafbfeb7280218c8439d0ba150f809`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f9db3a285345521ed70deb53a73153e353715e2e8e4976e0ffa97c236c296a`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0f5857dc58d47020d0d4bec291ddfdba3d1c0259e54e83c255b98e09cad68b`  
		Last Modified: Tue, 12 Nov 2024 00:55:55 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9028d92b314d2596e2d3f5ce617257a35c38a1d2e79ba962357a2741963df81a`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.13.40-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b888d927481b1d47d60c9f5ef1191f6a487995c84264cae7cbd37966e7214c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d54f21a541c83c6cb2b6586615cfec4346f71de467d49d46d2a6c5b683238b`

```dockerfile
```

-	Layers:
	-	`sha256:f042d19fd7edc8c5a3ff4a042dd521d7eb65727bb779b73b14f1dda5b0cf7aff`  
		Last Modified: Tue, 12 Nov 2024 00:55:54 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3.13.40-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0f15c044786702dc99e19e911749b23d2edd2dbbc6c158eacf46e05ff7e7f176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (284991050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af05545f78127ee0804f1c557139fd211cb28905bd930c0ab44a85ec759b486`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.3.13.40
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.13.40 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97834f7eecadf60bfb24081933e8084f7861371bef3882bcc30642f4062ae788`  
		Last Modified: Tue, 12 Nov 2024 01:09:51 GMT  
		Size: 249.5 MB (249487447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2a7242804b913aae26afac636978a9c1ae85309eb029039badba64bdf4f5b9`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 353.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7867f5d53eaedd052d0e6b5499d54fe22e0975c8b57cd61ba5b8768749d20bee`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 863.5 KB (863479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00beda7972859546008c521ae79b8e2bbdc0bd502ba8620805495f46b4b0d62d`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eeb399d8db934dfd23e431b496a19a67aab69041474ae6a8b97ec7afe4dd060`  
		Last Modified: Tue, 12 Nov 2024 01:09:47 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaabf091eea37629b46996cab18b80152dea41dc6a9678f770cfb3eacff3d2a6`  
		Last Modified: Tue, 12 Nov 2024 01:09:47 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.13.40-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:45a3695cf706dae86c5e1192847ecefcd476942243c961d39e3d69dbd14dbe30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f514b9242e91460d0f52e90f29854c31118ca4474f8012fbf9ad6c7550cca4`

```dockerfile
```

-	Layers:
	-	`sha256:a1754f2703abef646e101fafb62d9eebb84e74c87c621f25677c3213519479e7`  
		Last Modified: Tue, 12 Nov 2024 01:09:46 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8`

```console
$ docker pull clickhouse@sha256:483935440135426977c106678d8e66a62cc35d6789d46da88404ab1fc5a381c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:cdc811aae31208585fa3fb4f4f12a3d3acf32c4e26101f92ce8f563a605cd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178783594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af14c36eab65d777010e7558f8c267935cf981ffb70df18f651c6b505848103`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b07dd07e1b82d4c98112e85407bd268cf85766f2c34d147b20651183802910`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 8.8 MB (8802576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f45f27d0be4d81ed312ac77c0769ecc8a26ebe5a2f89fe1a5411013b124944`  
		Last Modified: Tue, 12 Nov 2024 00:55:49 GMT  
		Size: 141.6 MB (141602673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce7ca591ce59226feabf12de023349866551184c68e2e102fe522b32496a008`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ef09230e4836d994bbe5443402cc90ef111b6f73ca6f76bab13170c36f853f`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c625ca81d187d83be46a1890b904f7a7217a8bfe819bb44172ff6eb35299dbf`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86a2945cbff6e172e884ea3d417becb92421dc5bfe36fb7a44c20ccaf7df9bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee8ade4d8aa3b9136d6604417a36f0141161876e30640d194d7a8328b96ae70`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:21243244872f6c180cc0540daf6c78a7563153542ab8a4569a42ef6e6cf86fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e098533a234612bdb0324e86fa5b658021558488e993e0b47f1e4349a1096d38`

```dockerfile
```

-	Layers:
	-	`sha256:6e00efd847634f80df847d3d9a293f3653c937f4d22714d0574aeaf2755183e2`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:232efe54fed33fb29e34d26048cda3acdf546796dd1c025e0b130b1acc0c2364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172169371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193563e3cedf52c1cf0fac821d51c7f6027324022fde1b5acc3e709a6d8d07e7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6948cfea4a51c536096b2b78d89558f999dc084aafe6d0a64ad270d500c584a3`  
		Last Modified: Tue, 12 Nov 2024 01:08:40 GMT  
		Size: 136.7 MB (136665946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae1e740a57e967033425e15cbbef58623f580e3e05eaa488af2549150489016`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca632dae928fb1896852c1fb89b6c1e5cdf2e934a59b4e94165c64241f35478`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49220562a2798401ef2a70bfba4f678a869b1627ab96f492fba656704002f582`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c29b785e3f2042e0c04eb6997fad37c4f703ac19a8f81c07b45531dc26e42d`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438b90cdb70d964cf18a00c838bcbe410cb2b74a1fa57cf456fda21c4f0903a4`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ddfe734a1c712615ee3d0127f21f4b191885287ccf44661a20ceebeec233d98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0e80c78377cd8a46ca655d9b51e98396c3a1b41c98720ddd0880a3067768ac`

```dockerfile
```

-	Layers:
	-	`sha256:d1a1a00d2596db9b2273ff26bbaca213308822cf8e26ab1c6cf979bc6ca32b96`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8-focal`

```console
$ docker pull clickhouse@sha256:483935440135426977c106678d8e66a62cc35d6789d46da88404ab1fc5a381c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:cdc811aae31208585fa3fb4f4f12a3d3acf32c4e26101f92ce8f563a605cd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178783594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af14c36eab65d777010e7558f8c267935cf981ffb70df18f651c6b505848103`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b07dd07e1b82d4c98112e85407bd268cf85766f2c34d147b20651183802910`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 8.8 MB (8802576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f45f27d0be4d81ed312ac77c0769ecc8a26ebe5a2f89fe1a5411013b124944`  
		Last Modified: Tue, 12 Nov 2024 00:55:49 GMT  
		Size: 141.6 MB (141602673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce7ca591ce59226feabf12de023349866551184c68e2e102fe522b32496a008`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ef09230e4836d994bbe5443402cc90ef111b6f73ca6f76bab13170c36f853f`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c625ca81d187d83be46a1890b904f7a7217a8bfe819bb44172ff6eb35299dbf`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86a2945cbff6e172e884ea3d417becb92421dc5bfe36fb7a44c20ccaf7df9bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee8ade4d8aa3b9136d6604417a36f0141161876e30640d194d7a8328b96ae70`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:21243244872f6c180cc0540daf6c78a7563153542ab8a4569a42ef6e6cf86fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e098533a234612bdb0324e86fa5b658021558488e993e0b47f1e4349a1096d38`

```dockerfile
```

-	Layers:
	-	`sha256:6e00efd847634f80df847d3d9a293f3653c937f4d22714d0574aeaf2755183e2`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:232efe54fed33fb29e34d26048cda3acdf546796dd1c025e0b130b1acc0c2364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172169371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193563e3cedf52c1cf0fac821d51c7f6027324022fde1b5acc3e709a6d8d07e7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6948cfea4a51c536096b2b78d89558f999dc084aafe6d0a64ad270d500c584a3`  
		Last Modified: Tue, 12 Nov 2024 01:08:40 GMT  
		Size: 136.7 MB (136665946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae1e740a57e967033425e15cbbef58623f580e3e05eaa488af2549150489016`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca632dae928fb1896852c1fb89b6c1e5cdf2e934a59b4e94165c64241f35478`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49220562a2798401ef2a70bfba4f678a869b1627ab96f492fba656704002f582`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c29b785e3f2042e0c04eb6997fad37c4f703ac19a8f81c07b45531dc26e42d`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438b90cdb70d964cf18a00c838bcbe410cb2b74a1fa57cf456fda21c4f0903a4`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ddfe734a1c712615ee3d0127f21f4b191885287ccf44661a20ceebeec233d98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0e80c78377cd8a46ca655d9b51e98396c3a1b41c98720ddd0880a3067768ac`

```dockerfile
```

-	Layers:
	-	`sha256:d1a1a00d2596db9b2273ff26bbaca213308822cf8e26ab1c6cf979bc6ca32b96`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.6`

```console
$ docker pull clickhouse@sha256:483935440135426977c106678d8e66a62cc35d6789d46da88404ab1fc5a381c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:cdc811aae31208585fa3fb4f4f12a3d3acf32c4e26101f92ce8f563a605cd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178783594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af14c36eab65d777010e7558f8c267935cf981ffb70df18f651c6b505848103`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b07dd07e1b82d4c98112e85407bd268cf85766f2c34d147b20651183802910`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 8.8 MB (8802576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f45f27d0be4d81ed312ac77c0769ecc8a26ebe5a2f89fe1a5411013b124944`  
		Last Modified: Tue, 12 Nov 2024 00:55:49 GMT  
		Size: 141.6 MB (141602673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce7ca591ce59226feabf12de023349866551184c68e2e102fe522b32496a008`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ef09230e4836d994bbe5443402cc90ef111b6f73ca6f76bab13170c36f853f`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c625ca81d187d83be46a1890b904f7a7217a8bfe819bb44172ff6eb35299dbf`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86a2945cbff6e172e884ea3d417becb92421dc5bfe36fb7a44c20ccaf7df9bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee8ade4d8aa3b9136d6604417a36f0141161876e30640d194d7a8328b96ae70`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:21243244872f6c180cc0540daf6c78a7563153542ab8a4569a42ef6e6cf86fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e098533a234612bdb0324e86fa5b658021558488e993e0b47f1e4349a1096d38`

```dockerfile
```

-	Layers:
	-	`sha256:6e00efd847634f80df847d3d9a293f3653c937f4d22714d0574aeaf2755183e2`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:232efe54fed33fb29e34d26048cda3acdf546796dd1c025e0b130b1acc0c2364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172169371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193563e3cedf52c1cf0fac821d51c7f6027324022fde1b5acc3e709a6d8d07e7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6948cfea4a51c536096b2b78d89558f999dc084aafe6d0a64ad270d500c584a3`  
		Last Modified: Tue, 12 Nov 2024 01:08:40 GMT  
		Size: 136.7 MB (136665946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae1e740a57e967033425e15cbbef58623f580e3e05eaa488af2549150489016`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca632dae928fb1896852c1fb89b6c1e5cdf2e934a59b4e94165c64241f35478`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49220562a2798401ef2a70bfba4f678a869b1627ab96f492fba656704002f582`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c29b785e3f2042e0c04eb6997fad37c4f703ac19a8f81c07b45531dc26e42d`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438b90cdb70d964cf18a00c838bcbe410cb2b74a1fa57cf456fda21c4f0903a4`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ddfe734a1c712615ee3d0127f21f4b191885287ccf44661a20ceebeec233d98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0e80c78377cd8a46ca655d9b51e98396c3a1b41c98720ddd0880a3067768ac`

```dockerfile
```

-	Layers:
	-	`sha256:d1a1a00d2596db9b2273ff26bbaca213308822cf8e26ab1c6cf979bc6ca32b96`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.6-focal`

```console
$ docker pull clickhouse@sha256:483935440135426977c106678d8e66a62cc35d6789d46da88404ab1fc5a381c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.6-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:cdc811aae31208585fa3fb4f4f12a3d3acf32c4e26101f92ce8f563a605cd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178783594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af14c36eab65d777010e7558f8c267935cf981ffb70df18f651c6b505848103`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b07dd07e1b82d4c98112e85407bd268cf85766f2c34d147b20651183802910`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 8.8 MB (8802576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f45f27d0be4d81ed312ac77c0769ecc8a26ebe5a2f89fe1a5411013b124944`  
		Last Modified: Tue, 12 Nov 2024 00:55:49 GMT  
		Size: 141.6 MB (141602673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce7ca591ce59226feabf12de023349866551184c68e2e102fe522b32496a008`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ef09230e4836d994bbe5443402cc90ef111b6f73ca6f76bab13170c36f853f`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c625ca81d187d83be46a1890b904f7a7217a8bfe819bb44172ff6eb35299dbf`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86a2945cbff6e172e884ea3d417becb92421dc5bfe36fb7a44c20ccaf7df9bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee8ade4d8aa3b9136d6604417a36f0141161876e30640d194d7a8328b96ae70`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.6-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:21243244872f6c180cc0540daf6c78a7563153542ab8a4569a42ef6e6cf86fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e098533a234612bdb0324e86fa5b658021558488e993e0b47f1e4349a1096d38`

```dockerfile
```

-	Layers:
	-	`sha256:6e00efd847634f80df847d3d9a293f3653c937f4d22714d0574aeaf2755183e2`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.6-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:232efe54fed33fb29e34d26048cda3acdf546796dd1c025e0b130b1acc0c2364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172169371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193563e3cedf52c1cf0fac821d51c7f6027324022fde1b5acc3e709a6d8d07e7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6948cfea4a51c536096b2b78d89558f999dc084aafe6d0a64ad270d500c584a3`  
		Last Modified: Tue, 12 Nov 2024 01:08:40 GMT  
		Size: 136.7 MB (136665946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae1e740a57e967033425e15cbbef58623f580e3e05eaa488af2549150489016`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca632dae928fb1896852c1fb89b6c1e5cdf2e934a59b4e94165c64241f35478`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49220562a2798401ef2a70bfba4f678a869b1627ab96f492fba656704002f582`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c29b785e3f2042e0c04eb6997fad37c4f703ac19a8f81c07b45531dc26e42d`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438b90cdb70d964cf18a00c838bcbe410cb2b74a1fa57cf456fda21c4f0903a4`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.6-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ddfe734a1c712615ee3d0127f21f4b191885287ccf44661a20ceebeec233d98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0e80c78377cd8a46ca655d9b51e98396c3a1b41c98720ddd0880a3067768ac`

```dockerfile
```

-	Layers:
	-	`sha256:d1a1a00d2596db9b2273ff26bbaca213308822cf8e26ab1c6cf979bc6ca32b96`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.6.70`

```console
$ docker pull clickhouse@sha256:483935440135426977c106678d8e66a62cc35d6789d46da88404ab1fc5a381c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.6.70` - linux; amd64

```console
$ docker pull clickhouse@sha256:cdc811aae31208585fa3fb4f4f12a3d3acf32c4e26101f92ce8f563a605cd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178783594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af14c36eab65d777010e7558f8c267935cf981ffb70df18f651c6b505848103`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b07dd07e1b82d4c98112e85407bd268cf85766f2c34d147b20651183802910`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 8.8 MB (8802576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f45f27d0be4d81ed312ac77c0769ecc8a26ebe5a2f89fe1a5411013b124944`  
		Last Modified: Tue, 12 Nov 2024 00:55:49 GMT  
		Size: 141.6 MB (141602673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce7ca591ce59226feabf12de023349866551184c68e2e102fe522b32496a008`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ef09230e4836d994bbe5443402cc90ef111b6f73ca6f76bab13170c36f853f`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c625ca81d187d83be46a1890b904f7a7217a8bfe819bb44172ff6eb35299dbf`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86a2945cbff6e172e884ea3d417becb92421dc5bfe36fb7a44c20ccaf7df9bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee8ade4d8aa3b9136d6604417a36f0141161876e30640d194d7a8328b96ae70`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.6.70` - unknown; unknown

```console
$ docker pull clickhouse@sha256:21243244872f6c180cc0540daf6c78a7563153542ab8a4569a42ef6e6cf86fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e098533a234612bdb0324e86fa5b658021558488e993e0b47f1e4349a1096d38`

```dockerfile
```

-	Layers:
	-	`sha256:6e00efd847634f80df847d3d9a293f3653c937f4d22714d0574aeaf2755183e2`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.6.70` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:232efe54fed33fb29e34d26048cda3acdf546796dd1c025e0b130b1acc0c2364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172169371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193563e3cedf52c1cf0fac821d51c7f6027324022fde1b5acc3e709a6d8d07e7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6948cfea4a51c536096b2b78d89558f999dc084aafe6d0a64ad270d500c584a3`  
		Last Modified: Tue, 12 Nov 2024 01:08:40 GMT  
		Size: 136.7 MB (136665946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae1e740a57e967033425e15cbbef58623f580e3e05eaa488af2549150489016`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca632dae928fb1896852c1fb89b6c1e5cdf2e934a59b4e94165c64241f35478`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49220562a2798401ef2a70bfba4f678a869b1627ab96f492fba656704002f582`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c29b785e3f2042e0c04eb6997fad37c4f703ac19a8f81c07b45531dc26e42d`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438b90cdb70d964cf18a00c838bcbe410cb2b74a1fa57cf456fda21c4f0903a4`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.6.70` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ddfe734a1c712615ee3d0127f21f4b191885287ccf44661a20ceebeec233d98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0e80c78377cd8a46ca655d9b51e98396c3a1b41c98720ddd0880a3067768ac`

```dockerfile
```

-	Layers:
	-	`sha256:d1a1a00d2596db9b2273ff26bbaca213308822cf8e26ab1c6cf979bc6ca32b96`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.6.70-focal`

```console
$ docker pull clickhouse@sha256:483935440135426977c106678d8e66a62cc35d6789d46da88404ab1fc5a381c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.6.70-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:cdc811aae31208585fa3fb4f4f12a3d3acf32c4e26101f92ce8f563a605cd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178783594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af14c36eab65d777010e7558f8c267935cf981ffb70df18f651c6b505848103`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b07dd07e1b82d4c98112e85407bd268cf85766f2c34d147b20651183802910`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 8.8 MB (8802576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f45f27d0be4d81ed312ac77c0769ecc8a26ebe5a2f89fe1a5411013b124944`  
		Last Modified: Tue, 12 Nov 2024 00:55:49 GMT  
		Size: 141.6 MB (141602673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce7ca591ce59226feabf12de023349866551184c68e2e102fe522b32496a008`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ef09230e4836d994bbe5443402cc90ef111b6f73ca6f76bab13170c36f853f`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c625ca81d187d83be46a1890b904f7a7217a8bfe819bb44172ff6eb35299dbf`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86a2945cbff6e172e884ea3d417becb92421dc5bfe36fb7a44c20ccaf7df9bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee8ade4d8aa3b9136d6604417a36f0141161876e30640d194d7a8328b96ae70`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.6.70-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:21243244872f6c180cc0540daf6c78a7563153542ab8a4569a42ef6e6cf86fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e098533a234612bdb0324e86fa5b658021558488e993e0b47f1e4349a1096d38`

```dockerfile
```

-	Layers:
	-	`sha256:6e00efd847634f80df847d3d9a293f3653c937f4d22714d0574aeaf2755183e2`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.6.70-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:232efe54fed33fb29e34d26048cda3acdf546796dd1c025e0b130b1acc0c2364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172169371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193563e3cedf52c1cf0fac821d51c7f6027324022fde1b5acc3e709a6d8d07e7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6948cfea4a51c536096b2b78d89558f999dc084aafe6d0a64ad270d500c584a3`  
		Last Modified: Tue, 12 Nov 2024 01:08:40 GMT  
		Size: 136.7 MB (136665946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae1e740a57e967033425e15cbbef58623f580e3e05eaa488af2549150489016`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca632dae928fb1896852c1fb89b6c1e5cdf2e934a59b4e94165c64241f35478`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49220562a2798401ef2a70bfba4f678a869b1627ab96f492fba656704002f582`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c29b785e3f2042e0c04eb6997fad37c4f703ac19a8f81c07b45531dc26e42d`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438b90cdb70d964cf18a00c838bcbe410cb2b74a1fa57cf456fda21c4f0903a4`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.6.70-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ddfe734a1c712615ee3d0127f21f4b191885287ccf44661a20ceebeec233d98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0e80c78377cd8a46ca655d9b51e98396c3a1b41c98720ddd0880a3067768ac`

```dockerfile
```

-	Layers:
	-	`sha256:d1a1a00d2596db9b2273ff26bbaca213308822cf8e26ab1c6cf979bc6ca32b96`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.9`

```console
$ docker pull clickhouse@sha256:a4c1e4a9897de86216d9cea74acc1796d2e678698c704aae376cb6131618123a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.9` - linux; amd64

```console
$ docker pull clickhouse@sha256:ae9b0d3d63d3d35aa0113a2a38063a10840ebc0f37e87fb362740971f0521e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181386353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797296700c3fcc096d888f8695ac176c5c33d248a6d5623d38e691ded69f6356`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.9.2.42
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e68efb36e419c9ae1ea4abc884c927fd41b3b6882420f53b60c1954dc6cd314`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 8.8 MB (8802641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59482d5b9e8ac2275b7beacb6480996f8cd17ce43d0889428ed38d8ab5f7f38`  
		Last Modified: Tue, 12 Nov 2024 00:55:43 GMT  
		Size: 144.2 MB (144205372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859a0e6cfc617c6d9273e2eb2bbb4dce205345e81959323a66dc490f3e61dfcf`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48af0c00d3ecb9124aefb75aafeeff66caeed524790e65ba7efbe3d6000006e`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1285251c75b3b6f72a0d1ff0fc9381e5f064899820ba81091314bf284533ec`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f6ba6c98f4885d8fad2ae658a77d668456ae07badd4e3dadacb49ce8d96dee`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9028d92b314d2596e2d3f5ce617257a35c38a1d2e79ba962357a2741963df81a`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:479224fc13cc78d123e923233199190e76a883373000ce7dde3d1869f096a402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f7318cc7d666c8f431be751b0b881d1e1442a837eab71946ca1e4270528d4e`

```dockerfile
```

-	Layers:
	-	`sha256:509647db4ed48d459339826f0d270211db4eac76ed3f2e57d160ee7cc8836ffa`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.9` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:368cbcd37206ebf95468318546259ebb796c2d1d295d31ea980b6df80ad64ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174393866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3914cdd99af870b7975a77088bf91e5f1440e73f9836f26aa420ecde6878b92a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.9.2.42
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cd409aa7a2dc0bb2030b168d4d164e6e7b569de28f07716b37b8b2b27bfc96`  
		Last Modified: Tue, 12 Nov 2024 01:07:49 GMT  
		Size: 138.9 MB (138890440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b9ff1aef9a175262e6028b4451b9bb3fd931b2a590b7771f393534756e9b02`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1735bf61434f2c3d5e2b69c84b035080c356cd05e3c7d7e364fa72146ca0b7d`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015af92968bb35cf6a9f3d3da9ffcc1247793a951f2cae23f4df58feb5a5b935`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fbce02053b8c546bea00f06df6024c96893880d917af9ac6bcff5c86dfa76e`  
		Last Modified: Tue, 12 Nov 2024 01:07:47 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9cca3930b6fe8cec4b1788f45fa096342d3460e07668dd60ac57de4211bca8`  
		Last Modified: Tue, 12 Nov 2024 01:07:47 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:07174820d710f6b3657b9b6a47e4066cadcd9606279952ec166a8eaf5106b049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b85815816540b5849b962fce81e36f5c6f6d66171aafa98fde573178598d17`

```dockerfile
```

-	Layers:
	-	`sha256:f0731053bbad48baf1fcce8c7676743469de10d412e08553f912d0d80732e09b`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.9-focal`

```console
$ docker pull clickhouse@sha256:a4c1e4a9897de86216d9cea74acc1796d2e678698c704aae376cb6131618123a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.9-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:ae9b0d3d63d3d35aa0113a2a38063a10840ebc0f37e87fb362740971f0521e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181386353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797296700c3fcc096d888f8695ac176c5c33d248a6d5623d38e691ded69f6356`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.9.2.42
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e68efb36e419c9ae1ea4abc884c927fd41b3b6882420f53b60c1954dc6cd314`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 8.8 MB (8802641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59482d5b9e8ac2275b7beacb6480996f8cd17ce43d0889428ed38d8ab5f7f38`  
		Last Modified: Tue, 12 Nov 2024 00:55:43 GMT  
		Size: 144.2 MB (144205372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859a0e6cfc617c6d9273e2eb2bbb4dce205345e81959323a66dc490f3e61dfcf`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48af0c00d3ecb9124aefb75aafeeff66caeed524790e65ba7efbe3d6000006e`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1285251c75b3b6f72a0d1ff0fc9381e5f064899820ba81091314bf284533ec`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f6ba6c98f4885d8fad2ae658a77d668456ae07badd4e3dadacb49ce8d96dee`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9028d92b314d2596e2d3f5ce617257a35c38a1d2e79ba962357a2741963df81a`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:479224fc13cc78d123e923233199190e76a883373000ce7dde3d1869f096a402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f7318cc7d666c8f431be751b0b881d1e1442a837eab71946ca1e4270528d4e`

```dockerfile
```

-	Layers:
	-	`sha256:509647db4ed48d459339826f0d270211db4eac76ed3f2e57d160ee7cc8836ffa`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.9-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:368cbcd37206ebf95468318546259ebb796c2d1d295d31ea980b6df80ad64ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174393866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3914cdd99af870b7975a77088bf91e5f1440e73f9836f26aa420ecde6878b92a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.9.2.42
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cd409aa7a2dc0bb2030b168d4d164e6e7b569de28f07716b37b8b2b27bfc96`  
		Last Modified: Tue, 12 Nov 2024 01:07:49 GMT  
		Size: 138.9 MB (138890440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b9ff1aef9a175262e6028b4451b9bb3fd931b2a590b7771f393534756e9b02`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1735bf61434f2c3d5e2b69c84b035080c356cd05e3c7d7e364fa72146ca0b7d`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015af92968bb35cf6a9f3d3da9ffcc1247793a951f2cae23f4df58feb5a5b935`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fbce02053b8c546bea00f06df6024c96893880d917af9ac6bcff5c86dfa76e`  
		Last Modified: Tue, 12 Nov 2024 01:07:47 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9cca3930b6fe8cec4b1788f45fa096342d3460e07668dd60ac57de4211bca8`  
		Last Modified: Tue, 12 Nov 2024 01:07:47 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:07174820d710f6b3657b9b6a47e4066cadcd9606279952ec166a8eaf5106b049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b85815816540b5849b962fce81e36f5c6f6d66171aafa98fde573178598d17`

```dockerfile
```

-	Layers:
	-	`sha256:f0731053bbad48baf1fcce8c7676743469de10d412e08553f912d0d80732e09b`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.9.2`

```console
$ docker pull clickhouse@sha256:a4c1e4a9897de86216d9cea74acc1796d2e678698c704aae376cb6131618123a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.9.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:ae9b0d3d63d3d35aa0113a2a38063a10840ebc0f37e87fb362740971f0521e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181386353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797296700c3fcc096d888f8695ac176c5c33d248a6d5623d38e691ded69f6356`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.9.2.42
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e68efb36e419c9ae1ea4abc884c927fd41b3b6882420f53b60c1954dc6cd314`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 8.8 MB (8802641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59482d5b9e8ac2275b7beacb6480996f8cd17ce43d0889428ed38d8ab5f7f38`  
		Last Modified: Tue, 12 Nov 2024 00:55:43 GMT  
		Size: 144.2 MB (144205372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859a0e6cfc617c6d9273e2eb2bbb4dce205345e81959323a66dc490f3e61dfcf`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48af0c00d3ecb9124aefb75aafeeff66caeed524790e65ba7efbe3d6000006e`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1285251c75b3b6f72a0d1ff0fc9381e5f064899820ba81091314bf284533ec`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f6ba6c98f4885d8fad2ae658a77d668456ae07badd4e3dadacb49ce8d96dee`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9028d92b314d2596e2d3f5ce617257a35c38a1d2e79ba962357a2741963df81a`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:479224fc13cc78d123e923233199190e76a883373000ce7dde3d1869f096a402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f7318cc7d666c8f431be751b0b881d1e1442a837eab71946ca1e4270528d4e`

```dockerfile
```

-	Layers:
	-	`sha256:509647db4ed48d459339826f0d270211db4eac76ed3f2e57d160ee7cc8836ffa`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.9.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:368cbcd37206ebf95468318546259ebb796c2d1d295d31ea980b6df80ad64ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174393866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3914cdd99af870b7975a77088bf91e5f1440e73f9836f26aa420ecde6878b92a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.9.2.42
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cd409aa7a2dc0bb2030b168d4d164e6e7b569de28f07716b37b8b2b27bfc96`  
		Last Modified: Tue, 12 Nov 2024 01:07:49 GMT  
		Size: 138.9 MB (138890440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b9ff1aef9a175262e6028b4451b9bb3fd931b2a590b7771f393534756e9b02`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1735bf61434f2c3d5e2b69c84b035080c356cd05e3c7d7e364fa72146ca0b7d`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015af92968bb35cf6a9f3d3da9ffcc1247793a951f2cae23f4df58feb5a5b935`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fbce02053b8c546bea00f06df6024c96893880d917af9ac6bcff5c86dfa76e`  
		Last Modified: Tue, 12 Nov 2024 01:07:47 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9cca3930b6fe8cec4b1788f45fa096342d3460e07668dd60ac57de4211bca8`  
		Last Modified: Tue, 12 Nov 2024 01:07:47 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:07174820d710f6b3657b9b6a47e4066cadcd9606279952ec166a8eaf5106b049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b85815816540b5849b962fce81e36f5c6f6d66171aafa98fde573178598d17`

```dockerfile
```

-	Layers:
	-	`sha256:f0731053bbad48baf1fcce8c7676743469de10d412e08553f912d0d80732e09b`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.9.2-focal`

```console
$ docker pull clickhouse@sha256:a4c1e4a9897de86216d9cea74acc1796d2e678698c704aae376cb6131618123a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.9.2-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:ae9b0d3d63d3d35aa0113a2a38063a10840ebc0f37e87fb362740971f0521e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181386353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797296700c3fcc096d888f8695ac176c5c33d248a6d5623d38e691ded69f6356`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.9.2.42
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e68efb36e419c9ae1ea4abc884c927fd41b3b6882420f53b60c1954dc6cd314`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 8.8 MB (8802641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59482d5b9e8ac2275b7beacb6480996f8cd17ce43d0889428ed38d8ab5f7f38`  
		Last Modified: Tue, 12 Nov 2024 00:55:43 GMT  
		Size: 144.2 MB (144205372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859a0e6cfc617c6d9273e2eb2bbb4dce205345e81959323a66dc490f3e61dfcf`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48af0c00d3ecb9124aefb75aafeeff66caeed524790e65ba7efbe3d6000006e`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1285251c75b3b6f72a0d1ff0fc9381e5f064899820ba81091314bf284533ec`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f6ba6c98f4885d8fad2ae658a77d668456ae07badd4e3dadacb49ce8d96dee`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9028d92b314d2596e2d3f5ce617257a35c38a1d2e79ba962357a2741963df81a`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9.2-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:479224fc13cc78d123e923233199190e76a883373000ce7dde3d1869f096a402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f7318cc7d666c8f431be751b0b881d1e1442a837eab71946ca1e4270528d4e`

```dockerfile
```

-	Layers:
	-	`sha256:509647db4ed48d459339826f0d270211db4eac76ed3f2e57d160ee7cc8836ffa`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.9.2-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:368cbcd37206ebf95468318546259ebb796c2d1d295d31ea980b6df80ad64ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174393866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3914cdd99af870b7975a77088bf91e5f1440e73f9836f26aa420ecde6878b92a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.9.2.42
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cd409aa7a2dc0bb2030b168d4d164e6e7b569de28f07716b37b8b2b27bfc96`  
		Last Modified: Tue, 12 Nov 2024 01:07:49 GMT  
		Size: 138.9 MB (138890440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b9ff1aef9a175262e6028b4451b9bb3fd931b2a590b7771f393534756e9b02`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1735bf61434f2c3d5e2b69c84b035080c356cd05e3c7d7e364fa72146ca0b7d`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015af92968bb35cf6a9f3d3da9ffcc1247793a951f2cae23f4df58feb5a5b935`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fbce02053b8c546bea00f06df6024c96893880d917af9ac6bcff5c86dfa76e`  
		Last Modified: Tue, 12 Nov 2024 01:07:47 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9cca3930b6fe8cec4b1788f45fa096342d3460e07668dd60ac57de4211bca8`  
		Last Modified: Tue, 12 Nov 2024 01:07:47 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9.2-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:07174820d710f6b3657b9b6a47e4066cadcd9606279952ec166a8eaf5106b049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b85815816540b5849b962fce81e36f5c6f6d66171aafa98fde573178598d17`

```dockerfile
```

-	Layers:
	-	`sha256:f0731053bbad48baf1fcce8c7676743469de10d412e08553f912d0d80732e09b`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.9.2.42`

```console
$ docker pull clickhouse@sha256:a4c1e4a9897de86216d9cea74acc1796d2e678698c704aae376cb6131618123a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.9.2.42` - linux; amd64

```console
$ docker pull clickhouse@sha256:ae9b0d3d63d3d35aa0113a2a38063a10840ebc0f37e87fb362740971f0521e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181386353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797296700c3fcc096d888f8695ac176c5c33d248a6d5623d38e691ded69f6356`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.9.2.42
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e68efb36e419c9ae1ea4abc884c927fd41b3b6882420f53b60c1954dc6cd314`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 8.8 MB (8802641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59482d5b9e8ac2275b7beacb6480996f8cd17ce43d0889428ed38d8ab5f7f38`  
		Last Modified: Tue, 12 Nov 2024 00:55:43 GMT  
		Size: 144.2 MB (144205372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859a0e6cfc617c6d9273e2eb2bbb4dce205345e81959323a66dc490f3e61dfcf`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48af0c00d3ecb9124aefb75aafeeff66caeed524790e65ba7efbe3d6000006e`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1285251c75b3b6f72a0d1ff0fc9381e5f064899820ba81091314bf284533ec`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f6ba6c98f4885d8fad2ae658a77d668456ae07badd4e3dadacb49ce8d96dee`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9028d92b314d2596e2d3f5ce617257a35c38a1d2e79ba962357a2741963df81a`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9.2.42` - unknown; unknown

```console
$ docker pull clickhouse@sha256:479224fc13cc78d123e923233199190e76a883373000ce7dde3d1869f096a402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f7318cc7d666c8f431be751b0b881d1e1442a837eab71946ca1e4270528d4e`

```dockerfile
```

-	Layers:
	-	`sha256:509647db4ed48d459339826f0d270211db4eac76ed3f2e57d160ee7cc8836ffa`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.9.2.42` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:368cbcd37206ebf95468318546259ebb796c2d1d295d31ea980b6df80ad64ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174393866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3914cdd99af870b7975a77088bf91e5f1440e73f9836f26aa420ecde6878b92a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.9.2.42
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cd409aa7a2dc0bb2030b168d4d164e6e7b569de28f07716b37b8b2b27bfc96`  
		Last Modified: Tue, 12 Nov 2024 01:07:49 GMT  
		Size: 138.9 MB (138890440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b9ff1aef9a175262e6028b4451b9bb3fd931b2a590b7771f393534756e9b02`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1735bf61434f2c3d5e2b69c84b035080c356cd05e3c7d7e364fa72146ca0b7d`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015af92968bb35cf6a9f3d3da9ffcc1247793a951f2cae23f4df58feb5a5b935`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fbce02053b8c546bea00f06df6024c96893880d917af9ac6bcff5c86dfa76e`  
		Last Modified: Tue, 12 Nov 2024 01:07:47 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9cca3930b6fe8cec4b1788f45fa096342d3460e07668dd60ac57de4211bca8`  
		Last Modified: Tue, 12 Nov 2024 01:07:47 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9.2.42` - unknown; unknown

```console
$ docker pull clickhouse@sha256:07174820d710f6b3657b9b6a47e4066cadcd9606279952ec166a8eaf5106b049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b85815816540b5849b962fce81e36f5c6f6d66171aafa98fde573178598d17`

```dockerfile
```

-	Layers:
	-	`sha256:f0731053bbad48baf1fcce8c7676743469de10d412e08553f912d0d80732e09b`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.9.2.42-focal`

```console
$ docker pull clickhouse@sha256:a4c1e4a9897de86216d9cea74acc1796d2e678698c704aae376cb6131618123a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.9.2.42-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:ae9b0d3d63d3d35aa0113a2a38063a10840ebc0f37e87fb362740971f0521e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.4 MB (181386353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797296700c3fcc096d888f8695ac176c5c33d248a6d5623d38e691ded69f6356`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.9.2.42
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e68efb36e419c9ae1ea4abc884c927fd41b3b6882420f53b60c1954dc6cd314`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 8.8 MB (8802641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59482d5b9e8ac2275b7beacb6480996f8cd17ce43d0889428ed38d8ab5f7f38`  
		Last Modified: Tue, 12 Nov 2024 00:55:43 GMT  
		Size: 144.2 MB (144205372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859a0e6cfc617c6d9273e2eb2bbb4dce205345e81959323a66dc490f3e61dfcf`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48af0c00d3ecb9124aefb75aafeeff66caeed524790e65ba7efbe3d6000006e`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1285251c75b3b6f72a0d1ff0fc9381e5f064899820ba81091314bf284533ec`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f6ba6c98f4885d8fad2ae658a77d668456ae07badd4e3dadacb49ce8d96dee`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9028d92b314d2596e2d3f5ce617257a35c38a1d2e79ba962357a2741963df81a`  
		Last Modified: Tue, 12 Nov 2024 00:55:42 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9.2.42-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:479224fc13cc78d123e923233199190e76a883373000ce7dde3d1869f096a402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95f7318cc7d666c8f431be751b0b881d1e1442a837eab71946ca1e4270528d4e`

```dockerfile
```

-	Layers:
	-	`sha256:509647db4ed48d459339826f0d270211db4eac76ed3f2e57d160ee7cc8836ffa`  
		Last Modified: Tue, 12 Nov 2024 00:55:41 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.9.2.42-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:368cbcd37206ebf95468318546259ebb796c2d1d295d31ea980b6df80ad64ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.4 MB (174393866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3914cdd99af870b7975a77088bf91e5f1440e73f9836f26aa420ecde6878b92a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.9.2.42
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.2.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4cd409aa7a2dc0bb2030b168d4d164e6e7b569de28f07716b37b8b2b27bfc96`  
		Last Modified: Tue, 12 Nov 2024 01:07:49 GMT  
		Size: 138.9 MB (138890440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b9ff1aef9a175262e6028b4451b9bb3fd931b2a590b7771f393534756e9b02`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1735bf61434f2c3d5e2b69c84b035080c356cd05e3c7d7e364fa72146ca0b7d`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015af92968bb35cf6a9f3d3da9ffcc1247793a951f2cae23f4df58feb5a5b935`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fbce02053b8c546bea00f06df6024c96893880d917af9ac6bcff5c86dfa76e`  
		Last Modified: Tue, 12 Nov 2024 01:07:47 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9cca3930b6fe8cec4b1788f45fa096342d3460e07668dd60ac57de4211bca8`  
		Last Modified: Tue, 12 Nov 2024 01:07:47 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9.2.42-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:07174820d710f6b3657b9b6a47e4066cadcd9606279952ec166a8eaf5106b049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b85815816540b5849b962fce81e36f5c6f6d66171aafa98fde573178598d17`

```dockerfile
```

-	Layers:
	-	`sha256:f0731053bbad48baf1fcce8c7676743469de10d412e08553f912d0d80732e09b`  
		Last Modified: Tue, 12 Nov 2024 01:07:46 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:focal`

```console
$ docker pull clickhouse@sha256:7bc9fa5ec703a95ffd5a2c6a271dab034aa0637dbc2fefbd5fc57e3283bec064
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:be2eb6602bb634c641a26de50062bc6db4a413fc5f8e2d30d69e63ae218c9300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180502273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780779b097fba8e76a39d39f0f34ce2e5bd628429919a69180f6c2f235a7e799`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111f8833bc453e9ec8c2ebf32ac32b825681a3b9b8e372c9e3398f52bb2d7bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 8.8 MB (8802605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c21f8f8706bb6e315bd1248a431189fb5403141581d2dd8c747495194028dc0`  
		Last Modified: Tue, 12 Nov 2024 00:55:36 GMT  
		Size: 143.3 MB (143321321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4048caa8e9536cbc81bd812da3ddbfcf0c242bc84e0aae8e5b62218311ada6f`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cef3cb7c9b8b7831050f192376fb3ec2e596319cbb7f00ab13fac740d9b429`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7326086bcd43354f495c22f41a1362e035b86efb1231658cc777d828e06c09b5`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0c972525eaadda0b5d220a60713fe6ae4aed202d0ce097494dd54d4cbddf88`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab0e4e89c886c68156494d0d15588424bdb261b6c099366489de19a967e3ea`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30fec73f163c700239a92f41e19b9f40da215af99c5ca19bc44ce23749fe999b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c0598285c843a368616c4153906d3ac3f653d3bfb236c35369f61c93ff8f72`

```dockerfile
```

-	Layers:
	-	`sha256:1e1412d68f0c82d49f7df302740602685430eae38a51dff2f5622494b8ef7716`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 26.5 KB (26526 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6eae6f07acede5586409eb0529970b5e8bbb650dbaf17e39c4efbb144757a6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174163120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d854e5fd0220b4126259e851b7ba390e22ab2b139704525b4329d29c0a7db8e3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f0a0c59e6c74754aaf916f8b6df9f98cffb99cb60e3ff6958bfafbe40c7254`  
		Last Modified: Tue, 12 Nov 2024 01:06:54 GMT  
		Size: 138.7 MB (138659691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adb863b4b4c69d8d08447ff2f92bde3bf58985fd69c6d0272273bfe6c682c8a`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d046b9b6fb2887e045118fa7b549f271dd6834e27a1a81bec062a420becc2333`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79602d6db082d0d6dd1cc2f9451cf185d6d2ae4746da01fcbbddfe11250b70ce`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9521f306a3451bfc3d658df655e47b14b6dfe1fa8a4ee01fa7239d256513d150`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7419c1b0b1b714719c8c0457161ee358c44e630ee2c264733dad78f1f666faa`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:53da8ae3932d2be58b4497df239aa92f12380d79a3046061686fb1473f1c482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c2a42d0eb4773da3eb4d1f61c94f4652b79ba86145e6503c285a87d063c446`

```dockerfile
```

-	Layers:
	-	`sha256:8a15f595e98190849d608ae4aaf07c44b896636f633ab5818e0c64c15671d1a2`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 26.8 KB (26762 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:focal-lts`

```console
$ docker pull clickhouse@sha256:483935440135426977c106678d8e66a62cc35d6789d46da88404ab1fc5a381c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:focal-lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:cdc811aae31208585fa3fb4f4f12a3d3acf32c4e26101f92ce8f563a605cd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178783594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af14c36eab65d777010e7558f8c267935cf981ffb70df18f651c6b505848103`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b07dd07e1b82d4c98112e85407bd268cf85766f2c34d147b20651183802910`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 8.8 MB (8802576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f45f27d0be4d81ed312ac77c0769ecc8a26ebe5a2f89fe1a5411013b124944`  
		Last Modified: Tue, 12 Nov 2024 00:55:49 GMT  
		Size: 141.6 MB (141602673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce7ca591ce59226feabf12de023349866551184c68e2e102fe522b32496a008`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ef09230e4836d994bbe5443402cc90ef111b6f73ca6f76bab13170c36f853f`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c625ca81d187d83be46a1890b904f7a7217a8bfe819bb44172ff6eb35299dbf`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86a2945cbff6e172e884ea3d417becb92421dc5bfe36fb7a44c20ccaf7df9bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee8ade4d8aa3b9136d6604417a36f0141161876e30640d194d7a8328b96ae70`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:focal-lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:21243244872f6c180cc0540daf6c78a7563153542ab8a4569a42ef6e6cf86fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e098533a234612bdb0324e86fa5b658021558488e993e0b47f1e4349a1096d38`

```dockerfile
```

-	Layers:
	-	`sha256:6e00efd847634f80df847d3d9a293f3653c937f4d22714d0574aeaf2755183e2`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:focal-lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:232efe54fed33fb29e34d26048cda3acdf546796dd1c025e0b130b1acc0c2364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172169371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193563e3cedf52c1cf0fac821d51c7f6027324022fde1b5acc3e709a6d8d07e7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6948cfea4a51c536096b2b78d89558f999dc084aafe6d0a64ad270d500c584a3`  
		Last Modified: Tue, 12 Nov 2024 01:08:40 GMT  
		Size: 136.7 MB (136665946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae1e740a57e967033425e15cbbef58623f580e3e05eaa488af2549150489016`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca632dae928fb1896852c1fb89b6c1e5cdf2e934a59b4e94165c64241f35478`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49220562a2798401ef2a70bfba4f678a869b1627ab96f492fba656704002f582`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c29b785e3f2042e0c04eb6997fad37c4f703ac19a8f81c07b45531dc26e42d`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438b90cdb70d964cf18a00c838bcbe410cb2b74a1fa57cf456fda21c4f0903a4`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:focal-lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ddfe734a1c712615ee3d0127f21f4b191885287ccf44661a20ceebeec233d98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0e80c78377cd8a46ca655d9b51e98396c3a1b41c98720ddd0880a3067768ac`

```dockerfile
```

-	Layers:
	-	`sha256:d1a1a00d2596db9b2273ff26bbaca213308822cf8e26ab1c6cf979bc6ca32b96`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:7bc9fa5ec703a95ffd5a2c6a271dab034aa0637dbc2fefbd5fc57e3283bec064
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:be2eb6602bb634c641a26de50062bc6db4a413fc5f8e2d30d69e63ae218c9300
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.5 MB (180502273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780779b097fba8e76a39d39f0f34ce2e5bd628429919a69180f6c2f235a7e799`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7111f8833bc453e9ec8c2ebf32ac32b825681a3b9b8e372c9e3398f52bb2d7bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 8.8 MB (8802605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c21f8f8706bb6e315bd1248a431189fb5403141581d2dd8c747495194028dc0`  
		Last Modified: Tue, 12 Nov 2024 00:55:36 GMT  
		Size: 143.3 MB (143321321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4048caa8e9536cbc81bd812da3ddbfcf0c242bc84e0aae8e5b62218311ada6f`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18cef3cb7c9b8b7831050f192376fb3ec2e596319cbb7f00ab13fac740d9b429`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7326086bcd43354f495c22f41a1362e035b86efb1231658cc777d828e06c09b5`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0c972525eaadda0b5d220a60713fe6ae4aed202d0ce097494dd54d4cbddf88`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaab0e4e89c886c68156494d0d15588424bdb261b6c099366489de19a967e3ea`  
		Last Modified: Tue, 12 Nov 2024 00:55:35 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:30fec73f163c700239a92f41e19b9f40da215af99c5ca19bc44ce23749fe999b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c0598285c843a368616c4153906d3ac3f653d3bfb236c35369f61c93ff8f72`

```dockerfile
```

-	Layers:
	-	`sha256:1e1412d68f0c82d49f7df302740602685430eae38a51dff2f5622494b8ef7716`  
		Last Modified: Tue, 12 Nov 2024 00:55:34 GMT  
		Size: 26.5 KB (26526 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6eae6f07acede5586409eb0529970b5e8bbb650dbaf17e39c4efbb144757a6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174163120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d854e5fd0220b4126259e851b7ba390e22ab2b139704525b4329d29c0a7db8e3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.10.1.2812
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.1.2812 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f0a0c59e6c74754aaf916f8b6df9f98cffb99cb60e3ff6958bfafbe40c7254`  
		Last Modified: Tue, 12 Nov 2024 01:06:54 GMT  
		Size: 138.7 MB (138659691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adb863b4b4c69d8d08447ff2f92bde3bf58985fd69c6d0272273bfe6c682c8a`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d046b9b6fb2887e045118fa7b549f271dd6834e27a1a81bec062a420becc2333`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79602d6db082d0d6dd1cc2f9451cf185d6d2ae4746da01fcbbddfe11250b70ce`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9521f306a3451bfc3d658df655e47b14b6dfe1fa8a4ee01fa7239d256513d150`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7419c1b0b1b714719c8c0457161ee358c44e630ee2c264733dad78f1f666faa`  
		Last Modified: Tue, 12 Nov 2024 01:06:52 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:53da8ae3932d2be58b4497df239aa92f12380d79a3046061686fb1473f1c482f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50c2a42d0eb4773da3eb4d1f61c94f4652b79ba86145e6503c285a87d063c446`

```dockerfile
```

-	Layers:
	-	`sha256:8a15f595e98190849d608ae4aaf07c44b896636f633ab5818e0c64c15671d1a2`  
		Last Modified: Tue, 12 Nov 2024 01:06:50 GMT  
		Size: 26.8 KB (26762 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:483935440135426977c106678d8e66a62cc35d6789d46da88404ab1fc5a381c3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:cdc811aae31208585fa3fb4f4f12a3d3acf32c4e26101f92ce8f563a605cd37a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178783594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8af14c36eab65d777010e7558f8c267935cf981ffb70df18f651c6b505848103`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85b07dd07e1b82d4c98112e85407bd268cf85766f2c34d147b20651183802910`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 8.8 MB (8802576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f45f27d0be4d81ed312ac77c0769ecc8a26ebe5a2f89fe1a5411013b124944`  
		Last Modified: Tue, 12 Nov 2024 00:55:49 GMT  
		Size: 141.6 MB (141602673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce7ca591ce59226feabf12de023349866551184c68e2e102fe522b32496a008`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ef09230e4836d994bbe5443402cc90ef111b6f73ca6f76bab13170c36f853f`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c625ca81d187d83be46a1890b904f7a7217a8bfe819bb44172ff6eb35299dbf`  
		Last Modified: Tue, 12 Nov 2024 00:55:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86a2945cbff6e172e884ea3d417becb92421dc5bfe36fb7a44c20ccaf7df9bc`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee8ade4d8aa3b9136d6604417a36f0141161876e30640d194d7a8328b96ae70`  
		Last Modified: Tue, 12 Nov 2024 00:55:48 GMT  
		Size: 3.1 KB (3144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:21243244872f6c180cc0540daf6c78a7563153542ab8a4569a42ef6e6cf86fb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e098533a234612bdb0324e86fa5b658021558488e993e0b47f1e4349a1096d38`

```dockerfile
```

-	Layers:
	-	`sha256:6e00efd847634f80df847d3d9a293f3653c937f4d22714d0574aeaf2755183e2`  
		Last Modified: Tue, 12 Nov 2024 00:55:46 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:232efe54fed33fb29e34d26048cda3acdf546796dd1c025e0b130b1acc0c2364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172169371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193563e3cedf52c1cf0fac821d51c7f6027324022fde1b5acc3e709a6d8d07e7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:39:45 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:39:45 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:39:45 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:39:47 GMT
ADD file:8537b4db344382b39d669af27cd94ec0f870ceafe58c67ee54e3f9b38fb8d671 in / 
# Fri, 11 Oct 2024 03:39:47 GMT
CMD ["/bin/bash"]
# Sun, 10 Nov 2024 19:13:47 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Sun, 10 Nov 2024 19:13:47 GMT
ARG apt_archive=http://archive.ubuntu.com
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPO_CHANNEL=stable
# Sun, 10 Nov 2024 19:13:47 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Sun, 10 Nov 2024 19:13:47 GMT
ARG VERSION=24.8.6.70
# Sun, 10 Nov 2024 19:13:47 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
ENV LANG=en_US.UTF-8
# Sun, 10 Nov 2024 19:13:47 GMT
ENV TZ=UTC
# Sun, 10 Nov 2024 19:13:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.6.70 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Sun, 10 Nov 2024 19:13:47 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Sun, 10 Nov 2024 19:13:47 GMT
VOLUME [/var/lib/clickhouse]
# Sun, 10 Nov 2024 19:13:47 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Sun, 10 Nov 2024 19:13:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ba974f84eb2fc21ccc6b14da8a5b6116a1131bd64b71ae6fb6023c06759053`  
		Last Modified: Tue, 12 Nov 2024 01:06:51 GMT  
		Size: 8.7 MB (8662321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6948cfea4a51c536096b2b78d89558f999dc084aafe6d0a64ad270d500c584a3`  
		Last Modified: Tue, 12 Nov 2024 01:08:40 GMT  
		Size: 136.7 MB (136665946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae1e740a57e967033425e15cbbef58623f580e3e05eaa488af2549150489016`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca632dae928fb1896852c1fb89b6c1e5cdf2e934a59b4e94165c64241f35478`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49220562a2798401ef2a70bfba4f678a869b1627ab96f492fba656704002f582`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c29b785e3f2042e0c04eb6997fad37c4f703ac19a8f81c07b45531dc26e42d`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438b90cdb70d964cf18a00c838bcbe410cb2b74a1fa57cf456fda21c4f0903a4`  
		Last Modified: Tue, 12 Nov 2024 01:08:38 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ddfe734a1c712615ee3d0127f21f4b191885287ccf44661a20ceebeec233d98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb0e80c78377cd8a46ca655d9b51e98396c3a1b41c98720ddd0880a3067768ac`

```dockerfile
```

-	Layers:
	-	`sha256:d1a1a00d2596db9b2273ff26bbaca213308822cf8e26ab1c6cf979bc6ca32b96`  
		Last Modified: Tue, 12 Nov 2024 01:08:37 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json
