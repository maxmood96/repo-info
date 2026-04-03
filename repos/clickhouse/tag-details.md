<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.21`](#clickhouse25821)
-	[`clickhouse:25.8.21-jammy`](#clickhouse25821-jammy)
-	[`clickhouse:25.8.21.7`](#clickhouse258217)
-	[`clickhouse:25.8.21.7-jammy`](#clickhouse258217-jammy)
-	[`clickhouse:26.1`](#clickhouse261)
-	[`clickhouse:26.1-jammy`](#clickhouse261-jammy)
-	[`clickhouse:26.1.7`](#clickhouse2617)
-	[`clickhouse:26.1.7-jammy`](#clickhouse2617-jammy)
-	[`clickhouse:26.1.7.13`](#clickhouse261713)
-	[`clickhouse:26.1.7.13-jammy`](#clickhouse261713-jammy)
-	[`clickhouse:26.2`](#clickhouse262)
-	[`clickhouse:26.2-jammy`](#clickhouse262-jammy)
-	[`clickhouse:26.2.7`](#clickhouse2627)
-	[`clickhouse:26.2.7-jammy`](#clickhouse2627-jammy)
-	[`clickhouse:26.2.7.17`](#clickhouse262717)
-	[`clickhouse:26.2.7.17-jammy`](#clickhouse262717-jammy)
-	[`clickhouse:26.3`](#clickhouse263)
-	[`clickhouse:26.3-jammy`](#clickhouse263-jammy)
-	[`clickhouse:26.3.3`](#clickhouse2633)
-	[`clickhouse:26.3.3-jammy`](#clickhouse2633-jammy)
-	[`clickhouse:26.3.3.20`](#clickhouse263320)
-	[`clickhouse:26.3.3.20-jammy`](#clickhouse263320-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:58e0e4f9f4ddd6840bddc1aa7a4a3f88d12e2ee040216fee50fc38b09565b884
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:ba6d0d08ccf4f32e24c08306b5c5945dbed755e42ccf4affefdfa254a4ebc280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229199929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efce1e3ffe173030f6b615b1d3435777d700320a579386fe5e69d889374bd3c2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:04 GMT
ARG VERSION=25.8.21.7
# Fri, 03 Apr 2026 16:46:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:30 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:30 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c405cf38316702974e718dbbd07eda14422d62e303fae7960fbaee9181a613d`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 7.6 MB (7599168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8b24ff35d307fb4bb43c39598fe990f47880d8680013e688386d04129cb4c9`  
		Last Modified: Fri, 03 Apr 2026 16:47:53 GMT  
		Size: 191.0 MB (190994325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd3f5bb4a70563fb0d4144e2c677e3ba05efdd409b5e2a2cc07133d5758fdd`  
		Last Modified: Fri, 03 Apr 2026 16:47:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051cf0dcaf87b85231342b8bee0d935d799eb6438f30b8176adaeffe9615156a`  
		Last Modified: Fri, 03 Apr 2026 16:47:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f002c854fda80c138e367007b9dc11b7b12148c5a9c7afb08315b89973924bb2`  
		Last Modified: Fri, 03 Apr 2026 16:47:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc491778644f694a3359437b40cf29c3bc1339cd37ccd68e38a2afc38ec8adb`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf1a01954f93a35a20adf2cfb7cfd424689e0fab1602577b54187eeb1a15131`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:34eec2b2db0fca0440fe5d8cc6bbf23d7a78d9e2ea75d5f14e482bcab886482c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1a98140197a194f029ee8228a60258282ade28f038370ff3e971b590ffb97`

```dockerfile
```

-	Layers:
	-	`sha256:af20e6927e3f7ac32892ef113f9ae398020be2074baffddf4f525db7a2972b65`  
		Last Modified: Fri, 03 Apr 2026 16:47:49 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e5f996c10f3c8cd53ac983c6363d16b08d9237fb1af6093a41be2c543b059875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214147489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405f4f114deb4e545b3b068d4d54516aaf725c46d5b9016583f253d7719203f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:57 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:57 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:57 GMT
ARG VERSION=25.8.21.7
# Fri, 03 Apr 2026 16:46:57 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:48:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:48:39 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:48:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:48:40 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:48:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:48:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c357252fe4ab6bd21b7ad7a9772aa8322cc2176c66f36f327bc72e995c27be74`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 7.6 MB (7578928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdad694ea1463318e46aae6bb784ac4187c33ee9d336af2b40216f9a59c859f`  
		Last Modified: Fri, 03 Apr 2026 16:49:02 GMT  
		Size: 178.1 MB (178091597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d6d6918cc917423e8958aea05ab808bb809aa75fb3b98a1703c8131b7d704a`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9abc5bcec96658f913e1eb9b0ef960f288a36cff723d1d36b8340e92faf8cd6`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253b8d977ba774cec1423754e8a8499256de1e48f0eaca9736181eccd953f14b`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95620ab76a1fe1ba4bfffb6516c3440927ccc9c6e5326ca265c7eaf75e6486ab`  
		Last Modified: Fri, 03 Apr 2026 16:48:59 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21717a7b1cd5bf759a01b74eab4368e5a519b74374e976d53aaf4facbd680fa2`  
		Last Modified: Fri, 03 Apr 2026 16:48:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b720516ad036276ef170ac1c74f82dad1d3d45f439f6b96748c1f1fca847ffda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077aaffc5751cdc04521d9865cf688bc54479e387a77df872f7be92696a28267`

```dockerfile
```

-	Layers:
	-	`sha256:3e8963e4d8fca9501fd57e06d4226b36e2428fc9c02e02d4fba54b74fbe28af3`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:58e0e4f9f4ddd6840bddc1aa7a4a3f88d12e2ee040216fee50fc38b09565b884
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ba6d0d08ccf4f32e24c08306b5c5945dbed755e42ccf4affefdfa254a4ebc280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229199929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efce1e3ffe173030f6b615b1d3435777d700320a579386fe5e69d889374bd3c2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:04 GMT
ARG VERSION=25.8.21.7
# Fri, 03 Apr 2026 16:46:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:30 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:30 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c405cf38316702974e718dbbd07eda14422d62e303fae7960fbaee9181a613d`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 7.6 MB (7599168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8b24ff35d307fb4bb43c39598fe990f47880d8680013e688386d04129cb4c9`  
		Last Modified: Fri, 03 Apr 2026 16:47:53 GMT  
		Size: 191.0 MB (190994325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd3f5bb4a70563fb0d4144e2c677e3ba05efdd409b5e2a2cc07133d5758fdd`  
		Last Modified: Fri, 03 Apr 2026 16:47:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051cf0dcaf87b85231342b8bee0d935d799eb6438f30b8176adaeffe9615156a`  
		Last Modified: Fri, 03 Apr 2026 16:47:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f002c854fda80c138e367007b9dc11b7b12148c5a9c7afb08315b89973924bb2`  
		Last Modified: Fri, 03 Apr 2026 16:47:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc491778644f694a3359437b40cf29c3bc1339cd37ccd68e38a2afc38ec8adb`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf1a01954f93a35a20adf2cfb7cfd424689e0fab1602577b54187eeb1a15131`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:34eec2b2db0fca0440fe5d8cc6bbf23d7a78d9e2ea75d5f14e482bcab886482c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1a98140197a194f029ee8228a60258282ade28f038370ff3e971b590ffb97`

```dockerfile
```

-	Layers:
	-	`sha256:af20e6927e3f7ac32892ef113f9ae398020be2074baffddf4f525db7a2972b65`  
		Last Modified: Fri, 03 Apr 2026 16:47:49 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e5f996c10f3c8cd53ac983c6363d16b08d9237fb1af6093a41be2c543b059875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214147489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405f4f114deb4e545b3b068d4d54516aaf725c46d5b9016583f253d7719203f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:57 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:57 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:57 GMT
ARG VERSION=25.8.21.7
# Fri, 03 Apr 2026 16:46:57 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:48:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:48:39 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:48:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:48:40 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:48:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:48:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c357252fe4ab6bd21b7ad7a9772aa8322cc2176c66f36f327bc72e995c27be74`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 7.6 MB (7578928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdad694ea1463318e46aae6bb784ac4187c33ee9d336af2b40216f9a59c859f`  
		Last Modified: Fri, 03 Apr 2026 16:49:02 GMT  
		Size: 178.1 MB (178091597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d6d6918cc917423e8958aea05ab808bb809aa75fb3b98a1703c8131b7d704a`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9abc5bcec96658f913e1eb9b0ef960f288a36cff723d1d36b8340e92faf8cd6`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253b8d977ba774cec1423754e8a8499256de1e48f0eaca9736181eccd953f14b`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95620ab76a1fe1ba4bfffb6516c3440927ccc9c6e5326ca265c7eaf75e6486ab`  
		Last Modified: Fri, 03 Apr 2026 16:48:59 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21717a7b1cd5bf759a01b74eab4368e5a519b74374e976d53aaf4facbd680fa2`  
		Last Modified: Fri, 03 Apr 2026 16:48:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b720516ad036276ef170ac1c74f82dad1d3d45f439f6b96748c1f1fca847ffda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077aaffc5751cdc04521d9865cf688bc54479e387a77df872f7be92696a28267`

```dockerfile
```

-	Layers:
	-	`sha256:3e8963e4d8fca9501fd57e06d4226b36e2428fc9c02e02d4fba54b74fbe28af3`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.21`

```console
$ docker pull clickhouse@sha256:58e0e4f9f4ddd6840bddc1aa7a4a3f88d12e2ee040216fee50fc38b09565b884
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.21` - linux; amd64

```console
$ docker pull clickhouse@sha256:ba6d0d08ccf4f32e24c08306b5c5945dbed755e42ccf4affefdfa254a4ebc280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229199929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efce1e3ffe173030f6b615b1d3435777d700320a579386fe5e69d889374bd3c2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:04 GMT
ARG VERSION=25.8.21.7
# Fri, 03 Apr 2026 16:46:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:30 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:30 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c405cf38316702974e718dbbd07eda14422d62e303fae7960fbaee9181a613d`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 7.6 MB (7599168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8b24ff35d307fb4bb43c39598fe990f47880d8680013e688386d04129cb4c9`  
		Last Modified: Fri, 03 Apr 2026 16:47:53 GMT  
		Size: 191.0 MB (190994325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd3f5bb4a70563fb0d4144e2c677e3ba05efdd409b5e2a2cc07133d5758fdd`  
		Last Modified: Fri, 03 Apr 2026 16:47:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051cf0dcaf87b85231342b8bee0d935d799eb6438f30b8176adaeffe9615156a`  
		Last Modified: Fri, 03 Apr 2026 16:47:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f002c854fda80c138e367007b9dc11b7b12148c5a9c7afb08315b89973924bb2`  
		Last Modified: Fri, 03 Apr 2026 16:47:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc491778644f694a3359437b40cf29c3bc1339cd37ccd68e38a2afc38ec8adb`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf1a01954f93a35a20adf2cfb7cfd424689e0fab1602577b54187eeb1a15131`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.21` - unknown; unknown

```console
$ docker pull clickhouse@sha256:34eec2b2db0fca0440fe5d8cc6bbf23d7a78d9e2ea75d5f14e482bcab886482c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1a98140197a194f029ee8228a60258282ade28f038370ff3e971b590ffb97`

```dockerfile
```

-	Layers:
	-	`sha256:af20e6927e3f7ac32892ef113f9ae398020be2074baffddf4f525db7a2972b65`  
		Last Modified: Fri, 03 Apr 2026 16:47:49 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.21` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e5f996c10f3c8cd53ac983c6363d16b08d9237fb1af6093a41be2c543b059875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214147489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405f4f114deb4e545b3b068d4d54516aaf725c46d5b9016583f253d7719203f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:57 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:57 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:57 GMT
ARG VERSION=25.8.21.7
# Fri, 03 Apr 2026 16:46:57 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:48:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:48:39 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:48:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:48:40 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:48:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:48:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c357252fe4ab6bd21b7ad7a9772aa8322cc2176c66f36f327bc72e995c27be74`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 7.6 MB (7578928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdad694ea1463318e46aae6bb784ac4187c33ee9d336af2b40216f9a59c859f`  
		Last Modified: Fri, 03 Apr 2026 16:49:02 GMT  
		Size: 178.1 MB (178091597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d6d6918cc917423e8958aea05ab808bb809aa75fb3b98a1703c8131b7d704a`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9abc5bcec96658f913e1eb9b0ef960f288a36cff723d1d36b8340e92faf8cd6`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253b8d977ba774cec1423754e8a8499256de1e48f0eaca9736181eccd953f14b`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95620ab76a1fe1ba4bfffb6516c3440927ccc9c6e5326ca265c7eaf75e6486ab`  
		Last Modified: Fri, 03 Apr 2026 16:48:59 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21717a7b1cd5bf759a01b74eab4368e5a519b74374e976d53aaf4facbd680fa2`  
		Last Modified: Fri, 03 Apr 2026 16:48:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.21` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b720516ad036276ef170ac1c74f82dad1d3d45f439f6b96748c1f1fca847ffda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077aaffc5751cdc04521d9865cf688bc54479e387a77df872f7be92696a28267`

```dockerfile
```

-	Layers:
	-	`sha256:3e8963e4d8fca9501fd57e06d4226b36e2428fc9c02e02d4fba54b74fbe28af3`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.21-jammy`

```console
$ docker pull clickhouse@sha256:58e0e4f9f4ddd6840bddc1aa7a4a3f88d12e2ee040216fee50fc38b09565b884
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.21-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ba6d0d08ccf4f32e24c08306b5c5945dbed755e42ccf4affefdfa254a4ebc280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229199929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efce1e3ffe173030f6b615b1d3435777d700320a579386fe5e69d889374bd3c2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:04 GMT
ARG VERSION=25.8.21.7
# Fri, 03 Apr 2026 16:46:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:30 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:30 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c405cf38316702974e718dbbd07eda14422d62e303fae7960fbaee9181a613d`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 7.6 MB (7599168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8b24ff35d307fb4bb43c39598fe990f47880d8680013e688386d04129cb4c9`  
		Last Modified: Fri, 03 Apr 2026 16:47:53 GMT  
		Size: 191.0 MB (190994325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd3f5bb4a70563fb0d4144e2c677e3ba05efdd409b5e2a2cc07133d5758fdd`  
		Last Modified: Fri, 03 Apr 2026 16:47:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051cf0dcaf87b85231342b8bee0d935d799eb6438f30b8176adaeffe9615156a`  
		Last Modified: Fri, 03 Apr 2026 16:47:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f002c854fda80c138e367007b9dc11b7b12148c5a9c7afb08315b89973924bb2`  
		Last Modified: Fri, 03 Apr 2026 16:47:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc491778644f694a3359437b40cf29c3bc1339cd37ccd68e38a2afc38ec8adb`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf1a01954f93a35a20adf2cfb7cfd424689e0fab1602577b54187eeb1a15131`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.21-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:34eec2b2db0fca0440fe5d8cc6bbf23d7a78d9e2ea75d5f14e482bcab886482c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1a98140197a194f029ee8228a60258282ade28f038370ff3e971b590ffb97`

```dockerfile
```

-	Layers:
	-	`sha256:af20e6927e3f7ac32892ef113f9ae398020be2074baffddf4f525db7a2972b65`  
		Last Modified: Fri, 03 Apr 2026 16:47:49 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.21-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e5f996c10f3c8cd53ac983c6363d16b08d9237fb1af6093a41be2c543b059875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214147489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405f4f114deb4e545b3b068d4d54516aaf725c46d5b9016583f253d7719203f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:57 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:57 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:57 GMT
ARG VERSION=25.8.21.7
# Fri, 03 Apr 2026 16:46:57 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:48:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:48:39 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:48:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:48:40 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:48:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:48:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c357252fe4ab6bd21b7ad7a9772aa8322cc2176c66f36f327bc72e995c27be74`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 7.6 MB (7578928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdad694ea1463318e46aae6bb784ac4187c33ee9d336af2b40216f9a59c859f`  
		Last Modified: Fri, 03 Apr 2026 16:49:02 GMT  
		Size: 178.1 MB (178091597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d6d6918cc917423e8958aea05ab808bb809aa75fb3b98a1703c8131b7d704a`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9abc5bcec96658f913e1eb9b0ef960f288a36cff723d1d36b8340e92faf8cd6`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253b8d977ba774cec1423754e8a8499256de1e48f0eaca9736181eccd953f14b`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95620ab76a1fe1ba4bfffb6516c3440927ccc9c6e5326ca265c7eaf75e6486ab`  
		Last Modified: Fri, 03 Apr 2026 16:48:59 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21717a7b1cd5bf759a01b74eab4368e5a519b74374e976d53aaf4facbd680fa2`  
		Last Modified: Fri, 03 Apr 2026 16:48:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.21-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b720516ad036276ef170ac1c74f82dad1d3d45f439f6b96748c1f1fca847ffda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077aaffc5751cdc04521d9865cf688bc54479e387a77df872f7be92696a28267`

```dockerfile
```

-	Layers:
	-	`sha256:3e8963e4d8fca9501fd57e06d4226b36e2428fc9c02e02d4fba54b74fbe28af3`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.21.7`

```console
$ docker pull clickhouse@sha256:58e0e4f9f4ddd6840bddc1aa7a4a3f88d12e2ee040216fee50fc38b09565b884
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.21.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:ba6d0d08ccf4f32e24c08306b5c5945dbed755e42ccf4affefdfa254a4ebc280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229199929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efce1e3ffe173030f6b615b1d3435777d700320a579386fe5e69d889374bd3c2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:04 GMT
ARG VERSION=25.8.21.7
# Fri, 03 Apr 2026 16:46:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:30 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:30 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c405cf38316702974e718dbbd07eda14422d62e303fae7960fbaee9181a613d`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 7.6 MB (7599168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8b24ff35d307fb4bb43c39598fe990f47880d8680013e688386d04129cb4c9`  
		Last Modified: Fri, 03 Apr 2026 16:47:53 GMT  
		Size: 191.0 MB (190994325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd3f5bb4a70563fb0d4144e2c677e3ba05efdd409b5e2a2cc07133d5758fdd`  
		Last Modified: Fri, 03 Apr 2026 16:47:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051cf0dcaf87b85231342b8bee0d935d799eb6438f30b8176adaeffe9615156a`  
		Last Modified: Fri, 03 Apr 2026 16:47:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f002c854fda80c138e367007b9dc11b7b12148c5a9c7afb08315b89973924bb2`  
		Last Modified: Fri, 03 Apr 2026 16:47:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc491778644f694a3359437b40cf29c3bc1339cd37ccd68e38a2afc38ec8adb`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf1a01954f93a35a20adf2cfb7cfd424689e0fab1602577b54187eeb1a15131`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.21.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:34eec2b2db0fca0440fe5d8cc6bbf23d7a78d9e2ea75d5f14e482bcab886482c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1a98140197a194f029ee8228a60258282ade28f038370ff3e971b590ffb97`

```dockerfile
```

-	Layers:
	-	`sha256:af20e6927e3f7ac32892ef113f9ae398020be2074baffddf4f525db7a2972b65`  
		Last Modified: Fri, 03 Apr 2026 16:47:49 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.21.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e5f996c10f3c8cd53ac983c6363d16b08d9237fb1af6093a41be2c543b059875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214147489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405f4f114deb4e545b3b068d4d54516aaf725c46d5b9016583f253d7719203f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:57 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:57 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:57 GMT
ARG VERSION=25.8.21.7
# Fri, 03 Apr 2026 16:46:57 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:48:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:48:39 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:48:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:48:40 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:48:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:48:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c357252fe4ab6bd21b7ad7a9772aa8322cc2176c66f36f327bc72e995c27be74`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 7.6 MB (7578928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdad694ea1463318e46aae6bb784ac4187c33ee9d336af2b40216f9a59c859f`  
		Last Modified: Fri, 03 Apr 2026 16:49:02 GMT  
		Size: 178.1 MB (178091597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d6d6918cc917423e8958aea05ab808bb809aa75fb3b98a1703c8131b7d704a`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9abc5bcec96658f913e1eb9b0ef960f288a36cff723d1d36b8340e92faf8cd6`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253b8d977ba774cec1423754e8a8499256de1e48f0eaca9736181eccd953f14b`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95620ab76a1fe1ba4bfffb6516c3440927ccc9c6e5326ca265c7eaf75e6486ab`  
		Last Modified: Fri, 03 Apr 2026 16:48:59 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21717a7b1cd5bf759a01b74eab4368e5a519b74374e976d53aaf4facbd680fa2`  
		Last Modified: Fri, 03 Apr 2026 16:48:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.21.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b720516ad036276ef170ac1c74f82dad1d3d45f439f6b96748c1f1fca847ffda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077aaffc5751cdc04521d9865cf688bc54479e387a77df872f7be92696a28267`

```dockerfile
```

-	Layers:
	-	`sha256:3e8963e4d8fca9501fd57e06d4226b36e2428fc9c02e02d4fba54b74fbe28af3`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.21.7-jammy`

```console
$ docker pull clickhouse@sha256:58e0e4f9f4ddd6840bddc1aa7a4a3f88d12e2ee040216fee50fc38b09565b884
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.21.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:ba6d0d08ccf4f32e24c08306b5c5945dbed755e42ccf4affefdfa254a4ebc280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229199929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efce1e3ffe173030f6b615b1d3435777d700320a579386fe5e69d889374bd3c2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:04 GMT
ARG VERSION=25.8.21.7
# Fri, 03 Apr 2026 16:46:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:30 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:30 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c405cf38316702974e718dbbd07eda14422d62e303fae7960fbaee9181a613d`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 7.6 MB (7599168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8b24ff35d307fb4bb43c39598fe990f47880d8680013e688386d04129cb4c9`  
		Last Modified: Fri, 03 Apr 2026 16:47:53 GMT  
		Size: 191.0 MB (190994325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cd3f5bb4a70563fb0d4144e2c677e3ba05efdd409b5e2a2cc07133d5758fdd`  
		Last Modified: Fri, 03 Apr 2026 16:47:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051cf0dcaf87b85231342b8bee0d935d799eb6438f30b8176adaeffe9615156a`  
		Last Modified: Fri, 03 Apr 2026 16:47:50 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f002c854fda80c138e367007b9dc11b7b12148c5a9c7afb08315b89973924bb2`  
		Last Modified: Fri, 03 Apr 2026 16:47:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc491778644f694a3359437b40cf29c3bc1339cd37ccd68e38a2afc38ec8adb`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf1a01954f93a35a20adf2cfb7cfd424689e0fab1602577b54187eeb1a15131`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.21.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:34eec2b2db0fca0440fe5d8cc6bbf23d7a78d9e2ea75d5f14e482bcab886482c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bd1a98140197a194f029ee8228a60258282ade28f038370ff3e971b590ffb97`

```dockerfile
```

-	Layers:
	-	`sha256:af20e6927e3f7ac32892ef113f9ae398020be2074baffddf4f525db7a2972b65`  
		Last Modified: Fri, 03 Apr 2026 16:47:49 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.21.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e5f996c10f3c8cd53ac983c6363d16b08d9237fb1af6093a41be2c543b059875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214147489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405f4f114deb4e545b3b068d4d54516aaf725c46d5b9016583f253d7719203f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:57 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:57 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:57 GMT
ARG VERSION=25.8.21.7
# Fri, 03 Apr 2026 16:46:57 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:48:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:48:39 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:48:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:48:40 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:48:40 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:48:40 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:48:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c357252fe4ab6bd21b7ad7a9772aa8322cc2176c66f36f327bc72e995c27be74`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 7.6 MB (7578928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdad694ea1463318e46aae6bb784ac4187c33ee9d336af2b40216f9a59c859f`  
		Last Modified: Fri, 03 Apr 2026 16:49:02 GMT  
		Size: 178.1 MB (178091597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d6d6918cc917423e8958aea05ab808bb809aa75fb3b98a1703c8131b7d704a`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9abc5bcec96658f913e1eb9b0ef960f288a36cff723d1d36b8340e92faf8cd6`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253b8d977ba774cec1423754e8a8499256de1e48f0eaca9736181eccd953f14b`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95620ab76a1fe1ba4bfffb6516c3440927ccc9c6e5326ca265c7eaf75e6486ab`  
		Last Modified: Fri, 03 Apr 2026 16:48:59 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21717a7b1cd5bf759a01b74eab4368e5a519b74374e976d53aaf4facbd680fa2`  
		Last Modified: Fri, 03 Apr 2026 16:48:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.21.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b720516ad036276ef170ac1c74f82dad1d3d45f439f6b96748c1f1fca847ffda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077aaffc5751cdc04521d9865cf688bc54479e387a77df872f7be92696a28267`

```dockerfile
```

-	Layers:
	-	`sha256:3e8963e4d8fca9501fd57e06d4226b36e2428fc9c02e02d4fba54b74fbe28af3`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1`

```console
$ docker pull clickhouse@sha256:a0bf2389ad67cfbb44230505eb10080e1c6effa4ff6212dc36cd0106f5134ad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:1eb5f563707a5ac5c13e2d27997ab9886d977956508988d9aed0cfd344eca2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246285489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1570bfa0a5ec5b460f7bb2f0ceeb849e0447ddd3c23c8bf7fbddd963d131211`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:00 GMT
ARG VERSION=26.1.7.13
# Fri, 03 Apr 2026 16:46:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:24 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6857345950c51ce8ef8a98559cc67a9191790eab8ca6974a456440bef7f3024`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 7.6 MB (7599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583469396bad238ef8e345b07fd359d8001f2f3c5c28124049c11738000b8ef1`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 208.1 MB (208079872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edf25ec03a605d2e3676c54522bfdb1f2da1c6d2a63e6ab5fb3a2c79490eba3`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f6273e20d1f6d163aca3d37c4fcd96e3b2ed9fda0585a68406f9b98dc5f053`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c84bcffe7f4c5eebcf59ddb2121c3127f149247881cab37ec9dae40c83207e`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42323d1b9cc4879388e1bf79708479d3872263948fc543a36c427dd7e8ed0885`  
		Last Modified: Fri, 03 Apr 2026 16:47:47 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef48ed1a7d5c1efd6a2c17f1c90430d7ba655449c5dc21e90abe621b11a668c`  
		Last Modified: Fri, 03 Apr 2026 16:47:47 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5f110508a8a0a67bfd822ebc50bf02035ffe16b0123ac23c9e3ff2a407e4691c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7735fe30792d443fde52e0aa5d74b98c9d9ffc9b52945b0dcaa6e625d953ab`

```dockerfile
```

-	Layers:
	-	`sha256:d9b9bda6fb64296b6903a2f0c7111a722b1b17d2fa962de7ce2d55df8c8125c1`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:8d13d61fb6a533192c0fba92a16ac32dbd69fd741a58bb2a8c39e8eb490ed49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228497538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128213f07180905cf5711f4cb225917177ac7392893f076886b5fc1993178e4f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:36 GMT
ARG VERSION=26.1.7.13
# Fri, 03 Apr 2026 16:46:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:48:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:48:07 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:48:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:48:07 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:48:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:48:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b17542e7b778221f66900a871553196cd81be4cf3c3d5431cb78d1300cf581`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 7.6 MB (7578950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45648534c40fc4fa9f71793e546d5125a0ccacad33389a7d88258cab2d64037`  
		Last Modified: Fri, 03 Apr 2026 16:48:31 GMT  
		Size: 192.4 MB (192441595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4767a82da151a827d754531bafd2f230880ce5d56fe55f7e78562bb3e5b19f8`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d772c1deb5fe8ad59690cc3c5d028a0389ae7e2d7c4436ac267e2e54ac7dd523`  
		Last Modified: Fri, 03 Apr 2026 16:48:27 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ee5176fe8b5f4e252bcba43e57945802cfea3204232b60fb0cfe4decc67e73`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9ce4b6d0f2385d7d4c1929d62285e90dc29555c364b5111447f842a00b6b18`  
		Last Modified: Fri, 03 Apr 2026 16:48:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086f44b973ea9585bbb02f780d93368761832af34c130d36d476587edc354797`  
		Last Modified: Fri, 03 Apr 2026 16:48:28 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:041d66fd2ee6bf9f4c41656e0cb288c31f98dd323980b45c89c62a97e64c5baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b968132551a0061b64feb4419ad62be5ffdf0f678683fab51c00b056731b438f`

```dockerfile
```

-	Layers:
	-	`sha256:e97428bfa540aa2f251aa6234fc9a31d5686910a4264ebe05bbc30003829932f`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1-jammy`

```console
$ docker pull clickhouse@sha256:a0bf2389ad67cfbb44230505eb10080e1c6effa4ff6212dc36cd0106f5134ad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1eb5f563707a5ac5c13e2d27997ab9886d977956508988d9aed0cfd344eca2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246285489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1570bfa0a5ec5b460f7bb2f0ceeb849e0447ddd3c23c8bf7fbddd963d131211`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:00 GMT
ARG VERSION=26.1.7.13
# Fri, 03 Apr 2026 16:46:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:24 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6857345950c51ce8ef8a98559cc67a9191790eab8ca6974a456440bef7f3024`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 7.6 MB (7599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583469396bad238ef8e345b07fd359d8001f2f3c5c28124049c11738000b8ef1`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 208.1 MB (208079872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edf25ec03a605d2e3676c54522bfdb1f2da1c6d2a63e6ab5fb3a2c79490eba3`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f6273e20d1f6d163aca3d37c4fcd96e3b2ed9fda0585a68406f9b98dc5f053`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c84bcffe7f4c5eebcf59ddb2121c3127f149247881cab37ec9dae40c83207e`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42323d1b9cc4879388e1bf79708479d3872263948fc543a36c427dd7e8ed0885`  
		Last Modified: Fri, 03 Apr 2026 16:47:47 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef48ed1a7d5c1efd6a2c17f1c90430d7ba655449c5dc21e90abe621b11a668c`  
		Last Modified: Fri, 03 Apr 2026 16:47:47 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5f110508a8a0a67bfd822ebc50bf02035ffe16b0123ac23c9e3ff2a407e4691c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7735fe30792d443fde52e0aa5d74b98c9d9ffc9b52945b0dcaa6e625d953ab`

```dockerfile
```

-	Layers:
	-	`sha256:d9b9bda6fb64296b6903a2f0c7111a722b1b17d2fa962de7ce2d55df8c8125c1`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:8d13d61fb6a533192c0fba92a16ac32dbd69fd741a58bb2a8c39e8eb490ed49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228497538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128213f07180905cf5711f4cb225917177ac7392893f076886b5fc1993178e4f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:36 GMT
ARG VERSION=26.1.7.13
# Fri, 03 Apr 2026 16:46:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:48:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:48:07 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:48:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:48:07 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:48:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:48:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b17542e7b778221f66900a871553196cd81be4cf3c3d5431cb78d1300cf581`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 7.6 MB (7578950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45648534c40fc4fa9f71793e546d5125a0ccacad33389a7d88258cab2d64037`  
		Last Modified: Fri, 03 Apr 2026 16:48:31 GMT  
		Size: 192.4 MB (192441595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4767a82da151a827d754531bafd2f230880ce5d56fe55f7e78562bb3e5b19f8`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d772c1deb5fe8ad59690cc3c5d028a0389ae7e2d7c4436ac267e2e54ac7dd523`  
		Last Modified: Fri, 03 Apr 2026 16:48:27 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ee5176fe8b5f4e252bcba43e57945802cfea3204232b60fb0cfe4decc67e73`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9ce4b6d0f2385d7d4c1929d62285e90dc29555c364b5111447f842a00b6b18`  
		Last Modified: Fri, 03 Apr 2026 16:48:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086f44b973ea9585bbb02f780d93368761832af34c130d36d476587edc354797`  
		Last Modified: Fri, 03 Apr 2026 16:48:28 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:041d66fd2ee6bf9f4c41656e0cb288c31f98dd323980b45c89c62a97e64c5baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b968132551a0061b64feb4419ad62be5ffdf0f678683fab51c00b056731b438f`

```dockerfile
```

-	Layers:
	-	`sha256:e97428bfa540aa2f251aa6234fc9a31d5686910a4264ebe05bbc30003829932f`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.7`

```console
$ docker pull clickhouse@sha256:a0bf2389ad67cfbb44230505eb10080e1c6effa4ff6212dc36cd0106f5134ad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:1eb5f563707a5ac5c13e2d27997ab9886d977956508988d9aed0cfd344eca2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246285489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1570bfa0a5ec5b460f7bb2f0ceeb849e0447ddd3c23c8bf7fbddd963d131211`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:00 GMT
ARG VERSION=26.1.7.13
# Fri, 03 Apr 2026 16:46:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:24 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6857345950c51ce8ef8a98559cc67a9191790eab8ca6974a456440bef7f3024`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 7.6 MB (7599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583469396bad238ef8e345b07fd359d8001f2f3c5c28124049c11738000b8ef1`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 208.1 MB (208079872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edf25ec03a605d2e3676c54522bfdb1f2da1c6d2a63e6ab5fb3a2c79490eba3`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f6273e20d1f6d163aca3d37c4fcd96e3b2ed9fda0585a68406f9b98dc5f053`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c84bcffe7f4c5eebcf59ddb2121c3127f149247881cab37ec9dae40c83207e`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42323d1b9cc4879388e1bf79708479d3872263948fc543a36c427dd7e8ed0885`  
		Last Modified: Fri, 03 Apr 2026 16:47:47 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef48ed1a7d5c1efd6a2c17f1c90430d7ba655449c5dc21e90abe621b11a668c`  
		Last Modified: Fri, 03 Apr 2026 16:47:47 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5f110508a8a0a67bfd822ebc50bf02035ffe16b0123ac23c9e3ff2a407e4691c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7735fe30792d443fde52e0aa5d74b98c9d9ffc9b52945b0dcaa6e625d953ab`

```dockerfile
```

-	Layers:
	-	`sha256:d9b9bda6fb64296b6903a2f0c7111a722b1b17d2fa962de7ce2d55df8c8125c1`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:8d13d61fb6a533192c0fba92a16ac32dbd69fd741a58bb2a8c39e8eb490ed49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228497538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128213f07180905cf5711f4cb225917177ac7392893f076886b5fc1993178e4f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:36 GMT
ARG VERSION=26.1.7.13
# Fri, 03 Apr 2026 16:46:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:48:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:48:07 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:48:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:48:07 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:48:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:48:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b17542e7b778221f66900a871553196cd81be4cf3c3d5431cb78d1300cf581`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 7.6 MB (7578950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45648534c40fc4fa9f71793e546d5125a0ccacad33389a7d88258cab2d64037`  
		Last Modified: Fri, 03 Apr 2026 16:48:31 GMT  
		Size: 192.4 MB (192441595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4767a82da151a827d754531bafd2f230880ce5d56fe55f7e78562bb3e5b19f8`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d772c1deb5fe8ad59690cc3c5d028a0389ae7e2d7c4436ac267e2e54ac7dd523`  
		Last Modified: Fri, 03 Apr 2026 16:48:27 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ee5176fe8b5f4e252bcba43e57945802cfea3204232b60fb0cfe4decc67e73`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9ce4b6d0f2385d7d4c1929d62285e90dc29555c364b5111447f842a00b6b18`  
		Last Modified: Fri, 03 Apr 2026 16:48:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086f44b973ea9585bbb02f780d93368761832af34c130d36d476587edc354797`  
		Last Modified: Fri, 03 Apr 2026 16:48:28 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:041d66fd2ee6bf9f4c41656e0cb288c31f98dd323980b45c89c62a97e64c5baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b968132551a0061b64feb4419ad62be5ffdf0f678683fab51c00b056731b438f`

```dockerfile
```

-	Layers:
	-	`sha256:e97428bfa540aa2f251aa6234fc9a31d5686910a4264ebe05bbc30003829932f`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.7-jammy`

```console
$ docker pull clickhouse@sha256:a0bf2389ad67cfbb44230505eb10080e1c6effa4ff6212dc36cd0106f5134ad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1eb5f563707a5ac5c13e2d27997ab9886d977956508988d9aed0cfd344eca2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246285489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1570bfa0a5ec5b460f7bb2f0ceeb849e0447ddd3c23c8bf7fbddd963d131211`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:00 GMT
ARG VERSION=26.1.7.13
# Fri, 03 Apr 2026 16:46:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:24 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6857345950c51ce8ef8a98559cc67a9191790eab8ca6974a456440bef7f3024`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 7.6 MB (7599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583469396bad238ef8e345b07fd359d8001f2f3c5c28124049c11738000b8ef1`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 208.1 MB (208079872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edf25ec03a605d2e3676c54522bfdb1f2da1c6d2a63e6ab5fb3a2c79490eba3`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f6273e20d1f6d163aca3d37c4fcd96e3b2ed9fda0585a68406f9b98dc5f053`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c84bcffe7f4c5eebcf59ddb2121c3127f149247881cab37ec9dae40c83207e`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42323d1b9cc4879388e1bf79708479d3872263948fc543a36c427dd7e8ed0885`  
		Last Modified: Fri, 03 Apr 2026 16:47:47 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef48ed1a7d5c1efd6a2c17f1c90430d7ba655449c5dc21e90abe621b11a668c`  
		Last Modified: Fri, 03 Apr 2026 16:47:47 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5f110508a8a0a67bfd822ebc50bf02035ffe16b0123ac23c9e3ff2a407e4691c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7735fe30792d443fde52e0aa5d74b98c9d9ffc9b52945b0dcaa6e625d953ab`

```dockerfile
```

-	Layers:
	-	`sha256:d9b9bda6fb64296b6903a2f0c7111a722b1b17d2fa962de7ce2d55df8c8125c1`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:8d13d61fb6a533192c0fba92a16ac32dbd69fd741a58bb2a8c39e8eb490ed49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228497538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128213f07180905cf5711f4cb225917177ac7392893f076886b5fc1993178e4f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:36 GMT
ARG VERSION=26.1.7.13
# Fri, 03 Apr 2026 16:46:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:48:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:48:07 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:48:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:48:07 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:48:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:48:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b17542e7b778221f66900a871553196cd81be4cf3c3d5431cb78d1300cf581`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 7.6 MB (7578950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45648534c40fc4fa9f71793e546d5125a0ccacad33389a7d88258cab2d64037`  
		Last Modified: Fri, 03 Apr 2026 16:48:31 GMT  
		Size: 192.4 MB (192441595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4767a82da151a827d754531bafd2f230880ce5d56fe55f7e78562bb3e5b19f8`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d772c1deb5fe8ad59690cc3c5d028a0389ae7e2d7c4436ac267e2e54ac7dd523`  
		Last Modified: Fri, 03 Apr 2026 16:48:27 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ee5176fe8b5f4e252bcba43e57945802cfea3204232b60fb0cfe4decc67e73`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9ce4b6d0f2385d7d4c1929d62285e90dc29555c364b5111447f842a00b6b18`  
		Last Modified: Fri, 03 Apr 2026 16:48:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086f44b973ea9585bbb02f780d93368761832af34c130d36d476587edc354797`  
		Last Modified: Fri, 03 Apr 2026 16:48:28 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:041d66fd2ee6bf9f4c41656e0cb288c31f98dd323980b45c89c62a97e64c5baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b968132551a0061b64feb4419ad62be5ffdf0f678683fab51c00b056731b438f`

```dockerfile
```

-	Layers:
	-	`sha256:e97428bfa540aa2f251aa6234fc9a31d5686910a4264ebe05bbc30003829932f`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.7.13`

```console
$ docker pull clickhouse@sha256:a0bf2389ad67cfbb44230505eb10080e1c6effa4ff6212dc36cd0106f5134ad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.7.13` - linux; amd64

```console
$ docker pull clickhouse@sha256:1eb5f563707a5ac5c13e2d27997ab9886d977956508988d9aed0cfd344eca2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246285489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1570bfa0a5ec5b460f7bb2f0ceeb849e0447ddd3c23c8bf7fbddd963d131211`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:00 GMT
ARG VERSION=26.1.7.13
# Fri, 03 Apr 2026 16:46:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:24 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6857345950c51ce8ef8a98559cc67a9191790eab8ca6974a456440bef7f3024`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 7.6 MB (7599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583469396bad238ef8e345b07fd359d8001f2f3c5c28124049c11738000b8ef1`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 208.1 MB (208079872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edf25ec03a605d2e3676c54522bfdb1f2da1c6d2a63e6ab5fb3a2c79490eba3`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f6273e20d1f6d163aca3d37c4fcd96e3b2ed9fda0585a68406f9b98dc5f053`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c84bcffe7f4c5eebcf59ddb2121c3127f149247881cab37ec9dae40c83207e`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42323d1b9cc4879388e1bf79708479d3872263948fc543a36c427dd7e8ed0885`  
		Last Modified: Fri, 03 Apr 2026 16:47:47 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef48ed1a7d5c1efd6a2c17f1c90430d7ba655449c5dc21e90abe621b11a668c`  
		Last Modified: Fri, 03 Apr 2026 16:47:47 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.7.13` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5f110508a8a0a67bfd822ebc50bf02035ffe16b0123ac23c9e3ff2a407e4691c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7735fe30792d443fde52e0aa5d74b98c9d9ffc9b52945b0dcaa6e625d953ab`

```dockerfile
```

-	Layers:
	-	`sha256:d9b9bda6fb64296b6903a2f0c7111a722b1b17d2fa962de7ce2d55df8c8125c1`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.7.13` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:8d13d61fb6a533192c0fba92a16ac32dbd69fd741a58bb2a8c39e8eb490ed49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228497538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128213f07180905cf5711f4cb225917177ac7392893f076886b5fc1993178e4f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:36 GMT
ARG VERSION=26.1.7.13
# Fri, 03 Apr 2026 16:46:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:48:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:48:07 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:48:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:48:07 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:48:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:48:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b17542e7b778221f66900a871553196cd81be4cf3c3d5431cb78d1300cf581`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 7.6 MB (7578950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45648534c40fc4fa9f71793e546d5125a0ccacad33389a7d88258cab2d64037`  
		Last Modified: Fri, 03 Apr 2026 16:48:31 GMT  
		Size: 192.4 MB (192441595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4767a82da151a827d754531bafd2f230880ce5d56fe55f7e78562bb3e5b19f8`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d772c1deb5fe8ad59690cc3c5d028a0389ae7e2d7c4436ac267e2e54ac7dd523`  
		Last Modified: Fri, 03 Apr 2026 16:48:27 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ee5176fe8b5f4e252bcba43e57945802cfea3204232b60fb0cfe4decc67e73`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9ce4b6d0f2385d7d4c1929d62285e90dc29555c364b5111447f842a00b6b18`  
		Last Modified: Fri, 03 Apr 2026 16:48:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086f44b973ea9585bbb02f780d93368761832af34c130d36d476587edc354797`  
		Last Modified: Fri, 03 Apr 2026 16:48:28 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.7.13` - unknown; unknown

```console
$ docker pull clickhouse@sha256:041d66fd2ee6bf9f4c41656e0cb288c31f98dd323980b45c89c62a97e64c5baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b968132551a0061b64feb4419ad62be5ffdf0f678683fab51c00b056731b438f`

```dockerfile
```

-	Layers:
	-	`sha256:e97428bfa540aa2f251aa6234fc9a31d5686910a4264ebe05bbc30003829932f`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.7.13-jammy`

```console
$ docker pull clickhouse@sha256:a0bf2389ad67cfbb44230505eb10080e1c6effa4ff6212dc36cd0106f5134ad3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.7.13-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1eb5f563707a5ac5c13e2d27997ab9886d977956508988d9aed0cfd344eca2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246285489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1570bfa0a5ec5b460f7bb2f0ceeb849e0447ddd3c23c8bf7fbddd963d131211`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:00 GMT
ARG VERSION=26.1.7.13
# Fri, 03 Apr 2026 16:46:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:24 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6857345950c51ce8ef8a98559cc67a9191790eab8ca6974a456440bef7f3024`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 7.6 MB (7599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583469396bad238ef8e345b07fd359d8001f2f3c5c28124049c11738000b8ef1`  
		Last Modified: Fri, 03 Apr 2026 16:47:51 GMT  
		Size: 208.1 MB (208079872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edf25ec03a605d2e3676c54522bfdb1f2da1c6d2a63e6ab5fb3a2c79490eba3`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f6273e20d1f6d163aca3d37c4fcd96e3b2ed9fda0585a68406f9b98dc5f053`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c84bcffe7f4c5eebcf59ddb2121c3127f149247881cab37ec9dae40c83207e`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42323d1b9cc4879388e1bf79708479d3872263948fc543a36c427dd7e8ed0885`  
		Last Modified: Fri, 03 Apr 2026 16:47:47 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef48ed1a7d5c1efd6a2c17f1c90430d7ba655449c5dc21e90abe621b11a668c`  
		Last Modified: Fri, 03 Apr 2026 16:47:47 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.7.13-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5f110508a8a0a67bfd822ebc50bf02035ffe16b0123ac23c9e3ff2a407e4691c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7735fe30792d443fde52e0aa5d74b98c9d9ffc9b52945b0dcaa6e625d953ab`

```dockerfile
```

-	Layers:
	-	`sha256:d9b9bda6fb64296b6903a2f0c7111a722b1b17d2fa962de7ce2d55df8c8125c1`  
		Last Modified: Fri, 03 Apr 2026 16:47:46 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.7.13-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:8d13d61fb6a533192c0fba92a16ac32dbd69fd741a58bb2a8c39e8eb490ed49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228497538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128213f07180905cf5711f4cb225917177ac7392893f076886b5fc1993178e4f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:36 GMT
ARG VERSION=26.1.7.13
# Fri, 03 Apr 2026 16:46:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:48:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:48:07 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:48:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:48:07 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:48:07 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:48:07 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:48:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b17542e7b778221f66900a871553196cd81be4cf3c3d5431cb78d1300cf581`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 7.6 MB (7578950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45648534c40fc4fa9f71793e546d5125a0ccacad33389a7d88258cab2d64037`  
		Last Modified: Fri, 03 Apr 2026 16:48:31 GMT  
		Size: 192.4 MB (192441595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4767a82da151a827d754531bafd2f230880ce5d56fe55f7e78562bb3e5b19f8`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d772c1deb5fe8ad59690cc3c5d028a0389ae7e2d7c4436ac267e2e54ac7dd523`  
		Last Modified: Fri, 03 Apr 2026 16:48:27 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ee5176fe8b5f4e252bcba43e57945802cfea3204232b60fb0cfe4decc67e73`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9ce4b6d0f2385d7d4c1929d62285e90dc29555c364b5111447f842a00b6b18`  
		Last Modified: Fri, 03 Apr 2026 16:48:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086f44b973ea9585bbb02f780d93368761832af34c130d36d476587edc354797`  
		Last Modified: Fri, 03 Apr 2026 16:48:28 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.7.13-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:041d66fd2ee6bf9f4c41656e0cb288c31f98dd323980b45c89c62a97e64c5baf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b968132551a0061b64feb4419ad62be5ffdf0f678683fab51c00b056731b438f`

```dockerfile
```

-	Layers:
	-	`sha256:e97428bfa540aa2f251aa6234fc9a31d5686910a4264ebe05bbc30003829932f`  
		Last Modified: Fri, 03 Apr 2026 16:48:26 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2`

```console
$ docker pull clickhouse@sha256:86d4c94371cb07e8a0909e7b785eeab31aeaa692b626fccb4a7f6f63d3d985d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:45b683da243928563c703f4bd267364ba16b8f6294b0ad18600e91129de00074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253861864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea66770d70ad540dbe23297f4761a36643bcd107fb66dfbe1932e45610fdbb7b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:04 GMT
ARG VERSION=26.2.7.17
# Fri, 03 Apr 2026 16:46:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:46:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:46:30 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:46:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:46:30 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:46:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:46:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c405cf38316702974e718dbbd07eda14422d62e303fae7960fbaee9181a613d`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 7.6 MB (7599168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5a99d405a6bbc30d16b316996499a69fd88a9138be6bf25412d3457ddd8273`  
		Last Modified: Fri, 03 Apr 2026 16:46:57 GMT  
		Size: 215.7 MB (215656233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95c0d71132c157fc3ef54f2139d0405dbe35d4167955660808e1994aa4c3bb`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c832c8aa0f75d42a0b5184d0da86ae352af4d2af428baf3ea8427549246ec6`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4f6001c72610967203addf8b926876430b9c52781bc7c439cdf4b1a76c53b9`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e81457c0d32514fdbd102216b8ac825e76f3eea16f82416bfa0b0ca81d4002f`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d994f7c5a9a4b867ee40e071f6beba8dfad23380b03befd4a7ec54ad23e51e`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9674c041d0669f0b8dc6b3faf7d36d006e57e2dbd34b700064dbb68dcec396b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75eed0b2594aa3af22337c26b3dd587253defaa38b3f92557c27aca18645ab1b`

```dockerfile
```

-	Layers:
	-	`sha256:d86b7c7f5fa218dc9501690ff98c77d1b3db572916d08a609164cc903984a512`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cd900b6fa82dce48c2db0c8da93c925816bc6e610df8d8d13361df0e82a90719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237425482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd089181102c02a75365eb3c0569b41d188c47f16476b258284dd3ec58288ea2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:57 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:57 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:57 GMT
ARG VERSION=26.2.7.17
# Fri, 03 Apr 2026 16:46:57 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:33 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c357252fe4ab6bd21b7ad7a9772aa8322cc2176c66f36f327bc72e995c27be74`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 7.6 MB (7578928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db46e48e668203be36b20c5cefb526116de1c5b734a5973e7b94cffb01b2a1bc`  
		Last Modified: Fri, 03 Apr 2026 16:48:00 GMT  
		Size: 201.4 MB (201369559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b011289759fccdb26582c7e66d61249c3096e4d15ffa3c805d23f71cf53ea7b`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3459363f19c5ca4ea5786a8e405596e71fb92e1f60b5ff465abb29fcd871bd9f`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad35652b512969d67de755cf23eb2ab52e472dea6f9e87589970a7e989ef08f`  
		Last Modified: Fri, 03 Apr 2026 16:47:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adcc01615593db75c5307ac789e71d234b3e1eb4cb4fd8295f0ca0a567eaea6`  
		Last Modified: Fri, 03 Apr 2026 16:47:56 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad850f833213305621e9d0cfd7bb1dc646ba2ef5a0b2d0d81a8774ebcdd606c`  
		Last Modified: Fri, 03 Apr 2026 16:47:57 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:35ee6f3d9f0c59e4782159aea514954313fa956e56fad02518ac3430da8a0008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1418bb3e74ac61cd695877ecc9fb343cfcd19ebed9374953b891fb6b1302691f`

```dockerfile
```

-	Layers:
	-	`sha256:e1739c7d43e7fd74a2a84dd579ecfc40ca5608357d9325b6d8375fc49c763377`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2-jammy`

```console
$ docker pull clickhouse@sha256:86d4c94371cb07e8a0909e7b785eeab31aeaa692b626fccb4a7f6f63d3d985d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:45b683da243928563c703f4bd267364ba16b8f6294b0ad18600e91129de00074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253861864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea66770d70ad540dbe23297f4761a36643bcd107fb66dfbe1932e45610fdbb7b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:04 GMT
ARG VERSION=26.2.7.17
# Fri, 03 Apr 2026 16:46:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:46:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:46:30 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:46:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:46:30 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:46:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:46:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c405cf38316702974e718dbbd07eda14422d62e303fae7960fbaee9181a613d`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 7.6 MB (7599168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5a99d405a6bbc30d16b316996499a69fd88a9138be6bf25412d3457ddd8273`  
		Last Modified: Fri, 03 Apr 2026 16:46:57 GMT  
		Size: 215.7 MB (215656233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95c0d71132c157fc3ef54f2139d0405dbe35d4167955660808e1994aa4c3bb`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c832c8aa0f75d42a0b5184d0da86ae352af4d2af428baf3ea8427549246ec6`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4f6001c72610967203addf8b926876430b9c52781bc7c439cdf4b1a76c53b9`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e81457c0d32514fdbd102216b8ac825e76f3eea16f82416bfa0b0ca81d4002f`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d994f7c5a9a4b867ee40e071f6beba8dfad23380b03befd4a7ec54ad23e51e`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9674c041d0669f0b8dc6b3faf7d36d006e57e2dbd34b700064dbb68dcec396b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75eed0b2594aa3af22337c26b3dd587253defaa38b3f92557c27aca18645ab1b`

```dockerfile
```

-	Layers:
	-	`sha256:d86b7c7f5fa218dc9501690ff98c77d1b3db572916d08a609164cc903984a512`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cd900b6fa82dce48c2db0c8da93c925816bc6e610df8d8d13361df0e82a90719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237425482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd089181102c02a75365eb3c0569b41d188c47f16476b258284dd3ec58288ea2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:57 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:57 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:57 GMT
ARG VERSION=26.2.7.17
# Fri, 03 Apr 2026 16:46:57 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:33 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c357252fe4ab6bd21b7ad7a9772aa8322cc2176c66f36f327bc72e995c27be74`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 7.6 MB (7578928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db46e48e668203be36b20c5cefb526116de1c5b734a5973e7b94cffb01b2a1bc`  
		Last Modified: Fri, 03 Apr 2026 16:48:00 GMT  
		Size: 201.4 MB (201369559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b011289759fccdb26582c7e66d61249c3096e4d15ffa3c805d23f71cf53ea7b`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3459363f19c5ca4ea5786a8e405596e71fb92e1f60b5ff465abb29fcd871bd9f`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad35652b512969d67de755cf23eb2ab52e472dea6f9e87589970a7e989ef08f`  
		Last Modified: Fri, 03 Apr 2026 16:47:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adcc01615593db75c5307ac789e71d234b3e1eb4cb4fd8295f0ca0a567eaea6`  
		Last Modified: Fri, 03 Apr 2026 16:47:56 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad850f833213305621e9d0cfd7bb1dc646ba2ef5a0b2d0d81a8774ebcdd606c`  
		Last Modified: Fri, 03 Apr 2026 16:47:57 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:35ee6f3d9f0c59e4782159aea514954313fa956e56fad02518ac3430da8a0008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1418bb3e74ac61cd695877ecc9fb343cfcd19ebed9374953b891fb6b1302691f`

```dockerfile
```

-	Layers:
	-	`sha256:e1739c7d43e7fd74a2a84dd579ecfc40ca5608357d9325b6d8375fc49c763377`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.7`

```console
$ docker pull clickhouse@sha256:86d4c94371cb07e8a0909e7b785eeab31aeaa692b626fccb4a7f6f63d3d985d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:45b683da243928563c703f4bd267364ba16b8f6294b0ad18600e91129de00074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253861864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea66770d70ad540dbe23297f4761a36643bcd107fb66dfbe1932e45610fdbb7b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:04 GMT
ARG VERSION=26.2.7.17
# Fri, 03 Apr 2026 16:46:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:46:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:46:30 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:46:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:46:30 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:46:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:46:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c405cf38316702974e718dbbd07eda14422d62e303fae7960fbaee9181a613d`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 7.6 MB (7599168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5a99d405a6bbc30d16b316996499a69fd88a9138be6bf25412d3457ddd8273`  
		Last Modified: Fri, 03 Apr 2026 16:46:57 GMT  
		Size: 215.7 MB (215656233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95c0d71132c157fc3ef54f2139d0405dbe35d4167955660808e1994aa4c3bb`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c832c8aa0f75d42a0b5184d0da86ae352af4d2af428baf3ea8427549246ec6`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4f6001c72610967203addf8b926876430b9c52781bc7c439cdf4b1a76c53b9`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e81457c0d32514fdbd102216b8ac825e76f3eea16f82416bfa0b0ca81d4002f`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d994f7c5a9a4b867ee40e071f6beba8dfad23380b03befd4a7ec54ad23e51e`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9674c041d0669f0b8dc6b3faf7d36d006e57e2dbd34b700064dbb68dcec396b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75eed0b2594aa3af22337c26b3dd587253defaa38b3f92557c27aca18645ab1b`

```dockerfile
```

-	Layers:
	-	`sha256:d86b7c7f5fa218dc9501690ff98c77d1b3db572916d08a609164cc903984a512`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cd900b6fa82dce48c2db0c8da93c925816bc6e610df8d8d13361df0e82a90719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237425482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd089181102c02a75365eb3c0569b41d188c47f16476b258284dd3ec58288ea2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:57 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:57 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:57 GMT
ARG VERSION=26.2.7.17
# Fri, 03 Apr 2026 16:46:57 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:33 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c357252fe4ab6bd21b7ad7a9772aa8322cc2176c66f36f327bc72e995c27be74`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 7.6 MB (7578928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db46e48e668203be36b20c5cefb526116de1c5b734a5973e7b94cffb01b2a1bc`  
		Last Modified: Fri, 03 Apr 2026 16:48:00 GMT  
		Size: 201.4 MB (201369559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b011289759fccdb26582c7e66d61249c3096e4d15ffa3c805d23f71cf53ea7b`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3459363f19c5ca4ea5786a8e405596e71fb92e1f60b5ff465abb29fcd871bd9f`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad35652b512969d67de755cf23eb2ab52e472dea6f9e87589970a7e989ef08f`  
		Last Modified: Fri, 03 Apr 2026 16:47:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adcc01615593db75c5307ac789e71d234b3e1eb4cb4fd8295f0ca0a567eaea6`  
		Last Modified: Fri, 03 Apr 2026 16:47:56 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad850f833213305621e9d0cfd7bb1dc646ba2ef5a0b2d0d81a8774ebcdd606c`  
		Last Modified: Fri, 03 Apr 2026 16:47:57 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:35ee6f3d9f0c59e4782159aea514954313fa956e56fad02518ac3430da8a0008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1418bb3e74ac61cd695877ecc9fb343cfcd19ebed9374953b891fb6b1302691f`

```dockerfile
```

-	Layers:
	-	`sha256:e1739c7d43e7fd74a2a84dd579ecfc40ca5608357d9325b6d8375fc49c763377`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.7-jammy`

```console
$ docker pull clickhouse@sha256:86d4c94371cb07e8a0909e7b785eeab31aeaa692b626fccb4a7f6f63d3d985d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:45b683da243928563c703f4bd267364ba16b8f6294b0ad18600e91129de00074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253861864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea66770d70ad540dbe23297f4761a36643bcd107fb66dfbe1932e45610fdbb7b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:04 GMT
ARG VERSION=26.2.7.17
# Fri, 03 Apr 2026 16:46:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:46:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:46:30 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:46:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:46:30 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:46:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:46:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c405cf38316702974e718dbbd07eda14422d62e303fae7960fbaee9181a613d`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 7.6 MB (7599168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5a99d405a6bbc30d16b316996499a69fd88a9138be6bf25412d3457ddd8273`  
		Last Modified: Fri, 03 Apr 2026 16:46:57 GMT  
		Size: 215.7 MB (215656233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95c0d71132c157fc3ef54f2139d0405dbe35d4167955660808e1994aa4c3bb`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c832c8aa0f75d42a0b5184d0da86ae352af4d2af428baf3ea8427549246ec6`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4f6001c72610967203addf8b926876430b9c52781bc7c439cdf4b1a76c53b9`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e81457c0d32514fdbd102216b8ac825e76f3eea16f82416bfa0b0ca81d4002f`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d994f7c5a9a4b867ee40e071f6beba8dfad23380b03befd4a7ec54ad23e51e`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9674c041d0669f0b8dc6b3faf7d36d006e57e2dbd34b700064dbb68dcec396b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75eed0b2594aa3af22337c26b3dd587253defaa38b3f92557c27aca18645ab1b`

```dockerfile
```

-	Layers:
	-	`sha256:d86b7c7f5fa218dc9501690ff98c77d1b3db572916d08a609164cc903984a512`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cd900b6fa82dce48c2db0c8da93c925816bc6e610df8d8d13361df0e82a90719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237425482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd089181102c02a75365eb3c0569b41d188c47f16476b258284dd3ec58288ea2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:57 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:57 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:57 GMT
ARG VERSION=26.2.7.17
# Fri, 03 Apr 2026 16:46:57 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:33 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c357252fe4ab6bd21b7ad7a9772aa8322cc2176c66f36f327bc72e995c27be74`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 7.6 MB (7578928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db46e48e668203be36b20c5cefb526116de1c5b734a5973e7b94cffb01b2a1bc`  
		Last Modified: Fri, 03 Apr 2026 16:48:00 GMT  
		Size: 201.4 MB (201369559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b011289759fccdb26582c7e66d61249c3096e4d15ffa3c805d23f71cf53ea7b`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3459363f19c5ca4ea5786a8e405596e71fb92e1f60b5ff465abb29fcd871bd9f`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad35652b512969d67de755cf23eb2ab52e472dea6f9e87589970a7e989ef08f`  
		Last Modified: Fri, 03 Apr 2026 16:47:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adcc01615593db75c5307ac789e71d234b3e1eb4cb4fd8295f0ca0a567eaea6`  
		Last Modified: Fri, 03 Apr 2026 16:47:56 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad850f833213305621e9d0cfd7bb1dc646ba2ef5a0b2d0d81a8774ebcdd606c`  
		Last Modified: Fri, 03 Apr 2026 16:47:57 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:35ee6f3d9f0c59e4782159aea514954313fa956e56fad02518ac3430da8a0008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1418bb3e74ac61cd695877ecc9fb343cfcd19ebed9374953b891fb6b1302691f`

```dockerfile
```

-	Layers:
	-	`sha256:e1739c7d43e7fd74a2a84dd579ecfc40ca5608357d9325b6d8375fc49c763377`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.7.17`

```console
$ docker pull clickhouse@sha256:86d4c94371cb07e8a0909e7b785eeab31aeaa692b626fccb4a7f6f63d3d985d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.7.17` - linux; amd64

```console
$ docker pull clickhouse@sha256:45b683da243928563c703f4bd267364ba16b8f6294b0ad18600e91129de00074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253861864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea66770d70ad540dbe23297f4761a36643bcd107fb66dfbe1932e45610fdbb7b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:04 GMT
ARG VERSION=26.2.7.17
# Fri, 03 Apr 2026 16:46:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:46:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:46:30 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:46:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:46:30 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:46:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:46:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c405cf38316702974e718dbbd07eda14422d62e303fae7960fbaee9181a613d`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 7.6 MB (7599168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5a99d405a6bbc30d16b316996499a69fd88a9138be6bf25412d3457ddd8273`  
		Last Modified: Fri, 03 Apr 2026 16:46:57 GMT  
		Size: 215.7 MB (215656233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95c0d71132c157fc3ef54f2139d0405dbe35d4167955660808e1994aa4c3bb`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c832c8aa0f75d42a0b5184d0da86ae352af4d2af428baf3ea8427549246ec6`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4f6001c72610967203addf8b926876430b9c52781bc7c439cdf4b1a76c53b9`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e81457c0d32514fdbd102216b8ac825e76f3eea16f82416bfa0b0ca81d4002f`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d994f7c5a9a4b867ee40e071f6beba8dfad23380b03befd4a7ec54ad23e51e`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.7.17` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9674c041d0669f0b8dc6b3faf7d36d006e57e2dbd34b700064dbb68dcec396b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75eed0b2594aa3af22337c26b3dd587253defaa38b3f92557c27aca18645ab1b`

```dockerfile
```

-	Layers:
	-	`sha256:d86b7c7f5fa218dc9501690ff98c77d1b3db572916d08a609164cc903984a512`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.7.17` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cd900b6fa82dce48c2db0c8da93c925816bc6e610df8d8d13361df0e82a90719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237425482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd089181102c02a75365eb3c0569b41d188c47f16476b258284dd3ec58288ea2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:57 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:57 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:57 GMT
ARG VERSION=26.2.7.17
# Fri, 03 Apr 2026 16:46:57 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:33 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c357252fe4ab6bd21b7ad7a9772aa8322cc2176c66f36f327bc72e995c27be74`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 7.6 MB (7578928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db46e48e668203be36b20c5cefb526116de1c5b734a5973e7b94cffb01b2a1bc`  
		Last Modified: Fri, 03 Apr 2026 16:48:00 GMT  
		Size: 201.4 MB (201369559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b011289759fccdb26582c7e66d61249c3096e4d15ffa3c805d23f71cf53ea7b`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3459363f19c5ca4ea5786a8e405596e71fb92e1f60b5ff465abb29fcd871bd9f`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad35652b512969d67de755cf23eb2ab52e472dea6f9e87589970a7e989ef08f`  
		Last Modified: Fri, 03 Apr 2026 16:47:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adcc01615593db75c5307ac789e71d234b3e1eb4cb4fd8295f0ca0a567eaea6`  
		Last Modified: Fri, 03 Apr 2026 16:47:56 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad850f833213305621e9d0cfd7bb1dc646ba2ef5a0b2d0d81a8774ebcdd606c`  
		Last Modified: Fri, 03 Apr 2026 16:47:57 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.7.17` - unknown; unknown

```console
$ docker pull clickhouse@sha256:35ee6f3d9f0c59e4782159aea514954313fa956e56fad02518ac3430da8a0008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1418bb3e74ac61cd695877ecc9fb343cfcd19ebed9374953b891fb6b1302691f`

```dockerfile
```

-	Layers:
	-	`sha256:e1739c7d43e7fd74a2a84dd579ecfc40ca5608357d9325b6d8375fc49c763377`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.7.17-jammy`

```console
$ docker pull clickhouse@sha256:86d4c94371cb07e8a0909e7b785eeab31aeaa692b626fccb4a7f6f63d3d985d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.7.17-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:45b683da243928563c703f4bd267364ba16b8f6294b0ad18600e91129de00074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253861864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea66770d70ad540dbe23297f4761a36643bcd107fb66dfbe1932e45610fdbb7b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:04 GMT
ARG VERSION=26.2.7.17
# Fri, 03 Apr 2026 16:46:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:46:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:46:30 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:46:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:46:30 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:46:30 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:46:30 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:46:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c405cf38316702974e718dbbd07eda14422d62e303fae7960fbaee9181a613d`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 7.6 MB (7599168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5a99d405a6bbc30d16b316996499a69fd88a9138be6bf25412d3457ddd8273`  
		Last Modified: Fri, 03 Apr 2026 16:46:57 GMT  
		Size: 215.7 MB (215656233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af95c0d71132c157fc3ef54f2139d0405dbe35d4167955660808e1994aa4c3bb`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c832c8aa0f75d42a0b5184d0da86ae352af4d2af428baf3ea8427549246ec6`  
		Last Modified: Fri, 03 Apr 2026 16:46:53 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f4f6001c72610967203addf8b926876430b9c52781bc7c439cdf4b1a76c53b9`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e81457c0d32514fdbd102216b8ac825e76f3eea16f82416bfa0b0ca81d4002f`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d994f7c5a9a4b867ee40e071f6beba8dfad23380b03befd4a7ec54ad23e51e`  
		Last Modified: Fri, 03 Apr 2026 16:46:54 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.7.17-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9674c041d0669f0b8dc6b3faf7d36d006e57e2dbd34b700064dbb68dcec396b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75eed0b2594aa3af22337c26b3dd587253defaa38b3f92557c27aca18645ab1b`

```dockerfile
```

-	Layers:
	-	`sha256:d86b7c7f5fa218dc9501690ff98c77d1b3db572916d08a609164cc903984a512`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.7.17-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:cd900b6fa82dce48c2db0c8da93c925816bc6e610df8d8d13361df0e82a90719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237425482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd089181102c02a75365eb3c0569b41d188c47f16476b258284dd3ec58288ea2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:57 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:57 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:57 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:57 GMT
ARG VERSION=26.2.7.17
# Fri, 03 Apr 2026 16:46:57 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:33 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c357252fe4ab6bd21b7ad7a9772aa8322cc2176c66f36f327bc72e995c27be74`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 7.6 MB (7578928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db46e48e668203be36b20c5cefb526116de1c5b734a5973e7b94cffb01b2a1bc`  
		Last Modified: Fri, 03 Apr 2026 16:48:00 GMT  
		Size: 201.4 MB (201369559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b011289759fccdb26582c7e66d61249c3096e4d15ffa3c805d23f71cf53ea7b`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3459363f19c5ca4ea5786a8e405596e71fb92e1f60b5ff465abb29fcd871bd9f`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad35652b512969d67de755cf23eb2ab52e472dea6f9e87589970a7e989ef08f`  
		Last Modified: Fri, 03 Apr 2026 16:47:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adcc01615593db75c5307ac789e71d234b3e1eb4cb4fd8295f0ca0a567eaea6`  
		Last Modified: Fri, 03 Apr 2026 16:47:56 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad850f833213305621e9d0cfd7bb1dc646ba2ef5a0b2d0d81a8774ebcdd606c`  
		Last Modified: Fri, 03 Apr 2026 16:47:57 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.7.17-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:35ee6f3d9f0c59e4782159aea514954313fa956e56fad02518ac3430da8a0008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1418bb3e74ac61cd695877ecc9fb343cfcd19ebed9374953b891fb6b1302691f`

```dockerfile
```

-	Layers:
	-	`sha256:e1739c7d43e7fd74a2a84dd579ecfc40ca5608357d9325b6d8375fc49c763377`  
		Last Modified: Fri, 03 Apr 2026 16:47:55 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3`

```console
$ docker pull clickhouse@sha256:02a0c018bba7866b3f97557aab010cc421667dcafe341764e905c029dff71e15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:d68be73bdf7be601e717d426579d919def6196a219a9e8e9660627920e841f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30c5c9c2287381bea9f27cd4cbd20d99aac5823b3634d27f1ff3710d25b5e12`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:00 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:46:25 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:46:25 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:46:25 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:46:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6857345950c51ce8ef8a98559cc67a9191790eab8ca6974a456440bef7f3024`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 7.6 MB (7599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99913e78c74cc00b7ba5859eb2066644dad79ce03b4053c07eeb4db6eef32fb6`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 224.2 MB (224151091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8a9db3da8b5351b979f36ea1a601c7a671e67860b6cd410b7c452fa3ecdf70`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599de64d5329ead5c641b48eb53f9b2f6fcf608ad5694fce692c12b7bcc30289`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fd6529f09bf1460de272846c9c33062efc32446d69702ecc77fd1a2a18b111`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e4c0f60f2d8c4e72a5e8fd12f25f5e7c445b213c0c52b17dca35804f2ae9d6`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbcc9e4f59aa4c2dd57c2519381c1d5ad77c89bba110700f3a06e21e102b9eb`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e0b933cfd6b64288ffd271f41f97bb20e197793e721e24c58807796e845fcb88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e68767c605d7427d1a5a629b0df374ac22c0087ca6fad55eb46977f83835dae`

```dockerfile
```

-	Layers:
	-	`sha256:287da0d5ca517c00d2b31090410392f0c6d4e6af497cfd7f909336b50ab0e88b`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 26.6 KB (26639 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2d952953f9eeccce2e5ad717331f9551aa9432b51e0eb613c990b6dd06ad133f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c6aebf9a6816a1e73e3ddb80cc7da96b340d235fa98682fd0a670d813b5bea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:36 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:04 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b17542e7b778221f66900a871553196cd81be4cf3c3d5431cb78d1300cf581`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 7.6 MB (7578950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c2239644aa123e35a001751ddf1e00a88eea237350fcc1fc486c8798a3facd`  
		Last Modified: Fri, 03 Apr 2026 16:47:30 GMT  
		Size: 208.5 MB (208543188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32651eff2c26b01ebe63d89d97859d5810e5face21f18fb0fe78178f86a4e50`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d8766ec53e86c3478782cebcc5a1b67767856c8f99b1f99170f1e8f73c21e0`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b0a8b734471686e3b14611a73c269eab37b6482f710f8c3ad0740f1a1b750d`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5534d29b17931af1771e1ff1ca039f6ff2aa61d56cfc68b93ca33b2307b01af`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d77b7c94dec06a1b0a7a90bcf8f4d1594e135f06fb773a885746afe6cf0676`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:526fb039bcbbeee74b8afc16130a1c390f75a354ccb533da9ee496548fa5be06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033851e448f1c18c1a362fc476c144f484564c60c0d925542d7f563a1770958a`

```dockerfile
```

-	Layers:
	-	`sha256:4c2113e800b23097cd6232f7a54d79ddcb2a5a64b7f59f9a29a7cc69f20e48be`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 26.9 KB (26873 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3-jammy`

```console
$ docker pull clickhouse@sha256:02a0c018bba7866b3f97557aab010cc421667dcafe341764e905c029dff71e15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:d68be73bdf7be601e717d426579d919def6196a219a9e8e9660627920e841f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30c5c9c2287381bea9f27cd4cbd20d99aac5823b3634d27f1ff3710d25b5e12`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:00 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:46:25 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:46:25 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:46:25 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:46:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6857345950c51ce8ef8a98559cc67a9191790eab8ca6974a456440bef7f3024`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 7.6 MB (7599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99913e78c74cc00b7ba5859eb2066644dad79ce03b4053c07eeb4db6eef32fb6`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 224.2 MB (224151091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8a9db3da8b5351b979f36ea1a601c7a671e67860b6cd410b7c452fa3ecdf70`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599de64d5329ead5c641b48eb53f9b2f6fcf608ad5694fce692c12b7bcc30289`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fd6529f09bf1460de272846c9c33062efc32446d69702ecc77fd1a2a18b111`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e4c0f60f2d8c4e72a5e8fd12f25f5e7c445b213c0c52b17dca35804f2ae9d6`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbcc9e4f59aa4c2dd57c2519381c1d5ad77c89bba110700f3a06e21e102b9eb`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e0b933cfd6b64288ffd271f41f97bb20e197793e721e24c58807796e845fcb88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e68767c605d7427d1a5a629b0df374ac22c0087ca6fad55eb46977f83835dae`

```dockerfile
```

-	Layers:
	-	`sha256:287da0d5ca517c00d2b31090410392f0c6d4e6af497cfd7f909336b50ab0e88b`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 26.6 KB (26639 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2d952953f9eeccce2e5ad717331f9551aa9432b51e0eb613c990b6dd06ad133f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c6aebf9a6816a1e73e3ddb80cc7da96b340d235fa98682fd0a670d813b5bea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:36 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:04 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b17542e7b778221f66900a871553196cd81be4cf3c3d5431cb78d1300cf581`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 7.6 MB (7578950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c2239644aa123e35a001751ddf1e00a88eea237350fcc1fc486c8798a3facd`  
		Last Modified: Fri, 03 Apr 2026 16:47:30 GMT  
		Size: 208.5 MB (208543188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32651eff2c26b01ebe63d89d97859d5810e5face21f18fb0fe78178f86a4e50`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d8766ec53e86c3478782cebcc5a1b67767856c8f99b1f99170f1e8f73c21e0`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b0a8b734471686e3b14611a73c269eab37b6482f710f8c3ad0740f1a1b750d`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5534d29b17931af1771e1ff1ca039f6ff2aa61d56cfc68b93ca33b2307b01af`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d77b7c94dec06a1b0a7a90bcf8f4d1594e135f06fb773a885746afe6cf0676`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:526fb039bcbbeee74b8afc16130a1c390f75a354ccb533da9ee496548fa5be06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033851e448f1c18c1a362fc476c144f484564c60c0d925542d7f563a1770958a`

```dockerfile
```

-	Layers:
	-	`sha256:4c2113e800b23097cd6232f7a54d79ddcb2a5a64b7f59f9a29a7cc69f20e48be`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 26.9 KB (26873 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.3`

```console
$ docker pull clickhouse@sha256:02a0c018bba7866b3f97557aab010cc421667dcafe341764e905c029dff71e15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:d68be73bdf7be601e717d426579d919def6196a219a9e8e9660627920e841f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30c5c9c2287381bea9f27cd4cbd20d99aac5823b3634d27f1ff3710d25b5e12`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:00 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:46:25 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:46:25 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:46:25 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:46:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6857345950c51ce8ef8a98559cc67a9191790eab8ca6974a456440bef7f3024`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 7.6 MB (7599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99913e78c74cc00b7ba5859eb2066644dad79ce03b4053c07eeb4db6eef32fb6`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 224.2 MB (224151091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8a9db3da8b5351b979f36ea1a601c7a671e67860b6cd410b7c452fa3ecdf70`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599de64d5329ead5c641b48eb53f9b2f6fcf608ad5694fce692c12b7bcc30289`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fd6529f09bf1460de272846c9c33062efc32446d69702ecc77fd1a2a18b111`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e4c0f60f2d8c4e72a5e8fd12f25f5e7c445b213c0c52b17dca35804f2ae9d6`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbcc9e4f59aa4c2dd57c2519381c1d5ad77c89bba110700f3a06e21e102b9eb`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e0b933cfd6b64288ffd271f41f97bb20e197793e721e24c58807796e845fcb88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e68767c605d7427d1a5a629b0df374ac22c0087ca6fad55eb46977f83835dae`

```dockerfile
```

-	Layers:
	-	`sha256:287da0d5ca517c00d2b31090410392f0c6d4e6af497cfd7f909336b50ab0e88b`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 26.6 KB (26639 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2d952953f9eeccce2e5ad717331f9551aa9432b51e0eb613c990b6dd06ad133f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c6aebf9a6816a1e73e3ddb80cc7da96b340d235fa98682fd0a670d813b5bea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:36 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:04 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b17542e7b778221f66900a871553196cd81be4cf3c3d5431cb78d1300cf581`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 7.6 MB (7578950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c2239644aa123e35a001751ddf1e00a88eea237350fcc1fc486c8798a3facd`  
		Last Modified: Fri, 03 Apr 2026 16:47:30 GMT  
		Size: 208.5 MB (208543188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32651eff2c26b01ebe63d89d97859d5810e5face21f18fb0fe78178f86a4e50`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d8766ec53e86c3478782cebcc5a1b67767856c8f99b1f99170f1e8f73c21e0`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b0a8b734471686e3b14611a73c269eab37b6482f710f8c3ad0740f1a1b750d`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5534d29b17931af1771e1ff1ca039f6ff2aa61d56cfc68b93ca33b2307b01af`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d77b7c94dec06a1b0a7a90bcf8f4d1594e135f06fb773a885746afe6cf0676`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:526fb039bcbbeee74b8afc16130a1c390f75a354ccb533da9ee496548fa5be06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033851e448f1c18c1a362fc476c144f484564c60c0d925542d7f563a1770958a`

```dockerfile
```

-	Layers:
	-	`sha256:4c2113e800b23097cd6232f7a54d79ddcb2a5a64b7f59f9a29a7cc69f20e48be`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 26.9 KB (26873 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.3-jammy`

```console
$ docker pull clickhouse@sha256:02a0c018bba7866b3f97557aab010cc421667dcafe341764e905c029dff71e15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:d68be73bdf7be601e717d426579d919def6196a219a9e8e9660627920e841f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30c5c9c2287381bea9f27cd4cbd20d99aac5823b3634d27f1ff3710d25b5e12`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:00 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:46:25 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:46:25 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:46:25 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:46:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6857345950c51ce8ef8a98559cc67a9191790eab8ca6974a456440bef7f3024`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 7.6 MB (7599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99913e78c74cc00b7ba5859eb2066644dad79ce03b4053c07eeb4db6eef32fb6`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 224.2 MB (224151091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8a9db3da8b5351b979f36ea1a601c7a671e67860b6cd410b7c452fa3ecdf70`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599de64d5329ead5c641b48eb53f9b2f6fcf608ad5694fce692c12b7bcc30289`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fd6529f09bf1460de272846c9c33062efc32446d69702ecc77fd1a2a18b111`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e4c0f60f2d8c4e72a5e8fd12f25f5e7c445b213c0c52b17dca35804f2ae9d6`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbcc9e4f59aa4c2dd57c2519381c1d5ad77c89bba110700f3a06e21e102b9eb`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e0b933cfd6b64288ffd271f41f97bb20e197793e721e24c58807796e845fcb88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e68767c605d7427d1a5a629b0df374ac22c0087ca6fad55eb46977f83835dae`

```dockerfile
```

-	Layers:
	-	`sha256:287da0d5ca517c00d2b31090410392f0c6d4e6af497cfd7f909336b50ab0e88b`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 26.6 KB (26639 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2d952953f9eeccce2e5ad717331f9551aa9432b51e0eb613c990b6dd06ad133f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c6aebf9a6816a1e73e3ddb80cc7da96b340d235fa98682fd0a670d813b5bea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:36 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:04 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b17542e7b778221f66900a871553196cd81be4cf3c3d5431cb78d1300cf581`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 7.6 MB (7578950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c2239644aa123e35a001751ddf1e00a88eea237350fcc1fc486c8798a3facd`  
		Last Modified: Fri, 03 Apr 2026 16:47:30 GMT  
		Size: 208.5 MB (208543188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32651eff2c26b01ebe63d89d97859d5810e5face21f18fb0fe78178f86a4e50`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d8766ec53e86c3478782cebcc5a1b67767856c8f99b1f99170f1e8f73c21e0`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b0a8b734471686e3b14611a73c269eab37b6482f710f8c3ad0740f1a1b750d`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5534d29b17931af1771e1ff1ca039f6ff2aa61d56cfc68b93ca33b2307b01af`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d77b7c94dec06a1b0a7a90bcf8f4d1594e135f06fb773a885746afe6cf0676`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:526fb039bcbbeee74b8afc16130a1c390f75a354ccb533da9ee496548fa5be06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033851e448f1c18c1a362fc476c144f484564c60c0d925542d7f563a1770958a`

```dockerfile
```

-	Layers:
	-	`sha256:4c2113e800b23097cd6232f7a54d79ddcb2a5a64b7f59f9a29a7cc69f20e48be`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 26.9 KB (26873 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.3.20`

```console
$ docker pull clickhouse@sha256:02a0c018bba7866b3f97557aab010cc421667dcafe341764e905c029dff71e15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.3.20` - linux; amd64

```console
$ docker pull clickhouse@sha256:d68be73bdf7be601e717d426579d919def6196a219a9e8e9660627920e841f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30c5c9c2287381bea9f27cd4cbd20d99aac5823b3634d27f1ff3710d25b5e12`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:00 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:46:25 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:46:25 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:46:25 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:46:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6857345950c51ce8ef8a98559cc67a9191790eab8ca6974a456440bef7f3024`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 7.6 MB (7599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99913e78c74cc00b7ba5859eb2066644dad79ce03b4053c07eeb4db6eef32fb6`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 224.2 MB (224151091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8a9db3da8b5351b979f36ea1a601c7a671e67860b6cd410b7c452fa3ecdf70`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599de64d5329ead5c641b48eb53f9b2f6fcf608ad5694fce692c12b7bcc30289`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fd6529f09bf1460de272846c9c33062efc32446d69702ecc77fd1a2a18b111`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e4c0f60f2d8c4e72a5e8fd12f25f5e7c445b213c0c52b17dca35804f2ae9d6`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbcc9e4f59aa4c2dd57c2519381c1d5ad77c89bba110700f3a06e21e102b9eb`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.3.20` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e0b933cfd6b64288ffd271f41f97bb20e197793e721e24c58807796e845fcb88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e68767c605d7427d1a5a629b0df374ac22c0087ca6fad55eb46977f83835dae`

```dockerfile
```

-	Layers:
	-	`sha256:287da0d5ca517c00d2b31090410392f0c6d4e6af497cfd7f909336b50ab0e88b`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 26.6 KB (26639 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.3.20` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2d952953f9eeccce2e5ad717331f9551aa9432b51e0eb613c990b6dd06ad133f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c6aebf9a6816a1e73e3ddb80cc7da96b340d235fa98682fd0a670d813b5bea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:36 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:04 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b17542e7b778221f66900a871553196cd81be4cf3c3d5431cb78d1300cf581`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 7.6 MB (7578950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c2239644aa123e35a001751ddf1e00a88eea237350fcc1fc486c8798a3facd`  
		Last Modified: Fri, 03 Apr 2026 16:47:30 GMT  
		Size: 208.5 MB (208543188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32651eff2c26b01ebe63d89d97859d5810e5face21f18fb0fe78178f86a4e50`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d8766ec53e86c3478782cebcc5a1b67767856c8f99b1f99170f1e8f73c21e0`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b0a8b734471686e3b14611a73c269eab37b6482f710f8c3ad0740f1a1b750d`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5534d29b17931af1771e1ff1ca039f6ff2aa61d56cfc68b93ca33b2307b01af`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d77b7c94dec06a1b0a7a90bcf8f4d1594e135f06fb773a885746afe6cf0676`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.3.20` - unknown; unknown

```console
$ docker pull clickhouse@sha256:526fb039bcbbeee74b8afc16130a1c390f75a354ccb533da9ee496548fa5be06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033851e448f1c18c1a362fc476c144f484564c60c0d925542d7f563a1770958a`

```dockerfile
```

-	Layers:
	-	`sha256:4c2113e800b23097cd6232f7a54d79ddcb2a5a64b7f59f9a29a7cc69f20e48be`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 26.9 KB (26873 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.3.20-jammy`

```console
$ docker pull clickhouse@sha256:02a0c018bba7866b3f97557aab010cc421667dcafe341764e905c029dff71e15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.3.20-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:d68be73bdf7be601e717d426579d919def6196a219a9e8e9660627920e841f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30c5c9c2287381bea9f27cd4cbd20d99aac5823b3634d27f1ff3710d25b5e12`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:00 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:46:25 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:46:25 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:46:25 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:46:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6857345950c51ce8ef8a98559cc67a9191790eab8ca6974a456440bef7f3024`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 7.6 MB (7599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99913e78c74cc00b7ba5859eb2066644dad79ce03b4053c07eeb4db6eef32fb6`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 224.2 MB (224151091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8a9db3da8b5351b979f36ea1a601c7a671e67860b6cd410b7c452fa3ecdf70`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599de64d5329ead5c641b48eb53f9b2f6fcf608ad5694fce692c12b7bcc30289`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fd6529f09bf1460de272846c9c33062efc32446d69702ecc77fd1a2a18b111`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e4c0f60f2d8c4e72a5e8fd12f25f5e7c445b213c0c52b17dca35804f2ae9d6`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbcc9e4f59aa4c2dd57c2519381c1d5ad77c89bba110700f3a06e21e102b9eb`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.3.20-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e0b933cfd6b64288ffd271f41f97bb20e197793e721e24c58807796e845fcb88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e68767c605d7427d1a5a629b0df374ac22c0087ca6fad55eb46977f83835dae`

```dockerfile
```

-	Layers:
	-	`sha256:287da0d5ca517c00d2b31090410392f0c6d4e6af497cfd7f909336b50ab0e88b`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 26.6 KB (26639 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.3.20-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2d952953f9eeccce2e5ad717331f9551aa9432b51e0eb613c990b6dd06ad133f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c6aebf9a6816a1e73e3ddb80cc7da96b340d235fa98682fd0a670d813b5bea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:36 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:04 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b17542e7b778221f66900a871553196cd81be4cf3c3d5431cb78d1300cf581`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 7.6 MB (7578950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c2239644aa123e35a001751ddf1e00a88eea237350fcc1fc486c8798a3facd`  
		Last Modified: Fri, 03 Apr 2026 16:47:30 GMT  
		Size: 208.5 MB (208543188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32651eff2c26b01ebe63d89d97859d5810e5face21f18fb0fe78178f86a4e50`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d8766ec53e86c3478782cebcc5a1b67767856c8f99b1f99170f1e8f73c21e0`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b0a8b734471686e3b14611a73c269eab37b6482f710f8c3ad0740f1a1b750d`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5534d29b17931af1771e1ff1ca039f6ff2aa61d56cfc68b93ca33b2307b01af`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d77b7c94dec06a1b0a7a90bcf8f4d1594e135f06fb773a885746afe6cf0676`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.3.20-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:526fb039bcbbeee74b8afc16130a1c390f75a354ccb533da9ee496548fa5be06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033851e448f1c18c1a362fc476c144f484564c60c0d925542d7f563a1770958a`

```dockerfile
```

-	Layers:
	-	`sha256:4c2113e800b23097cd6232f7a54d79ddcb2a5a64b7f59f9a29a7cc69f20e48be`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 26.9 KB (26873 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:02a0c018bba7866b3f97557aab010cc421667dcafe341764e905c029dff71e15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:d68be73bdf7be601e717d426579d919def6196a219a9e8e9660627920e841f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30c5c9c2287381bea9f27cd4cbd20d99aac5823b3634d27f1ff3710d25b5e12`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:00 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:46:25 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:46:25 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:46:25 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:46:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6857345950c51ce8ef8a98559cc67a9191790eab8ca6974a456440bef7f3024`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 7.6 MB (7599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99913e78c74cc00b7ba5859eb2066644dad79ce03b4053c07eeb4db6eef32fb6`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 224.2 MB (224151091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8a9db3da8b5351b979f36ea1a601c7a671e67860b6cd410b7c452fa3ecdf70`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599de64d5329ead5c641b48eb53f9b2f6fcf608ad5694fce692c12b7bcc30289`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fd6529f09bf1460de272846c9c33062efc32446d69702ecc77fd1a2a18b111`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e4c0f60f2d8c4e72a5e8fd12f25f5e7c445b213c0c52b17dca35804f2ae9d6`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbcc9e4f59aa4c2dd57c2519381c1d5ad77c89bba110700f3a06e21e102b9eb`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e0b933cfd6b64288ffd271f41f97bb20e197793e721e24c58807796e845fcb88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e68767c605d7427d1a5a629b0df374ac22c0087ca6fad55eb46977f83835dae`

```dockerfile
```

-	Layers:
	-	`sha256:287da0d5ca517c00d2b31090410392f0c6d4e6af497cfd7f909336b50ab0e88b`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 26.6 KB (26639 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2d952953f9eeccce2e5ad717331f9551aa9432b51e0eb613c990b6dd06ad133f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c6aebf9a6816a1e73e3ddb80cc7da96b340d235fa98682fd0a670d813b5bea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:36 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:04 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b17542e7b778221f66900a871553196cd81be4cf3c3d5431cb78d1300cf581`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 7.6 MB (7578950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c2239644aa123e35a001751ddf1e00a88eea237350fcc1fc486c8798a3facd`  
		Last Modified: Fri, 03 Apr 2026 16:47:30 GMT  
		Size: 208.5 MB (208543188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32651eff2c26b01ebe63d89d97859d5810e5face21f18fb0fe78178f86a4e50`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d8766ec53e86c3478782cebcc5a1b67767856c8f99b1f99170f1e8f73c21e0`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b0a8b734471686e3b14611a73c269eab37b6482f710f8c3ad0740f1a1b750d`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5534d29b17931af1771e1ff1ca039f6ff2aa61d56cfc68b93ca33b2307b01af`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d77b7c94dec06a1b0a7a90bcf8f4d1594e135f06fb773a885746afe6cf0676`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:526fb039bcbbeee74b8afc16130a1c390f75a354ccb533da9ee496548fa5be06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033851e448f1c18c1a362fc476c144f484564c60c0d925542d7f563a1770958a`

```dockerfile
```

-	Layers:
	-	`sha256:4c2113e800b23097cd6232f7a54d79ddcb2a5a64b7f59f9a29a7cc69f20e48be`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 26.9 KB (26873 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:02a0c018bba7866b3f97557aab010cc421667dcafe341764e905c029dff71e15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:d68be73bdf7be601e717d426579d919def6196a219a9e8e9660627920e841f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30c5c9c2287381bea9f27cd4cbd20d99aac5823b3634d27f1ff3710d25b5e12`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:00 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:46:25 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:46:25 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:46:25 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:46:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6857345950c51ce8ef8a98559cc67a9191790eab8ca6974a456440bef7f3024`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 7.6 MB (7599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99913e78c74cc00b7ba5859eb2066644dad79ce03b4053c07eeb4db6eef32fb6`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 224.2 MB (224151091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8a9db3da8b5351b979f36ea1a601c7a671e67860b6cd410b7c452fa3ecdf70`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599de64d5329ead5c641b48eb53f9b2f6fcf608ad5694fce692c12b7bcc30289`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fd6529f09bf1460de272846c9c33062efc32446d69702ecc77fd1a2a18b111`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e4c0f60f2d8c4e72a5e8fd12f25f5e7c445b213c0c52b17dca35804f2ae9d6`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbcc9e4f59aa4c2dd57c2519381c1d5ad77c89bba110700f3a06e21e102b9eb`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e0b933cfd6b64288ffd271f41f97bb20e197793e721e24c58807796e845fcb88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e68767c605d7427d1a5a629b0df374ac22c0087ca6fad55eb46977f83835dae`

```dockerfile
```

-	Layers:
	-	`sha256:287da0d5ca517c00d2b31090410392f0c6d4e6af497cfd7f909336b50ab0e88b`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 26.6 KB (26639 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2d952953f9eeccce2e5ad717331f9551aa9432b51e0eb613c990b6dd06ad133f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c6aebf9a6816a1e73e3ddb80cc7da96b340d235fa98682fd0a670d813b5bea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:36 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:04 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b17542e7b778221f66900a871553196cd81be4cf3c3d5431cb78d1300cf581`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 7.6 MB (7578950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c2239644aa123e35a001751ddf1e00a88eea237350fcc1fc486c8798a3facd`  
		Last Modified: Fri, 03 Apr 2026 16:47:30 GMT  
		Size: 208.5 MB (208543188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32651eff2c26b01ebe63d89d97859d5810e5face21f18fb0fe78178f86a4e50`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d8766ec53e86c3478782cebcc5a1b67767856c8f99b1f99170f1e8f73c21e0`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b0a8b734471686e3b14611a73c269eab37b6482f710f8c3ad0740f1a1b750d`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5534d29b17931af1771e1ff1ca039f6ff2aa61d56cfc68b93ca33b2307b01af`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d77b7c94dec06a1b0a7a90bcf8f4d1594e135f06fb773a885746afe6cf0676`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:526fb039bcbbeee74b8afc16130a1c390f75a354ccb533da9ee496548fa5be06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033851e448f1c18c1a362fc476c144f484564c60c0d925542d7f563a1770958a`

```dockerfile
```

-	Layers:
	-	`sha256:4c2113e800b23097cd6232f7a54d79ddcb2a5a64b7f59f9a29a7cc69f20e48be`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 26.9 KB (26873 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:02a0c018bba7866b3f97557aab010cc421667dcafe341764e905c029dff71e15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:d68be73bdf7be601e717d426579d919def6196a219a9e8e9660627920e841f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30c5c9c2287381bea9f27cd4cbd20d99aac5823b3634d27f1ff3710d25b5e12`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:00 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:46:25 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:46:25 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:46:25 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:46:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6857345950c51ce8ef8a98559cc67a9191790eab8ca6974a456440bef7f3024`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 7.6 MB (7599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99913e78c74cc00b7ba5859eb2066644dad79ce03b4053c07eeb4db6eef32fb6`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 224.2 MB (224151091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8a9db3da8b5351b979f36ea1a601c7a671e67860b6cd410b7c452fa3ecdf70`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599de64d5329ead5c641b48eb53f9b2f6fcf608ad5694fce692c12b7bcc30289`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fd6529f09bf1460de272846c9c33062efc32446d69702ecc77fd1a2a18b111`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e4c0f60f2d8c4e72a5e8fd12f25f5e7c445b213c0c52b17dca35804f2ae9d6`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbcc9e4f59aa4c2dd57c2519381c1d5ad77c89bba110700f3a06e21e102b9eb`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e0b933cfd6b64288ffd271f41f97bb20e197793e721e24c58807796e845fcb88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e68767c605d7427d1a5a629b0df374ac22c0087ca6fad55eb46977f83835dae`

```dockerfile
```

-	Layers:
	-	`sha256:287da0d5ca517c00d2b31090410392f0c6d4e6af497cfd7f909336b50ab0e88b`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 26.6 KB (26639 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2d952953f9eeccce2e5ad717331f9551aa9432b51e0eb613c990b6dd06ad133f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c6aebf9a6816a1e73e3ddb80cc7da96b340d235fa98682fd0a670d813b5bea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:36 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:04 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b17542e7b778221f66900a871553196cd81be4cf3c3d5431cb78d1300cf581`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 7.6 MB (7578950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c2239644aa123e35a001751ddf1e00a88eea237350fcc1fc486c8798a3facd`  
		Last Modified: Fri, 03 Apr 2026 16:47:30 GMT  
		Size: 208.5 MB (208543188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32651eff2c26b01ebe63d89d97859d5810e5face21f18fb0fe78178f86a4e50`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d8766ec53e86c3478782cebcc5a1b67767856c8f99b1f99170f1e8f73c21e0`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b0a8b734471686e3b14611a73c269eab37b6482f710f8c3ad0740f1a1b750d`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5534d29b17931af1771e1ff1ca039f6ff2aa61d56cfc68b93ca33b2307b01af`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d77b7c94dec06a1b0a7a90bcf8f4d1594e135f06fb773a885746afe6cf0676`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:526fb039bcbbeee74b8afc16130a1c390f75a354ccb533da9ee496548fa5be06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033851e448f1c18c1a362fc476c144f484564c60c0d925542d7f563a1770958a`

```dockerfile
```

-	Layers:
	-	`sha256:4c2113e800b23097cd6232f7a54d79ddcb2a5a64b7f59f9a29a7cc69f20e48be`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 26.9 KB (26873 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:02a0c018bba7866b3f97557aab010cc421667dcafe341764e905c029dff71e15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:d68be73bdf7be601e717d426579d919def6196a219a9e8e9660627920e841f16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30c5c9c2287381bea9f27cd4cbd20d99aac5823b3634d27f1ff3710d25b5e12`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:00 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:46:25 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:46:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:46:25 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:46:25 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:46:25 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:46:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6857345950c51ce8ef8a98559cc67a9191790eab8ca6974a456440bef7f3024`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 7.6 MB (7599152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99913e78c74cc00b7ba5859eb2066644dad79ce03b4053c07eeb4db6eef32fb6`  
		Last Modified: Fri, 03 Apr 2026 16:46:52 GMT  
		Size: 224.2 MB (224151091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8a9db3da8b5351b979f36ea1a601c7a671e67860b6cd410b7c452fa3ecdf70`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599de64d5329ead5c641b48eb53f9b2f6fcf608ad5694fce692c12b7bcc30289`  
		Last Modified: Fri, 03 Apr 2026 16:46:48 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fd6529f09bf1460de272846c9c33062efc32446d69702ecc77fd1a2a18b111`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e4c0f60f2d8c4e72a5e8fd12f25f5e7c445b213c0c52b17dca35804f2ae9d6`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbcc9e4f59aa4c2dd57c2519381c1d5ad77c89bba110700f3a06e21e102b9eb`  
		Last Modified: Fri, 03 Apr 2026 16:46:49 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e0b933cfd6b64288ffd271f41f97bb20e197793e721e24c58807796e845fcb88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e68767c605d7427d1a5a629b0df374ac22c0087ca6fad55eb46977f83835dae`

```dockerfile
```

-	Layers:
	-	`sha256:287da0d5ca517c00d2b31090410392f0c6d4e6af497cfd7f909336b50ab0e88b`  
		Last Modified: Fri, 03 Apr 2026 16:46:47 GMT  
		Size: 26.6 KB (26639 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2d952953f9eeccce2e5ad717331f9551aa9432b51e0eb613c990b6dd06ad133f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36c6aebf9a6816a1e73e3ddb80cc7da96b340d235fa98682fd0a670d813b5bea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:14:08 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:14:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:14:08 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:14:11 GMT
ADD file:fed1a3166c21242469434b8e80ba5e315ccbaa7a7875551de1484fa034ccbde2 in / 
# Sun, 22 Mar 2026 18:14:11 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 16:46:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 03 Apr 2026 16:46:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 03 Apr 2026 16:46:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 03 Apr 2026 16:46:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 03 Apr 2026 16:46:36 GMT
ARG VERSION=26.3.3.20
# Fri, 03 Apr 2026 16:46:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 03 Apr 2026 16:47:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 03 Apr 2026 16:47:04 GMT
ENV TZ=UTC
# Fri, 03 Apr 2026 16:47:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 03 Apr 2026 16:47:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 03 Apr 2026 16:47:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 03 Apr 2026 16:47:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 03 Apr 2026 16:47:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:4e87bccff4c7739e349affe6ce8362fd45eedb0153cc5a1fc71fda623b506246`  
		Last Modified: Sun, 22 Mar 2026 18:43:32 GMT  
		Size: 27.6 MB (27606943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b17542e7b778221f66900a871553196cd81be4cf3c3d5431cb78d1300cf581`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 7.6 MB (7578950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c2239644aa123e35a001751ddf1e00a88eea237350fcc1fc486c8798a3facd`  
		Last Modified: Fri, 03 Apr 2026 16:47:30 GMT  
		Size: 208.5 MB (208543188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32651eff2c26b01ebe63d89d97859d5810e5face21f18fb0fe78178f86a4e50`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d8766ec53e86c3478782cebcc5a1b67767856c8f99b1f99170f1e8f73c21e0`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87b0a8b734471686e3b14611a73c269eab37b6482f710f8c3ad0740f1a1b750d`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5534d29b17931af1771e1ff1ca039f6ff2aa61d56cfc68b93ca33b2307b01af`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d77b7c94dec06a1b0a7a90bcf8f4d1594e135f06fb773a885746afe6cf0676`  
		Last Modified: Fri, 03 Apr 2026 16:47:27 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:526fb039bcbbeee74b8afc16130a1c390f75a354ccb533da9ee496548fa5be06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:033851e448f1c18c1a362fc476c144f484564c60c0d925542d7f563a1770958a`

```dockerfile
```

-	Layers:
	-	`sha256:4c2113e800b23097cd6232f7a54d79ddcb2a5a64b7f59f9a29a7cc69f20e48be`  
		Last Modified: Fri, 03 Apr 2026 16:47:26 GMT  
		Size: 26.9 KB (26873 bytes)  
		MIME: application/vnd.in-toto+json
