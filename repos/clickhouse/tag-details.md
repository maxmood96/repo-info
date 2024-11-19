<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:24`](#clickhouse24)
-	[`clickhouse:24-focal`](#clickhouse24-focal)
-	[`clickhouse:24.10`](#clickhouse2410)
-	[`clickhouse:24.10-focal`](#clickhouse2410-focal)
-	[`clickhouse:24.10.2`](#clickhouse24102)
-	[`clickhouse:24.10.2-focal`](#clickhouse24102-focal)
-	[`clickhouse:24.10.2.80`](#clickhouse2410280)
-	[`clickhouse:24.10.2.80-focal`](#clickhouse2410280-focal)
-	[`clickhouse:24.3`](#clickhouse243)
-	[`clickhouse:24.3-focal`](#clickhouse243-focal)
-	[`clickhouse:24.3.14`](#clickhouse24314)
-	[`clickhouse:24.3.14-focal`](#clickhouse24314-focal)
-	[`clickhouse:24.3.14.35`](#clickhouse2431435)
-	[`clickhouse:24.3.14.35-focal`](#clickhouse2431435-focal)
-	[`clickhouse:24.8`](#clickhouse248)
-	[`clickhouse:24.8-focal`](#clickhouse248-focal)
-	[`clickhouse:24.8.7`](#clickhouse2487)
-	[`clickhouse:24.8.7-focal`](#clickhouse2487-focal)
-	[`clickhouse:24.8.7.41`](#clickhouse248741)
-	[`clickhouse:24.8.7.41-focal`](#clickhouse248741-focal)
-	[`clickhouse:24.9`](#clickhouse249)
-	[`clickhouse:24.9-focal`](#clickhouse249-focal)
-	[`clickhouse:24.9.3`](#clickhouse2493)
-	[`clickhouse:24.9.3-focal`](#clickhouse2493-focal)
-	[`clickhouse:24.9.3.128`](#clickhouse2493128)
-	[`clickhouse:24.9.3.128-focal`](#clickhouse2493128-focal)
-	[`clickhouse:focal`](#clickhousefocal)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-focal`](#clickhouselts-focal)

## `clickhouse:24`

```console
$ docker pull clickhouse@sha256:aa887dfaa8d915a18ad93d25cef0334138ffeeb386353600ed90ecf07ff4eb5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24` - linux; amd64

```console
$ docker pull clickhouse@sha256:3073efa0428c680834cf03dd2428fac3408a8a60310cd0613f51731eb25bcdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180553647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33410aa159ab43ebeaa868575df2dc69997cf9bbc495f419df632b5938060b2e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11845068165d574aa2798c6158bf4904622cd7aff2c5675c6643ff0ba4fda74`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 8.8 MB (8802587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5feec6ebdd2d272ba4886d83efac935f56f806e73e527a868a28138c61e67718`  
		Last Modified: Mon, 18 Nov 2024 21:06:08 GMT  
		Size: 143.4 MB (143372719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfeab913ab2cc5b1eae6e120652382b1e4419e753305cbecd10ed1fd65a4bc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1a6ccef3905d7f4b64758101a5566220595da9cd94b3a8efe3c7c3d500827`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52154b45f848fae4d6dc15923fd51d332c33b0e778b1c11e06eb83e661dd7a95`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b265890db07ff12d8c1d5226fa954754fc2424e3c212fb8ec6357953893fe05f`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff950eeed9b85019e89aaffe2962b82fdbc03b54f59941891af221eb1511d3a4`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24` - unknown; unknown

```console
$ docker pull clickhouse@sha256:064a3c846ada78d4c69bda131ebe8c761653440c1cc0f3585a7a48d399021fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c888f3eb66030483fa7a082a00d60e89b78ac7a1f1e67da42a74eca0169fae`

```dockerfile
```

-	Layers:
	-	`sha256:f50539b9c37f17df612e4afdb20de110705ae3090a3db1da1b402faa4f251cc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:05 GMT  
		Size: 26.5 KB (26499 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f36884dc6d24d60a9bb6c320e8a052190ae2358d8f66efc4c71ad5ffa4638d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174195698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68ae827e8dcb485e903cb0057678535df1e43de4da3302cf7efd6fb2bcb936e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86846b838547ebb3f9804d50f4fe8eb4f6bfeff8d4821e1998c250e0dfd1a11`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 8.7 MB (8662233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7371f123ab3df4a130514d8f7597c2f06a212dda18e5943a8eb98574c2d0b52`  
		Last Modified: Mon, 18 Nov 2024 20:05:57 GMT  
		Size: 138.7 MB (138692361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a627ba3ba9c0dd7675bded26bee97be800d7ae7233b65cc5e87dec6385d6d684`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eab81eafda560d04753033a7793b0fbad07c01a37f4e1fa1b6cbb5d57fbe8d`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b4918a2555f120c31a57c5c66f22600ab0bc3d121542385b9eb52b639f3796`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6c7d5229f43bb415dcabb1c0fd300ecc1dbfed18d77c6e553ba203fcc0d0`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30b9bec89bc291fd156ad60a897a8bc119acda2d3294db0909a7abb9b7aa124`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2f77217c545db83c44c23cc6abdf4f34ce68265d9e261c4af075dc598e2811bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca457bdd672219881e4c7f28900a0fb3c0f87120ecf163a2c6fbfddd3eb9cf2d`

```dockerfile
```

-	Layers:
	-	`sha256:5791af50f4fcfa896eb3c0edf644ae24c07abc17fd5982c1cbb1724b8ede7636`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 26.7 KB (26735 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24-focal`

```console
$ docker pull clickhouse@sha256:aa887dfaa8d915a18ad93d25cef0334138ffeeb386353600ed90ecf07ff4eb5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:3073efa0428c680834cf03dd2428fac3408a8a60310cd0613f51731eb25bcdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180553647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33410aa159ab43ebeaa868575df2dc69997cf9bbc495f419df632b5938060b2e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11845068165d574aa2798c6158bf4904622cd7aff2c5675c6643ff0ba4fda74`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 8.8 MB (8802587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5feec6ebdd2d272ba4886d83efac935f56f806e73e527a868a28138c61e67718`  
		Last Modified: Mon, 18 Nov 2024 21:06:08 GMT  
		Size: 143.4 MB (143372719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfeab913ab2cc5b1eae6e120652382b1e4419e753305cbecd10ed1fd65a4bc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1a6ccef3905d7f4b64758101a5566220595da9cd94b3a8efe3c7c3d500827`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52154b45f848fae4d6dc15923fd51d332c33b0e778b1c11e06eb83e661dd7a95`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b265890db07ff12d8c1d5226fa954754fc2424e3c212fb8ec6357953893fe05f`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff950eeed9b85019e89aaffe2962b82fdbc03b54f59941891af221eb1511d3a4`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:064a3c846ada78d4c69bda131ebe8c761653440c1cc0f3585a7a48d399021fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c888f3eb66030483fa7a082a00d60e89b78ac7a1f1e67da42a74eca0169fae`

```dockerfile
```

-	Layers:
	-	`sha256:f50539b9c37f17df612e4afdb20de110705ae3090a3db1da1b402faa4f251cc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:05 GMT  
		Size: 26.5 KB (26499 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f36884dc6d24d60a9bb6c320e8a052190ae2358d8f66efc4c71ad5ffa4638d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174195698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68ae827e8dcb485e903cb0057678535df1e43de4da3302cf7efd6fb2bcb936e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86846b838547ebb3f9804d50f4fe8eb4f6bfeff8d4821e1998c250e0dfd1a11`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 8.7 MB (8662233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7371f123ab3df4a130514d8f7597c2f06a212dda18e5943a8eb98574c2d0b52`  
		Last Modified: Mon, 18 Nov 2024 20:05:57 GMT  
		Size: 138.7 MB (138692361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a627ba3ba9c0dd7675bded26bee97be800d7ae7233b65cc5e87dec6385d6d684`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eab81eafda560d04753033a7793b0fbad07c01a37f4e1fa1b6cbb5d57fbe8d`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b4918a2555f120c31a57c5c66f22600ab0bc3d121542385b9eb52b639f3796`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6c7d5229f43bb415dcabb1c0fd300ecc1dbfed18d77c6e553ba203fcc0d0`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30b9bec89bc291fd156ad60a897a8bc119acda2d3294db0909a7abb9b7aa124`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2f77217c545db83c44c23cc6abdf4f34ce68265d9e261c4af075dc598e2811bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca457bdd672219881e4c7f28900a0fb3c0f87120ecf163a2c6fbfddd3eb9cf2d`

```dockerfile
```

-	Layers:
	-	`sha256:5791af50f4fcfa896eb3c0edf644ae24c07abc17fd5982c1cbb1724b8ede7636`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 26.7 KB (26735 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.10`

```console
$ docker pull clickhouse@sha256:aa887dfaa8d915a18ad93d25cef0334138ffeeb386353600ed90ecf07ff4eb5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:3073efa0428c680834cf03dd2428fac3408a8a60310cd0613f51731eb25bcdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180553647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33410aa159ab43ebeaa868575df2dc69997cf9bbc495f419df632b5938060b2e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11845068165d574aa2798c6158bf4904622cd7aff2c5675c6643ff0ba4fda74`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 8.8 MB (8802587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5feec6ebdd2d272ba4886d83efac935f56f806e73e527a868a28138c61e67718`  
		Last Modified: Mon, 18 Nov 2024 21:06:08 GMT  
		Size: 143.4 MB (143372719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfeab913ab2cc5b1eae6e120652382b1e4419e753305cbecd10ed1fd65a4bc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1a6ccef3905d7f4b64758101a5566220595da9cd94b3a8efe3c7c3d500827`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52154b45f848fae4d6dc15923fd51d332c33b0e778b1c11e06eb83e661dd7a95`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b265890db07ff12d8c1d5226fa954754fc2424e3c212fb8ec6357953893fe05f`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff950eeed9b85019e89aaffe2962b82fdbc03b54f59941891af221eb1511d3a4`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:064a3c846ada78d4c69bda131ebe8c761653440c1cc0f3585a7a48d399021fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c888f3eb66030483fa7a082a00d60e89b78ac7a1f1e67da42a74eca0169fae`

```dockerfile
```

-	Layers:
	-	`sha256:f50539b9c37f17df612e4afdb20de110705ae3090a3db1da1b402faa4f251cc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:05 GMT  
		Size: 26.5 KB (26499 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f36884dc6d24d60a9bb6c320e8a052190ae2358d8f66efc4c71ad5ffa4638d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174195698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68ae827e8dcb485e903cb0057678535df1e43de4da3302cf7efd6fb2bcb936e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86846b838547ebb3f9804d50f4fe8eb4f6bfeff8d4821e1998c250e0dfd1a11`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 8.7 MB (8662233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7371f123ab3df4a130514d8f7597c2f06a212dda18e5943a8eb98574c2d0b52`  
		Last Modified: Mon, 18 Nov 2024 20:05:57 GMT  
		Size: 138.7 MB (138692361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a627ba3ba9c0dd7675bded26bee97be800d7ae7233b65cc5e87dec6385d6d684`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eab81eafda560d04753033a7793b0fbad07c01a37f4e1fa1b6cbb5d57fbe8d`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b4918a2555f120c31a57c5c66f22600ab0bc3d121542385b9eb52b639f3796`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6c7d5229f43bb415dcabb1c0fd300ecc1dbfed18d77c6e553ba203fcc0d0`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30b9bec89bc291fd156ad60a897a8bc119acda2d3294db0909a7abb9b7aa124`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2f77217c545db83c44c23cc6abdf4f34ce68265d9e261c4af075dc598e2811bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca457bdd672219881e4c7f28900a0fb3c0f87120ecf163a2c6fbfddd3eb9cf2d`

```dockerfile
```

-	Layers:
	-	`sha256:5791af50f4fcfa896eb3c0edf644ae24c07abc17fd5982c1cbb1724b8ede7636`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 26.7 KB (26735 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.10-focal`

```console
$ docker pull clickhouse@sha256:aa887dfaa8d915a18ad93d25cef0334138ffeeb386353600ed90ecf07ff4eb5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:3073efa0428c680834cf03dd2428fac3408a8a60310cd0613f51731eb25bcdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180553647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33410aa159ab43ebeaa868575df2dc69997cf9bbc495f419df632b5938060b2e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11845068165d574aa2798c6158bf4904622cd7aff2c5675c6643ff0ba4fda74`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 8.8 MB (8802587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5feec6ebdd2d272ba4886d83efac935f56f806e73e527a868a28138c61e67718`  
		Last Modified: Mon, 18 Nov 2024 21:06:08 GMT  
		Size: 143.4 MB (143372719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfeab913ab2cc5b1eae6e120652382b1e4419e753305cbecd10ed1fd65a4bc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1a6ccef3905d7f4b64758101a5566220595da9cd94b3a8efe3c7c3d500827`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52154b45f848fae4d6dc15923fd51d332c33b0e778b1c11e06eb83e661dd7a95`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b265890db07ff12d8c1d5226fa954754fc2424e3c212fb8ec6357953893fe05f`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff950eeed9b85019e89aaffe2962b82fdbc03b54f59941891af221eb1511d3a4`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:064a3c846ada78d4c69bda131ebe8c761653440c1cc0f3585a7a48d399021fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c888f3eb66030483fa7a082a00d60e89b78ac7a1f1e67da42a74eca0169fae`

```dockerfile
```

-	Layers:
	-	`sha256:f50539b9c37f17df612e4afdb20de110705ae3090a3db1da1b402faa4f251cc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:05 GMT  
		Size: 26.5 KB (26499 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f36884dc6d24d60a9bb6c320e8a052190ae2358d8f66efc4c71ad5ffa4638d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174195698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68ae827e8dcb485e903cb0057678535df1e43de4da3302cf7efd6fb2bcb936e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86846b838547ebb3f9804d50f4fe8eb4f6bfeff8d4821e1998c250e0dfd1a11`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 8.7 MB (8662233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7371f123ab3df4a130514d8f7597c2f06a212dda18e5943a8eb98574c2d0b52`  
		Last Modified: Mon, 18 Nov 2024 20:05:57 GMT  
		Size: 138.7 MB (138692361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a627ba3ba9c0dd7675bded26bee97be800d7ae7233b65cc5e87dec6385d6d684`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eab81eafda560d04753033a7793b0fbad07c01a37f4e1fa1b6cbb5d57fbe8d`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b4918a2555f120c31a57c5c66f22600ab0bc3d121542385b9eb52b639f3796`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6c7d5229f43bb415dcabb1c0fd300ecc1dbfed18d77c6e553ba203fcc0d0`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30b9bec89bc291fd156ad60a897a8bc119acda2d3294db0909a7abb9b7aa124`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2f77217c545db83c44c23cc6abdf4f34ce68265d9e261c4af075dc598e2811bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca457bdd672219881e4c7f28900a0fb3c0f87120ecf163a2c6fbfddd3eb9cf2d`

```dockerfile
```

-	Layers:
	-	`sha256:5791af50f4fcfa896eb3c0edf644ae24c07abc17fd5982c1cbb1724b8ede7636`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 26.7 KB (26735 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.10.2`

```console
$ docker pull clickhouse@sha256:aa887dfaa8d915a18ad93d25cef0334138ffeeb386353600ed90ecf07ff4eb5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:3073efa0428c680834cf03dd2428fac3408a8a60310cd0613f51731eb25bcdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180553647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33410aa159ab43ebeaa868575df2dc69997cf9bbc495f419df632b5938060b2e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11845068165d574aa2798c6158bf4904622cd7aff2c5675c6643ff0ba4fda74`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 8.8 MB (8802587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5feec6ebdd2d272ba4886d83efac935f56f806e73e527a868a28138c61e67718`  
		Last Modified: Mon, 18 Nov 2024 21:06:08 GMT  
		Size: 143.4 MB (143372719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfeab913ab2cc5b1eae6e120652382b1e4419e753305cbecd10ed1fd65a4bc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1a6ccef3905d7f4b64758101a5566220595da9cd94b3a8efe3c7c3d500827`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52154b45f848fae4d6dc15923fd51d332c33b0e778b1c11e06eb83e661dd7a95`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b265890db07ff12d8c1d5226fa954754fc2424e3c212fb8ec6357953893fe05f`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff950eeed9b85019e89aaffe2962b82fdbc03b54f59941891af221eb1511d3a4`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:064a3c846ada78d4c69bda131ebe8c761653440c1cc0f3585a7a48d399021fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c888f3eb66030483fa7a082a00d60e89b78ac7a1f1e67da42a74eca0169fae`

```dockerfile
```

-	Layers:
	-	`sha256:f50539b9c37f17df612e4afdb20de110705ae3090a3db1da1b402faa4f251cc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:05 GMT  
		Size: 26.5 KB (26499 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f36884dc6d24d60a9bb6c320e8a052190ae2358d8f66efc4c71ad5ffa4638d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174195698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68ae827e8dcb485e903cb0057678535df1e43de4da3302cf7efd6fb2bcb936e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86846b838547ebb3f9804d50f4fe8eb4f6bfeff8d4821e1998c250e0dfd1a11`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 8.7 MB (8662233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7371f123ab3df4a130514d8f7597c2f06a212dda18e5943a8eb98574c2d0b52`  
		Last Modified: Mon, 18 Nov 2024 20:05:57 GMT  
		Size: 138.7 MB (138692361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a627ba3ba9c0dd7675bded26bee97be800d7ae7233b65cc5e87dec6385d6d684`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eab81eafda560d04753033a7793b0fbad07c01a37f4e1fa1b6cbb5d57fbe8d`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b4918a2555f120c31a57c5c66f22600ab0bc3d121542385b9eb52b639f3796`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6c7d5229f43bb415dcabb1c0fd300ecc1dbfed18d77c6e553ba203fcc0d0`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30b9bec89bc291fd156ad60a897a8bc119acda2d3294db0909a7abb9b7aa124`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2f77217c545db83c44c23cc6abdf4f34ce68265d9e261c4af075dc598e2811bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca457bdd672219881e4c7f28900a0fb3c0f87120ecf163a2c6fbfddd3eb9cf2d`

```dockerfile
```

-	Layers:
	-	`sha256:5791af50f4fcfa896eb3c0edf644ae24c07abc17fd5982c1cbb1724b8ede7636`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 26.7 KB (26735 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.10.2-focal`

```console
$ docker pull clickhouse@sha256:aa887dfaa8d915a18ad93d25cef0334138ffeeb386353600ed90ecf07ff4eb5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10.2-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:3073efa0428c680834cf03dd2428fac3408a8a60310cd0613f51731eb25bcdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180553647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33410aa159ab43ebeaa868575df2dc69997cf9bbc495f419df632b5938060b2e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11845068165d574aa2798c6158bf4904622cd7aff2c5675c6643ff0ba4fda74`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 8.8 MB (8802587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5feec6ebdd2d272ba4886d83efac935f56f806e73e527a868a28138c61e67718`  
		Last Modified: Mon, 18 Nov 2024 21:06:08 GMT  
		Size: 143.4 MB (143372719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfeab913ab2cc5b1eae6e120652382b1e4419e753305cbecd10ed1fd65a4bc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1a6ccef3905d7f4b64758101a5566220595da9cd94b3a8efe3c7c3d500827`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52154b45f848fae4d6dc15923fd51d332c33b0e778b1c11e06eb83e661dd7a95`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b265890db07ff12d8c1d5226fa954754fc2424e3c212fb8ec6357953893fe05f`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff950eeed9b85019e89aaffe2962b82fdbc03b54f59941891af221eb1511d3a4`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.2-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:064a3c846ada78d4c69bda131ebe8c761653440c1cc0f3585a7a48d399021fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c888f3eb66030483fa7a082a00d60e89b78ac7a1f1e67da42a74eca0169fae`

```dockerfile
```

-	Layers:
	-	`sha256:f50539b9c37f17df612e4afdb20de110705ae3090a3db1da1b402faa4f251cc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:05 GMT  
		Size: 26.5 KB (26499 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10.2-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f36884dc6d24d60a9bb6c320e8a052190ae2358d8f66efc4c71ad5ffa4638d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174195698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68ae827e8dcb485e903cb0057678535df1e43de4da3302cf7efd6fb2bcb936e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86846b838547ebb3f9804d50f4fe8eb4f6bfeff8d4821e1998c250e0dfd1a11`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 8.7 MB (8662233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7371f123ab3df4a130514d8f7597c2f06a212dda18e5943a8eb98574c2d0b52`  
		Last Modified: Mon, 18 Nov 2024 20:05:57 GMT  
		Size: 138.7 MB (138692361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a627ba3ba9c0dd7675bded26bee97be800d7ae7233b65cc5e87dec6385d6d684`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eab81eafda560d04753033a7793b0fbad07c01a37f4e1fa1b6cbb5d57fbe8d`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b4918a2555f120c31a57c5c66f22600ab0bc3d121542385b9eb52b639f3796`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6c7d5229f43bb415dcabb1c0fd300ecc1dbfed18d77c6e553ba203fcc0d0`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30b9bec89bc291fd156ad60a897a8bc119acda2d3294db0909a7abb9b7aa124`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.2-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2f77217c545db83c44c23cc6abdf4f34ce68265d9e261c4af075dc598e2811bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca457bdd672219881e4c7f28900a0fb3c0f87120ecf163a2c6fbfddd3eb9cf2d`

```dockerfile
```

-	Layers:
	-	`sha256:5791af50f4fcfa896eb3c0edf644ae24c07abc17fd5982c1cbb1724b8ede7636`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 26.7 KB (26735 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.10.2.80`

```console
$ docker pull clickhouse@sha256:aa887dfaa8d915a18ad93d25cef0334138ffeeb386353600ed90ecf07ff4eb5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10.2.80` - linux; amd64

```console
$ docker pull clickhouse@sha256:3073efa0428c680834cf03dd2428fac3408a8a60310cd0613f51731eb25bcdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180553647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33410aa159ab43ebeaa868575df2dc69997cf9bbc495f419df632b5938060b2e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11845068165d574aa2798c6158bf4904622cd7aff2c5675c6643ff0ba4fda74`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 8.8 MB (8802587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5feec6ebdd2d272ba4886d83efac935f56f806e73e527a868a28138c61e67718`  
		Last Modified: Mon, 18 Nov 2024 21:06:08 GMT  
		Size: 143.4 MB (143372719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfeab913ab2cc5b1eae6e120652382b1e4419e753305cbecd10ed1fd65a4bc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1a6ccef3905d7f4b64758101a5566220595da9cd94b3a8efe3c7c3d500827`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52154b45f848fae4d6dc15923fd51d332c33b0e778b1c11e06eb83e661dd7a95`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b265890db07ff12d8c1d5226fa954754fc2424e3c212fb8ec6357953893fe05f`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff950eeed9b85019e89aaffe2962b82fdbc03b54f59941891af221eb1511d3a4`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.2.80` - unknown; unknown

```console
$ docker pull clickhouse@sha256:064a3c846ada78d4c69bda131ebe8c761653440c1cc0f3585a7a48d399021fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c888f3eb66030483fa7a082a00d60e89b78ac7a1f1e67da42a74eca0169fae`

```dockerfile
```

-	Layers:
	-	`sha256:f50539b9c37f17df612e4afdb20de110705ae3090a3db1da1b402faa4f251cc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:05 GMT  
		Size: 26.5 KB (26499 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10.2.80` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f36884dc6d24d60a9bb6c320e8a052190ae2358d8f66efc4c71ad5ffa4638d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174195698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68ae827e8dcb485e903cb0057678535df1e43de4da3302cf7efd6fb2bcb936e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86846b838547ebb3f9804d50f4fe8eb4f6bfeff8d4821e1998c250e0dfd1a11`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 8.7 MB (8662233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7371f123ab3df4a130514d8f7597c2f06a212dda18e5943a8eb98574c2d0b52`  
		Last Modified: Mon, 18 Nov 2024 20:05:57 GMT  
		Size: 138.7 MB (138692361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a627ba3ba9c0dd7675bded26bee97be800d7ae7233b65cc5e87dec6385d6d684`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eab81eafda560d04753033a7793b0fbad07c01a37f4e1fa1b6cbb5d57fbe8d`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b4918a2555f120c31a57c5c66f22600ab0bc3d121542385b9eb52b639f3796`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6c7d5229f43bb415dcabb1c0fd300ecc1dbfed18d77c6e553ba203fcc0d0`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30b9bec89bc291fd156ad60a897a8bc119acda2d3294db0909a7abb9b7aa124`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.2.80` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2f77217c545db83c44c23cc6abdf4f34ce68265d9e261c4af075dc598e2811bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca457bdd672219881e4c7f28900a0fb3c0f87120ecf163a2c6fbfddd3eb9cf2d`

```dockerfile
```

-	Layers:
	-	`sha256:5791af50f4fcfa896eb3c0edf644ae24c07abc17fd5982c1cbb1724b8ede7636`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 26.7 KB (26735 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.10.2.80-focal`

```console
$ docker pull clickhouse@sha256:aa887dfaa8d915a18ad93d25cef0334138ffeeb386353600ed90ecf07ff4eb5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.10.2.80-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:3073efa0428c680834cf03dd2428fac3408a8a60310cd0613f51731eb25bcdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180553647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33410aa159ab43ebeaa868575df2dc69997cf9bbc495f419df632b5938060b2e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11845068165d574aa2798c6158bf4904622cd7aff2c5675c6643ff0ba4fda74`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 8.8 MB (8802587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5feec6ebdd2d272ba4886d83efac935f56f806e73e527a868a28138c61e67718`  
		Last Modified: Mon, 18 Nov 2024 21:06:08 GMT  
		Size: 143.4 MB (143372719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfeab913ab2cc5b1eae6e120652382b1e4419e753305cbecd10ed1fd65a4bc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1a6ccef3905d7f4b64758101a5566220595da9cd94b3a8efe3c7c3d500827`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52154b45f848fae4d6dc15923fd51d332c33b0e778b1c11e06eb83e661dd7a95`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b265890db07ff12d8c1d5226fa954754fc2424e3c212fb8ec6357953893fe05f`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff950eeed9b85019e89aaffe2962b82fdbc03b54f59941891af221eb1511d3a4`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.2.80-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:064a3c846ada78d4c69bda131ebe8c761653440c1cc0f3585a7a48d399021fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c888f3eb66030483fa7a082a00d60e89b78ac7a1f1e67da42a74eca0169fae`

```dockerfile
```

-	Layers:
	-	`sha256:f50539b9c37f17df612e4afdb20de110705ae3090a3db1da1b402faa4f251cc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:05 GMT  
		Size: 26.5 KB (26499 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.10.2.80-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f36884dc6d24d60a9bb6c320e8a052190ae2358d8f66efc4c71ad5ffa4638d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174195698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68ae827e8dcb485e903cb0057678535df1e43de4da3302cf7efd6fb2bcb936e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86846b838547ebb3f9804d50f4fe8eb4f6bfeff8d4821e1998c250e0dfd1a11`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 8.7 MB (8662233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7371f123ab3df4a130514d8f7597c2f06a212dda18e5943a8eb98574c2d0b52`  
		Last Modified: Mon, 18 Nov 2024 20:05:57 GMT  
		Size: 138.7 MB (138692361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a627ba3ba9c0dd7675bded26bee97be800d7ae7233b65cc5e87dec6385d6d684`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eab81eafda560d04753033a7793b0fbad07c01a37f4e1fa1b6cbb5d57fbe8d`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b4918a2555f120c31a57c5c66f22600ab0bc3d121542385b9eb52b639f3796`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6c7d5229f43bb415dcabb1c0fd300ecc1dbfed18d77c6e553ba203fcc0d0`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30b9bec89bc291fd156ad60a897a8bc119acda2d3294db0909a7abb9b7aa124`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.10.2.80-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2f77217c545db83c44c23cc6abdf4f34ce68265d9e261c4af075dc598e2811bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca457bdd672219881e4c7f28900a0fb3c0f87120ecf163a2c6fbfddd3eb9cf2d`

```dockerfile
```

-	Layers:
	-	`sha256:5791af50f4fcfa896eb3c0edf644ae24c07abc17fd5982c1cbb1724b8ede7636`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 26.7 KB (26735 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3`

```console
$ docker pull clickhouse@sha256:a959b93fd697b98b666cd6785e9ae5c8399f97fd18c292cd05064b0ade1bdc10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:bdfe63c36f0cb1d46c4afeb68b09ff5b232ceb6a93342af306cc37ef2caacc40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297443951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec830c15f99be6a4bc00e3f53130204977735cff5972d4639757fa8ed7261ba`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.3.14.35
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4349295a30f5633937a1bc092bec1c82695ddfd8955b8bb5fedd667580fda1`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 8.8 MB (8802606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90e98037cdc68bd3bd57a6f7d4e87a4b7bbbfda65c98dcb410b712e36ce9abc`  
		Last Modified: Mon, 18 Nov 2024 20:06:38 GMT  
		Size: 260.3 MB (260262844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603324bec5fdd275d1b54e5b85b4683fb79b60c25859e1a1e501de4c7385eb6c`  
		Last Modified: Mon, 18 Nov 2024 20:06:30 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737142a71c6850267fbbca130d678ca0821ba40569c900cdc20ebfdd29c17e3b`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66c68ee28dcd47004997a8a48f04af830fb66cc9b6f660c3c7fe15ab924f1de`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9eb19838727458fd3b28c7b1a78d95ea5acbc31962923aff0a261d43e9f51ad`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be74f34f41c7e88691ba050be7c2a78401668d41560a8b11f86b1f45c5a411`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c039285153d9794aa2e78d3ea7c34a1c83c03a57ba0f07f7945245a27e8e2e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0127b13de2f69cada0646b70b1c38dbfcad4dc055b65343e605aa510d2d13a`

```dockerfile
```

-	Layers:
	-	`sha256:bf6ed6310c4f352c18babfa257b66edcd2e8500ee6501271a1d1bbe15b4639c8`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:834ec1b749893206dc7a6ba5aa9ac85446c8f58171d1e934311bea1801e6add0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (285993226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd94852f8c365151aa1775115b9a6ac2ca7701c67e8e174a2d1353737d2dbd79`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.3.14.35
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb8cd16abd8b1cc2089409c1804a81daf37d8c0b1e790771c8f3c627b4817d0`  
		Last Modified: Mon, 18 Nov 2024 20:09:21 GMT  
		Size: 250.5 MB (250489631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d2b9ae7dc28a86d74efaf057fdf5fa3d7ec13f7e846f7f1adaeb4e6cab2db3`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061c50d579970f38c199ee0d16d897797fe3baddf9e9c1515036ccb8d4741319`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf56093c6ea32d71954bf6215e876e1dfd80d61536cc17c8cb1dd9042b5beacd`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2187ca256d0261e951dcaf4882c42e9af92da1da71954bc47fa1087978f2b8`  
		Last Modified: Mon, 18 Nov 2024 20:09:17 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9ba020a18f6f926b8e64647cbac78712f017c66ab7459780412ba1b3a4d820`  
		Last Modified: Mon, 18 Nov 2024 20:09:17 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f27a92c93086fbd80abd972b59f9a45a8bd3ad61709630985199f09f20fe8ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e92e3ca5118335d71cfd040286d52ed0118bd10ec5f4011f1e63d54e20222ca`

```dockerfile
```

-	Layers:
	-	`sha256:8dd23a374d3a37db5702626e0c93c5216b79a2e7e9755d31c0c8ec3ba4fff5df`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3-focal`

```console
$ docker pull clickhouse@sha256:a959b93fd697b98b666cd6785e9ae5c8399f97fd18c292cd05064b0ade1bdc10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:bdfe63c36f0cb1d46c4afeb68b09ff5b232ceb6a93342af306cc37ef2caacc40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297443951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec830c15f99be6a4bc00e3f53130204977735cff5972d4639757fa8ed7261ba`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.3.14.35
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4349295a30f5633937a1bc092bec1c82695ddfd8955b8bb5fedd667580fda1`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 8.8 MB (8802606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90e98037cdc68bd3bd57a6f7d4e87a4b7bbbfda65c98dcb410b712e36ce9abc`  
		Last Modified: Mon, 18 Nov 2024 20:06:38 GMT  
		Size: 260.3 MB (260262844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603324bec5fdd275d1b54e5b85b4683fb79b60c25859e1a1e501de4c7385eb6c`  
		Last Modified: Mon, 18 Nov 2024 20:06:30 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737142a71c6850267fbbca130d678ca0821ba40569c900cdc20ebfdd29c17e3b`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66c68ee28dcd47004997a8a48f04af830fb66cc9b6f660c3c7fe15ab924f1de`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9eb19838727458fd3b28c7b1a78d95ea5acbc31962923aff0a261d43e9f51ad`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be74f34f41c7e88691ba050be7c2a78401668d41560a8b11f86b1f45c5a411`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c039285153d9794aa2e78d3ea7c34a1c83c03a57ba0f07f7945245a27e8e2e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0127b13de2f69cada0646b70b1c38dbfcad4dc055b65343e605aa510d2d13a`

```dockerfile
```

-	Layers:
	-	`sha256:bf6ed6310c4f352c18babfa257b66edcd2e8500ee6501271a1d1bbe15b4639c8`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:834ec1b749893206dc7a6ba5aa9ac85446c8f58171d1e934311bea1801e6add0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (285993226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd94852f8c365151aa1775115b9a6ac2ca7701c67e8e174a2d1353737d2dbd79`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.3.14.35
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb8cd16abd8b1cc2089409c1804a81daf37d8c0b1e790771c8f3c627b4817d0`  
		Last Modified: Mon, 18 Nov 2024 20:09:21 GMT  
		Size: 250.5 MB (250489631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d2b9ae7dc28a86d74efaf057fdf5fa3d7ec13f7e846f7f1adaeb4e6cab2db3`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061c50d579970f38c199ee0d16d897797fe3baddf9e9c1515036ccb8d4741319`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf56093c6ea32d71954bf6215e876e1dfd80d61536cc17c8cb1dd9042b5beacd`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2187ca256d0261e951dcaf4882c42e9af92da1da71954bc47fa1087978f2b8`  
		Last Modified: Mon, 18 Nov 2024 20:09:17 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9ba020a18f6f926b8e64647cbac78712f017c66ab7459780412ba1b3a4d820`  
		Last Modified: Mon, 18 Nov 2024 20:09:17 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f27a92c93086fbd80abd972b59f9a45a8bd3ad61709630985199f09f20fe8ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e92e3ca5118335d71cfd040286d52ed0118bd10ec5f4011f1e63d54e20222ca`

```dockerfile
```

-	Layers:
	-	`sha256:8dd23a374d3a37db5702626e0c93c5216b79a2e7e9755d31c0c8ec3ba4fff5df`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3.14`

```console
$ docker pull clickhouse@sha256:a959b93fd697b98b666cd6785e9ae5c8399f97fd18c292cd05064b0ade1bdc10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3.14` - linux; amd64

```console
$ docker pull clickhouse@sha256:bdfe63c36f0cb1d46c4afeb68b09ff5b232ceb6a93342af306cc37ef2caacc40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297443951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec830c15f99be6a4bc00e3f53130204977735cff5972d4639757fa8ed7261ba`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.3.14.35
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4349295a30f5633937a1bc092bec1c82695ddfd8955b8bb5fedd667580fda1`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 8.8 MB (8802606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90e98037cdc68bd3bd57a6f7d4e87a4b7bbbfda65c98dcb410b712e36ce9abc`  
		Last Modified: Mon, 18 Nov 2024 20:06:38 GMT  
		Size: 260.3 MB (260262844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603324bec5fdd275d1b54e5b85b4683fb79b60c25859e1a1e501de4c7385eb6c`  
		Last Modified: Mon, 18 Nov 2024 20:06:30 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737142a71c6850267fbbca130d678ca0821ba40569c900cdc20ebfdd29c17e3b`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66c68ee28dcd47004997a8a48f04af830fb66cc9b6f660c3c7fe15ab924f1de`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9eb19838727458fd3b28c7b1a78d95ea5acbc31962923aff0a261d43e9f51ad`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be74f34f41c7e88691ba050be7c2a78401668d41560a8b11f86b1f45c5a411`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c039285153d9794aa2e78d3ea7c34a1c83c03a57ba0f07f7945245a27e8e2e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0127b13de2f69cada0646b70b1c38dbfcad4dc055b65343e605aa510d2d13a`

```dockerfile
```

-	Layers:
	-	`sha256:bf6ed6310c4f352c18babfa257b66edcd2e8500ee6501271a1d1bbe15b4639c8`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3.14` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:834ec1b749893206dc7a6ba5aa9ac85446c8f58171d1e934311bea1801e6add0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (285993226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd94852f8c365151aa1775115b9a6ac2ca7701c67e8e174a2d1353737d2dbd79`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.3.14.35
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb8cd16abd8b1cc2089409c1804a81daf37d8c0b1e790771c8f3c627b4817d0`  
		Last Modified: Mon, 18 Nov 2024 20:09:21 GMT  
		Size: 250.5 MB (250489631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d2b9ae7dc28a86d74efaf057fdf5fa3d7ec13f7e846f7f1adaeb4e6cab2db3`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061c50d579970f38c199ee0d16d897797fe3baddf9e9c1515036ccb8d4741319`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf56093c6ea32d71954bf6215e876e1dfd80d61536cc17c8cb1dd9042b5beacd`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2187ca256d0261e951dcaf4882c42e9af92da1da71954bc47fa1087978f2b8`  
		Last Modified: Mon, 18 Nov 2024 20:09:17 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9ba020a18f6f926b8e64647cbac78712f017c66ab7459780412ba1b3a4d820`  
		Last Modified: Mon, 18 Nov 2024 20:09:17 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f27a92c93086fbd80abd972b59f9a45a8bd3ad61709630985199f09f20fe8ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e92e3ca5118335d71cfd040286d52ed0118bd10ec5f4011f1e63d54e20222ca`

```dockerfile
```

-	Layers:
	-	`sha256:8dd23a374d3a37db5702626e0c93c5216b79a2e7e9755d31c0c8ec3ba4fff5df`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3.14-focal`

```console
$ docker pull clickhouse@sha256:a959b93fd697b98b666cd6785e9ae5c8399f97fd18c292cd05064b0ade1bdc10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3.14-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:bdfe63c36f0cb1d46c4afeb68b09ff5b232ceb6a93342af306cc37ef2caacc40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297443951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec830c15f99be6a4bc00e3f53130204977735cff5972d4639757fa8ed7261ba`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.3.14.35
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4349295a30f5633937a1bc092bec1c82695ddfd8955b8bb5fedd667580fda1`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 8.8 MB (8802606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90e98037cdc68bd3bd57a6f7d4e87a4b7bbbfda65c98dcb410b712e36ce9abc`  
		Last Modified: Mon, 18 Nov 2024 20:06:38 GMT  
		Size: 260.3 MB (260262844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603324bec5fdd275d1b54e5b85b4683fb79b60c25859e1a1e501de4c7385eb6c`  
		Last Modified: Mon, 18 Nov 2024 20:06:30 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737142a71c6850267fbbca130d678ca0821ba40569c900cdc20ebfdd29c17e3b`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66c68ee28dcd47004997a8a48f04af830fb66cc9b6f660c3c7fe15ab924f1de`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9eb19838727458fd3b28c7b1a78d95ea5acbc31962923aff0a261d43e9f51ad`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be74f34f41c7e88691ba050be7c2a78401668d41560a8b11f86b1f45c5a411`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.14-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c039285153d9794aa2e78d3ea7c34a1c83c03a57ba0f07f7945245a27e8e2e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0127b13de2f69cada0646b70b1c38dbfcad4dc055b65343e605aa510d2d13a`

```dockerfile
```

-	Layers:
	-	`sha256:bf6ed6310c4f352c18babfa257b66edcd2e8500ee6501271a1d1bbe15b4639c8`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3.14-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:834ec1b749893206dc7a6ba5aa9ac85446c8f58171d1e934311bea1801e6add0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (285993226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd94852f8c365151aa1775115b9a6ac2ca7701c67e8e174a2d1353737d2dbd79`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.3.14.35
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb8cd16abd8b1cc2089409c1804a81daf37d8c0b1e790771c8f3c627b4817d0`  
		Last Modified: Mon, 18 Nov 2024 20:09:21 GMT  
		Size: 250.5 MB (250489631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d2b9ae7dc28a86d74efaf057fdf5fa3d7ec13f7e846f7f1adaeb4e6cab2db3`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061c50d579970f38c199ee0d16d897797fe3baddf9e9c1515036ccb8d4741319`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf56093c6ea32d71954bf6215e876e1dfd80d61536cc17c8cb1dd9042b5beacd`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2187ca256d0261e951dcaf4882c42e9af92da1da71954bc47fa1087978f2b8`  
		Last Modified: Mon, 18 Nov 2024 20:09:17 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9ba020a18f6f926b8e64647cbac78712f017c66ab7459780412ba1b3a4d820`  
		Last Modified: Mon, 18 Nov 2024 20:09:17 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.14-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f27a92c93086fbd80abd972b59f9a45a8bd3ad61709630985199f09f20fe8ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e92e3ca5118335d71cfd040286d52ed0118bd10ec5f4011f1e63d54e20222ca`

```dockerfile
```

-	Layers:
	-	`sha256:8dd23a374d3a37db5702626e0c93c5216b79a2e7e9755d31c0c8ec3ba4fff5df`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3.14.35`

```console
$ docker pull clickhouse@sha256:a959b93fd697b98b666cd6785e9ae5c8399f97fd18c292cd05064b0ade1bdc10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3.14.35` - linux; amd64

```console
$ docker pull clickhouse@sha256:bdfe63c36f0cb1d46c4afeb68b09ff5b232ceb6a93342af306cc37ef2caacc40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297443951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec830c15f99be6a4bc00e3f53130204977735cff5972d4639757fa8ed7261ba`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.3.14.35
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4349295a30f5633937a1bc092bec1c82695ddfd8955b8bb5fedd667580fda1`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 8.8 MB (8802606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90e98037cdc68bd3bd57a6f7d4e87a4b7bbbfda65c98dcb410b712e36ce9abc`  
		Last Modified: Mon, 18 Nov 2024 20:06:38 GMT  
		Size: 260.3 MB (260262844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603324bec5fdd275d1b54e5b85b4683fb79b60c25859e1a1e501de4c7385eb6c`  
		Last Modified: Mon, 18 Nov 2024 20:06:30 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737142a71c6850267fbbca130d678ca0821ba40569c900cdc20ebfdd29c17e3b`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66c68ee28dcd47004997a8a48f04af830fb66cc9b6f660c3c7fe15ab924f1de`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9eb19838727458fd3b28c7b1a78d95ea5acbc31962923aff0a261d43e9f51ad`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be74f34f41c7e88691ba050be7c2a78401668d41560a8b11f86b1f45c5a411`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.14.35` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c039285153d9794aa2e78d3ea7c34a1c83c03a57ba0f07f7945245a27e8e2e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0127b13de2f69cada0646b70b1c38dbfcad4dc055b65343e605aa510d2d13a`

```dockerfile
```

-	Layers:
	-	`sha256:bf6ed6310c4f352c18babfa257b66edcd2e8500ee6501271a1d1bbe15b4639c8`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3.14.35` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:834ec1b749893206dc7a6ba5aa9ac85446c8f58171d1e934311bea1801e6add0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (285993226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd94852f8c365151aa1775115b9a6ac2ca7701c67e8e174a2d1353737d2dbd79`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.3.14.35
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb8cd16abd8b1cc2089409c1804a81daf37d8c0b1e790771c8f3c627b4817d0`  
		Last Modified: Mon, 18 Nov 2024 20:09:21 GMT  
		Size: 250.5 MB (250489631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d2b9ae7dc28a86d74efaf057fdf5fa3d7ec13f7e846f7f1adaeb4e6cab2db3`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061c50d579970f38c199ee0d16d897797fe3baddf9e9c1515036ccb8d4741319`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf56093c6ea32d71954bf6215e876e1dfd80d61536cc17c8cb1dd9042b5beacd`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2187ca256d0261e951dcaf4882c42e9af92da1da71954bc47fa1087978f2b8`  
		Last Modified: Mon, 18 Nov 2024 20:09:17 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9ba020a18f6f926b8e64647cbac78712f017c66ab7459780412ba1b3a4d820`  
		Last Modified: Mon, 18 Nov 2024 20:09:17 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.14.35` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f27a92c93086fbd80abd972b59f9a45a8bd3ad61709630985199f09f20fe8ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e92e3ca5118335d71cfd040286d52ed0118bd10ec5f4011f1e63d54e20222ca`

```dockerfile
```

-	Layers:
	-	`sha256:8dd23a374d3a37db5702626e0c93c5216b79a2e7e9755d31c0c8ec3ba4fff5df`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3.14.35-focal`

```console
$ docker pull clickhouse@sha256:a959b93fd697b98b666cd6785e9ae5c8399f97fd18c292cd05064b0ade1bdc10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3.14.35-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:bdfe63c36f0cb1d46c4afeb68b09ff5b232ceb6a93342af306cc37ef2caacc40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.4 MB (297443951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec830c15f99be6a4bc00e3f53130204977735cff5972d4639757fa8ed7261ba`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.3.14.35
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4349295a30f5633937a1bc092bec1c82695ddfd8955b8bb5fedd667580fda1`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 8.8 MB (8802606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90e98037cdc68bd3bd57a6f7d4e87a4b7bbbfda65c98dcb410b712e36ce9abc`  
		Last Modified: Mon, 18 Nov 2024 20:06:38 GMT  
		Size: 260.3 MB (260262844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603324bec5fdd275d1b54e5b85b4683fb79b60c25859e1a1e501de4c7385eb6c`  
		Last Modified: Mon, 18 Nov 2024 20:06:30 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:737142a71c6850267fbbca130d678ca0821ba40569c900cdc20ebfdd29c17e3b`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66c68ee28dcd47004997a8a48f04af830fb66cc9b6f660c3c7fe15ab924f1de`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9eb19838727458fd3b28c7b1a78d95ea5acbc31962923aff0a261d43e9f51ad`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79be74f34f41c7e88691ba050be7c2a78401668d41560a8b11f86b1f45c5a411`  
		Last Modified: Mon, 18 Nov 2024 20:06:32 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.14.35-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c039285153d9794aa2e78d3ea7c34a1c83c03a57ba0f07f7945245a27e8e2e4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c0127b13de2f69cada0646b70b1c38dbfcad4dc055b65343e605aa510d2d13a`

```dockerfile
```

-	Layers:
	-	`sha256:bf6ed6310c4f352c18babfa257b66edcd2e8500ee6501271a1d1bbe15b4639c8`  
		Last Modified: Mon, 18 Nov 2024 20:06:31 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3.14.35-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:834ec1b749893206dc7a6ba5aa9ac85446c8f58171d1e934311bea1801e6add0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (285993226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd94852f8c365151aa1775115b9a6ac2ca7701c67e8e174a2d1353737d2dbd79`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.3.14.35
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.14.35 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb8cd16abd8b1cc2089409c1804a81daf37d8c0b1e790771c8f3c627b4817d0`  
		Last Modified: Mon, 18 Nov 2024 20:09:21 GMT  
		Size: 250.5 MB (250489631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d2b9ae7dc28a86d74efaf057fdf5fa3d7ec13f7e846f7f1adaeb4e6cab2db3`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061c50d579970f38c199ee0d16d897797fe3baddf9e9c1515036ccb8d4741319`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf56093c6ea32d71954bf6215e876e1dfd80d61536cc17c8cb1dd9042b5beacd`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2187ca256d0261e951dcaf4882c42e9af92da1da71954bc47fa1087978f2b8`  
		Last Modified: Mon, 18 Nov 2024 20:09:17 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9ba020a18f6f926b8e64647cbac78712f017c66ab7459780412ba1b3a4d820`  
		Last Modified: Mon, 18 Nov 2024 20:09:17 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.14.35-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f27a92c93086fbd80abd972b59f9a45a8bd3ad61709630985199f09f20fe8ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e92e3ca5118335d71cfd040286d52ed0118bd10ec5f4011f1e63d54e20222ca`

```dockerfile
```

-	Layers:
	-	`sha256:8dd23a374d3a37db5702626e0c93c5216b79a2e7e9755d31c0c8ec3ba4fff5df`  
		Last Modified: Mon, 18 Nov 2024 20:09:16 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8`

```console
$ docker pull clickhouse@sha256:698363cd1136335696abf40a67f5546127dfdf5fe6ad2ca88fe60cd3ae7bdf2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:47cef6f2fbb1fb511670b86d9f4783ec9cfa3c072a40a59282a980cf38b6aa0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178812657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1387e7bdaf532e3d74a9b01fa5552a8d49c42257102256a8dd84a75943af949`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.8.7.41
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e67b6741df06aa8eb8d8fcb7c95e8cc10d7e92f9a3cb3181ae40f97bba8a4f2`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 8.8 MB (8802629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ba309f2e22dfad8a2676a95340a87935e01c40b10278c763606e6a38f8ae3f`  
		Last Modified: Mon, 18 Nov 2024 20:06:18 GMT  
		Size: 141.6 MB (141631685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48aef40100afaae89d86927eec76e4e414602914f5b5e776ca029cf0907bf538`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f960df628b7b0375c45e65adc733c6779004504ec3ef541e913e73cc895b07`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec64844717ad2ae00fe14780a6cc2f44eb95615036366e291852afabf464492f`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4d29135e7f625c0a17e60870a4120bf338bf85646c29a1281f4c26ef11796b`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cfd9c027f10cb6506f9e0695b3c98044eab94a91ebe1b125e9b3f95f4e54c9`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b101c6fca19411ff534750286eaf83eecb9bb127846c5077bbf85882c93b6d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c985ecdf74273a1483a770cc4add37729a95eaf93cd09b69b9f5433d9ab26f`

```dockerfile
```

-	Layers:
	-	`sha256:1c0ef4be653a14e13ddd9f068f8b7e943b538376f38f98b9a9c90b9ee1ceb60a`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d00c2769c76341b3cf1a4dc8e9f5a5b1ee9b893de45609ae576556ebab7882ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172188479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c08925b341a204c06bd134b161f7126a241b3031a0a0d2fc3ab207d2c58bef0`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.8.7.41
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03120df1d949cda902248b711ed24360e5f33e29ab93d0fcc3ad4f49f4c94663`  
		Last Modified: Mon, 18 Nov 2024 20:08:02 GMT  
		Size: 136.7 MB (136685053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05d90f88b9b12fdedfe65bc756bff7ebf2bcd74475f8002682c5912815c5ea0`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73efb287cd7a74820405dc5e4d603782ddab7a5d7675d8257e9b89562076788`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021af34596bc467a509c70e886da66789b1d1cbb835980cfb8d2e74962bd504a`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf8f562b370201341e7dfa04698b7cd723787c43682db929bc33aa4618dc511`  
		Last Modified: Mon, 18 Nov 2024 20:07:59 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127256b32943afe8f2b034ae5168c0037568ed72ab28fecb0336a496b56352bf`  
		Last Modified: Mon, 18 Nov 2024 20:07:59 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dee6a322dd46dd22fbcda8db3070427a0d203231dfafa78e92767b46a3a20ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4ccb8f250378ac75e417fc9c9f2ec26e248ad4d82ded701075407f0e6c2dab`

```dockerfile
```

-	Layers:
	-	`sha256:df1379770a3a3a41c884e93ea770d057adc7fb09481238e53c57279c24b95360`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8-focal`

```console
$ docker pull clickhouse@sha256:698363cd1136335696abf40a67f5546127dfdf5fe6ad2ca88fe60cd3ae7bdf2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:47cef6f2fbb1fb511670b86d9f4783ec9cfa3c072a40a59282a980cf38b6aa0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178812657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1387e7bdaf532e3d74a9b01fa5552a8d49c42257102256a8dd84a75943af949`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.8.7.41
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e67b6741df06aa8eb8d8fcb7c95e8cc10d7e92f9a3cb3181ae40f97bba8a4f2`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 8.8 MB (8802629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ba309f2e22dfad8a2676a95340a87935e01c40b10278c763606e6a38f8ae3f`  
		Last Modified: Mon, 18 Nov 2024 20:06:18 GMT  
		Size: 141.6 MB (141631685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48aef40100afaae89d86927eec76e4e414602914f5b5e776ca029cf0907bf538`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f960df628b7b0375c45e65adc733c6779004504ec3ef541e913e73cc895b07`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec64844717ad2ae00fe14780a6cc2f44eb95615036366e291852afabf464492f`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4d29135e7f625c0a17e60870a4120bf338bf85646c29a1281f4c26ef11796b`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cfd9c027f10cb6506f9e0695b3c98044eab94a91ebe1b125e9b3f95f4e54c9`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b101c6fca19411ff534750286eaf83eecb9bb127846c5077bbf85882c93b6d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c985ecdf74273a1483a770cc4add37729a95eaf93cd09b69b9f5433d9ab26f`

```dockerfile
```

-	Layers:
	-	`sha256:1c0ef4be653a14e13ddd9f068f8b7e943b538376f38f98b9a9c90b9ee1ceb60a`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d00c2769c76341b3cf1a4dc8e9f5a5b1ee9b893de45609ae576556ebab7882ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172188479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c08925b341a204c06bd134b161f7126a241b3031a0a0d2fc3ab207d2c58bef0`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.8.7.41
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03120df1d949cda902248b711ed24360e5f33e29ab93d0fcc3ad4f49f4c94663`  
		Last Modified: Mon, 18 Nov 2024 20:08:02 GMT  
		Size: 136.7 MB (136685053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05d90f88b9b12fdedfe65bc756bff7ebf2bcd74475f8002682c5912815c5ea0`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73efb287cd7a74820405dc5e4d603782ddab7a5d7675d8257e9b89562076788`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021af34596bc467a509c70e886da66789b1d1cbb835980cfb8d2e74962bd504a`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf8f562b370201341e7dfa04698b7cd723787c43682db929bc33aa4618dc511`  
		Last Modified: Mon, 18 Nov 2024 20:07:59 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127256b32943afe8f2b034ae5168c0037568ed72ab28fecb0336a496b56352bf`  
		Last Modified: Mon, 18 Nov 2024 20:07:59 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dee6a322dd46dd22fbcda8db3070427a0d203231dfafa78e92767b46a3a20ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4ccb8f250378ac75e417fc9c9f2ec26e248ad4d82ded701075407f0e6c2dab`

```dockerfile
```

-	Layers:
	-	`sha256:df1379770a3a3a41c884e93ea770d057adc7fb09481238e53c57279c24b95360`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.7`

```console
$ docker pull clickhouse@sha256:698363cd1136335696abf40a67f5546127dfdf5fe6ad2ca88fe60cd3ae7bdf2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:47cef6f2fbb1fb511670b86d9f4783ec9cfa3c072a40a59282a980cf38b6aa0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178812657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1387e7bdaf532e3d74a9b01fa5552a8d49c42257102256a8dd84a75943af949`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.8.7.41
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e67b6741df06aa8eb8d8fcb7c95e8cc10d7e92f9a3cb3181ae40f97bba8a4f2`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 8.8 MB (8802629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ba309f2e22dfad8a2676a95340a87935e01c40b10278c763606e6a38f8ae3f`  
		Last Modified: Mon, 18 Nov 2024 20:06:18 GMT  
		Size: 141.6 MB (141631685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48aef40100afaae89d86927eec76e4e414602914f5b5e776ca029cf0907bf538`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f960df628b7b0375c45e65adc733c6779004504ec3ef541e913e73cc895b07`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec64844717ad2ae00fe14780a6cc2f44eb95615036366e291852afabf464492f`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4d29135e7f625c0a17e60870a4120bf338bf85646c29a1281f4c26ef11796b`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cfd9c027f10cb6506f9e0695b3c98044eab94a91ebe1b125e9b3f95f4e54c9`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b101c6fca19411ff534750286eaf83eecb9bb127846c5077bbf85882c93b6d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c985ecdf74273a1483a770cc4add37729a95eaf93cd09b69b9f5433d9ab26f`

```dockerfile
```

-	Layers:
	-	`sha256:1c0ef4be653a14e13ddd9f068f8b7e943b538376f38f98b9a9c90b9ee1ceb60a`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d00c2769c76341b3cf1a4dc8e9f5a5b1ee9b893de45609ae576556ebab7882ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172188479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c08925b341a204c06bd134b161f7126a241b3031a0a0d2fc3ab207d2c58bef0`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.8.7.41
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03120df1d949cda902248b711ed24360e5f33e29ab93d0fcc3ad4f49f4c94663`  
		Last Modified: Mon, 18 Nov 2024 20:08:02 GMT  
		Size: 136.7 MB (136685053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05d90f88b9b12fdedfe65bc756bff7ebf2bcd74475f8002682c5912815c5ea0`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73efb287cd7a74820405dc5e4d603782ddab7a5d7675d8257e9b89562076788`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021af34596bc467a509c70e886da66789b1d1cbb835980cfb8d2e74962bd504a`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf8f562b370201341e7dfa04698b7cd723787c43682db929bc33aa4618dc511`  
		Last Modified: Mon, 18 Nov 2024 20:07:59 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127256b32943afe8f2b034ae5168c0037568ed72ab28fecb0336a496b56352bf`  
		Last Modified: Mon, 18 Nov 2024 20:07:59 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dee6a322dd46dd22fbcda8db3070427a0d203231dfafa78e92767b46a3a20ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4ccb8f250378ac75e417fc9c9f2ec26e248ad4d82ded701075407f0e6c2dab`

```dockerfile
```

-	Layers:
	-	`sha256:df1379770a3a3a41c884e93ea770d057adc7fb09481238e53c57279c24b95360`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.7-focal`

```console
$ docker pull clickhouse@sha256:698363cd1136335696abf40a67f5546127dfdf5fe6ad2ca88fe60cd3ae7bdf2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.7-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:47cef6f2fbb1fb511670b86d9f4783ec9cfa3c072a40a59282a980cf38b6aa0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178812657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1387e7bdaf532e3d74a9b01fa5552a8d49c42257102256a8dd84a75943af949`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.8.7.41
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e67b6741df06aa8eb8d8fcb7c95e8cc10d7e92f9a3cb3181ae40f97bba8a4f2`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 8.8 MB (8802629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ba309f2e22dfad8a2676a95340a87935e01c40b10278c763606e6a38f8ae3f`  
		Last Modified: Mon, 18 Nov 2024 20:06:18 GMT  
		Size: 141.6 MB (141631685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48aef40100afaae89d86927eec76e4e414602914f5b5e776ca029cf0907bf538`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f960df628b7b0375c45e65adc733c6779004504ec3ef541e913e73cc895b07`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec64844717ad2ae00fe14780a6cc2f44eb95615036366e291852afabf464492f`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4d29135e7f625c0a17e60870a4120bf338bf85646c29a1281f4c26ef11796b`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cfd9c027f10cb6506f9e0695b3c98044eab94a91ebe1b125e9b3f95f4e54c9`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.7-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b101c6fca19411ff534750286eaf83eecb9bb127846c5077bbf85882c93b6d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c985ecdf74273a1483a770cc4add37729a95eaf93cd09b69b9f5433d9ab26f`

```dockerfile
```

-	Layers:
	-	`sha256:1c0ef4be653a14e13ddd9f068f8b7e943b538376f38f98b9a9c90b9ee1ceb60a`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.7-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d00c2769c76341b3cf1a4dc8e9f5a5b1ee9b893de45609ae576556ebab7882ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172188479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c08925b341a204c06bd134b161f7126a241b3031a0a0d2fc3ab207d2c58bef0`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.8.7.41
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03120df1d949cda902248b711ed24360e5f33e29ab93d0fcc3ad4f49f4c94663`  
		Last Modified: Mon, 18 Nov 2024 20:08:02 GMT  
		Size: 136.7 MB (136685053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05d90f88b9b12fdedfe65bc756bff7ebf2bcd74475f8002682c5912815c5ea0`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73efb287cd7a74820405dc5e4d603782ddab7a5d7675d8257e9b89562076788`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021af34596bc467a509c70e886da66789b1d1cbb835980cfb8d2e74962bd504a`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf8f562b370201341e7dfa04698b7cd723787c43682db929bc33aa4618dc511`  
		Last Modified: Mon, 18 Nov 2024 20:07:59 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127256b32943afe8f2b034ae5168c0037568ed72ab28fecb0336a496b56352bf`  
		Last Modified: Mon, 18 Nov 2024 20:07:59 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.7-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dee6a322dd46dd22fbcda8db3070427a0d203231dfafa78e92767b46a3a20ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4ccb8f250378ac75e417fc9c9f2ec26e248ad4d82ded701075407f0e6c2dab`

```dockerfile
```

-	Layers:
	-	`sha256:df1379770a3a3a41c884e93ea770d057adc7fb09481238e53c57279c24b95360`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.7.41`

```console
$ docker pull clickhouse@sha256:698363cd1136335696abf40a67f5546127dfdf5fe6ad2ca88fe60cd3ae7bdf2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.7.41` - linux; amd64

```console
$ docker pull clickhouse@sha256:47cef6f2fbb1fb511670b86d9f4783ec9cfa3c072a40a59282a980cf38b6aa0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178812657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1387e7bdaf532e3d74a9b01fa5552a8d49c42257102256a8dd84a75943af949`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.8.7.41
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e67b6741df06aa8eb8d8fcb7c95e8cc10d7e92f9a3cb3181ae40f97bba8a4f2`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 8.8 MB (8802629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ba309f2e22dfad8a2676a95340a87935e01c40b10278c763606e6a38f8ae3f`  
		Last Modified: Mon, 18 Nov 2024 20:06:18 GMT  
		Size: 141.6 MB (141631685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48aef40100afaae89d86927eec76e4e414602914f5b5e776ca029cf0907bf538`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f960df628b7b0375c45e65adc733c6779004504ec3ef541e913e73cc895b07`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec64844717ad2ae00fe14780a6cc2f44eb95615036366e291852afabf464492f`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4d29135e7f625c0a17e60870a4120bf338bf85646c29a1281f4c26ef11796b`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cfd9c027f10cb6506f9e0695b3c98044eab94a91ebe1b125e9b3f95f4e54c9`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.7.41` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b101c6fca19411ff534750286eaf83eecb9bb127846c5077bbf85882c93b6d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c985ecdf74273a1483a770cc4add37729a95eaf93cd09b69b9f5433d9ab26f`

```dockerfile
```

-	Layers:
	-	`sha256:1c0ef4be653a14e13ddd9f068f8b7e943b538376f38f98b9a9c90b9ee1ceb60a`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.7.41` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d00c2769c76341b3cf1a4dc8e9f5a5b1ee9b893de45609ae576556ebab7882ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172188479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c08925b341a204c06bd134b161f7126a241b3031a0a0d2fc3ab207d2c58bef0`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.8.7.41
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03120df1d949cda902248b711ed24360e5f33e29ab93d0fcc3ad4f49f4c94663`  
		Last Modified: Mon, 18 Nov 2024 20:08:02 GMT  
		Size: 136.7 MB (136685053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05d90f88b9b12fdedfe65bc756bff7ebf2bcd74475f8002682c5912815c5ea0`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73efb287cd7a74820405dc5e4d603782ddab7a5d7675d8257e9b89562076788`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021af34596bc467a509c70e886da66789b1d1cbb835980cfb8d2e74962bd504a`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf8f562b370201341e7dfa04698b7cd723787c43682db929bc33aa4618dc511`  
		Last Modified: Mon, 18 Nov 2024 20:07:59 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127256b32943afe8f2b034ae5168c0037568ed72ab28fecb0336a496b56352bf`  
		Last Modified: Mon, 18 Nov 2024 20:07:59 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.7.41` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dee6a322dd46dd22fbcda8db3070427a0d203231dfafa78e92767b46a3a20ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4ccb8f250378ac75e417fc9c9f2ec26e248ad4d82ded701075407f0e6c2dab`

```dockerfile
```

-	Layers:
	-	`sha256:df1379770a3a3a41c884e93ea770d057adc7fb09481238e53c57279c24b95360`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.7.41-focal`

```console
$ docker pull clickhouse@sha256:698363cd1136335696abf40a67f5546127dfdf5fe6ad2ca88fe60cd3ae7bdf2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.7.41-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:47cef6f2fbb1fb511670b86d9f4783ec9cfa3c072a40a59282a980cf38b6aa0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178812657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1387e7bdaf532e3d74a9b01fa5552a8d49c42257102256a8dd84a75943af949`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.8.7.41
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e67b6741df06aa8eb8d8fcb7c95e8cc10d7e92f9a3cb3181ae40f97bba8a4f2`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 8.8 MB (8802629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ba309f2e22dfad8a2676a95340a87935e01c40b10278c763606e6a38f8ae3f`  
		Last Modified: Mon, 18 Nov 2024 20:06:18 GMT  
		Size: 141.6 MB (141631685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48aef40100afaae89d86927eec76e4e414602914f5b5e776ca029cf0907bf538`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f960df628b7b0375c45e65adc733c6779004504ec3ef541e913e73cc895b07`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec64844717ad2ae00fe14780a6cc2f44eb95615036366e291852afabf464492f`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4d29135e7f625c0a17e60870a4120bf338bf85646c29a1281f4c26ef11796b`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cfd9c027f10cb6506f9e0695b3c98044eab94a91ebe1b125e9b3f95f4e54c9`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.7.41-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b101c6fca19411ff534750286eaf83eecb9bb127846c5077bbf85882c93b6d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c985ecdf74273a1483a770cc4add37729a95eaf93cd09b69b9f5433d9ab26f`

```dockerfile
```

-	Layers:
	-	`sha256:1c0ef4be653a14e13ddd9f068f8b7e943b538376f38f98b9a9c90b9ee1ceb60a`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.7.41-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d00c2769c76341b3cf1a4dc8e9f5a5b1ee9b893de45609ae576556ebab7882ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172188479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c08925b341a204c06bd134b161f7126a241b3031a0a0d2fc3ab207d2c58bef0`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.8.7.41
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03120df1d949cda902248b711ed24360e5f33e29ab93d0fcc3ad4f49f4c94663`  
		Last Modified: Mon, 18 Nov 2024 20:08:02 GMT  
		Size: 136.7 MB (136685053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05d90f88b9b12fdedfe65bc756bff7ebf2bcd74475f8002682c5912815c5ea0`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73efb287cd7a74820405dc5e4d603782ddab7a5d7675d8257e9b89562076788`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021af34596bc467a509c70e886da66789b1d1cbb835980cfb8d2e74962bd504a`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf8f562b370201341e7dfa04698b7cd723787c43682db929bc33aa4618dc511`  
		Last Modified: Mon, 18 Nov 2024 20:07:59 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127256b32943afe8f2b034ae5168c0037568ed72ab28fecb0336a496b56352bf`  
		Last Modified: Mon, 18 Nov 2024 20:07:59 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.7.41-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dee6a322dd46dd22fbcda8db3070427a0d203231dfafa78e92767b46a3a20ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4ccb8f250378ac75e417fc9c9f2ec26e248ad4d82ded701075407f0e6c2dab`

```dockerfile
```

-	Layers:
	-	`sha256:df1379770a3a3a41c884e93ea770d057adc7fb09481238e53c57279c24b95360`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.9`

```console
$ docker pull clickhouse@sha256:95917d87b6c57270af9abdfbeaa5d7b88d813a4a28d984d16207ed038818da86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.9` - linux; amd64

```console
$ docker pull clickhouse@sha256:24c147a07e416691cef95aae7ffa58ea07439880fd3022fbff329329a74ac049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179305080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8481deefc73e3bcb2c21bd0d76d8c2415b41fcc564993e7621fd4940409c1db7`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.9.3.128
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e15b0b4d694bad5f3c6ca5e5744f61f6f07837e6dcf88c5dd86ce6646b65f39`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 8.8 MB (8802589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ba56f782ba1762e80edd7d2920b4b0970a37f738f8284be32d04ed9efddf2a`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 142.1 MB (142124154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5fd0be77bf5fef30f129aa2516620add4a583706017496cc11384924ce4ead`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecda6c4ae5ded0d521129071991a02ed0fee3c43f544a5358e77c6c89036ebf`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b2f8d34b2bbcca1e9b028a99c34b66a57c80d78d50151d2e7ed46daa6a7808`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217024fbf7f8b25ec8ce47d74c2a1ffead51e7364c018fd410c8fd180677b55f`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105b54b1cca978a37bee956925552d8b406dd1211ff113c1fd2ca37186190246`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:83e6726807428e467a209397221766017bd35c36cebd3291edaf23dfd4d4d876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b65aadce97ae243b0258cd77399b506f0ec9f6ce53229548cad3b054b85191`

```dockerfile
```

-	Layers:
	-	`sha256:d99e3dea25205bcee42d5ec71a98fa8c98d79fa3aabea5f6b207c80320136afc`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 25.3 KB (25274 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.9` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ff0663d28148ff37f407c0747c0ec2ee1daa7edf402902e297b9498e72f185d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172636079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9757d60d8ef45953a75e2064857bc2840a2e9852e16836453128270a67f0679`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.9.3.128
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54eee1a828755b8263fe2502b17ab154bf021d94eb2f403be0f11c9114c4fbdb`  
		Last Modified: Mon, 18 Nov 2024 20:07:04 GMT  
		Size: 137.1 MB (137132654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f774813cb7f9b1a6441941042f3066f75022a99edb91b1b2c957a7a3b61757`  
		Last Modified: Mon, 18 Nov 2024 20:07:01 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952515573b1c5460b81626a0a61476bb346e4e70b923a873661af0cbd18fabeb`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd67aeea5e6ea64c2f333b0a053da848613823a6f686d77d8e19696b1374f0a`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dbe23c4dcb320ba874bc91b536a8d51463d9ac61ba829ed901b1a2be327b36`  
		Last Modified: Mon, 18 Nov 2024 20:07:03 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe91bb7b2da741a03a2af4eb41773365e8ae5e4a499c68409bb27a146a04c261`  
		Last Modified: Mon, 18 Nov 2024 20:07:03 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1897282b473c2d034c8566a4d3d83039be197c92469ae5b61594cbc6fc00357d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f05f49e41fb1f170d36e02cffe5ebc991782bd236d1e9edafa0d36af3de38bb`

```dockerfile
```

-	Layers:
	-	`sha256:394afef8bb85ec6c69f19efabcddc608c825603d4cf61ceffdc415ceb5851332`  
		Last Modified: Mon, 18 Nov 2024 20:07:01 GMT  
		Size: 25.5 KB (25462 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.9-focal`

```console
$ docker pull clickhouse@sha256:95917d87b6c57270af9abdfbeaa5d7b88d813a4a28d984d16207ed038818da86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.9-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:24c147a07e416691cef95aae7ffa58ea07439880fd3022fbff329329a74ac049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179305080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8481deefc73e3bcb2c21bd0d76d8c2415b41fcc564993e7621fd4940409c1db7`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.9.3.128
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e15b0b4d694bad5f3c6ca5e5744f61f6f07837e6dcf88c5dd86ce6646b65f39`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 8.8 MB (8802589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ba56f782ba1762e80edd7d2920b4b0970a37f738f8284be32d04ed9efddf2a`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 142.1 MB (142124154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5fd0be77bf5fef30f129aa2516620add4a583706017496cc11384924ce4ead`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecda6c4ae5ded0d521129071991a02ed0fee3c43f544a5358e77c6c89036ebf`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b2f8d34b2bbcca1e9b028a99c34b66a57c80d78d50151d2e7ed46daa6a7808`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217024fbf7f8b25ec8ce47d74c2a1ffead51e7364c018fd410c8fd180677b55f`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105b54b1cca978a37bee956925552d8b406dd1211ff113c1fd2ca37186190246`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:83e6726807428e467a209397221766017bd35c36cebd3291edaf23dfd4d4d876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b65aadce97ae243b0258cd77399b506f0ec9f6ce53229548cad3b054b85191`

```dockerfile
```

-	Layers:
	-	`sha256:d99e3dea25205bcee42d5ec71a98fa8c98d79fa3aabea5f6b207c80320136afc`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 25.3 KB (25274 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.9-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ff0663d28148ff37f407c0747c0ec2ee1daa7edf402902e297b9498e72f185d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172636079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9757d60d8ef45953a75e2064857bc2840a2e9852e16836453128270a67f0679`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.9.3.128
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54eee1a828755b8263fe2502b17ab154bf021d94eb2f403be0f11c9114c4fbdb`  
		Last Modified: Mon, 18 Nov 2024 20:07:04 GMT  
		Size: 137.1 MB (137132654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f774813cb7f9b1a6441941042f3066f75022a99edb91b1b2c957a7a3b61757`  
		Last Modified: Mon, 18 Nov 2024 20:07:01 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952515573b1c5460b81626a0a61476bb346e4e70b923a873661af0cbd18fabeb`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd67aeea5e6ea64c2f333b0a053da848613823a6f686d77d8e19696b1374f0a`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dbe23c4dcb320ba874bc91b536a8d51463d9ac61ba829ed901b1a2be327b36`  
		Last Modified: Mon, 18 Nov 2024 20:07:03 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe91bb7b2da741a03a2af4eb41773365e8ae5e4a499c68409bb27a146a04c261`  
		Last Modified: Mon, 18 Nov 2024 20:07:03 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1897282b473c2d034c8566a4d3d83039be197c92469ae5b61594cbc6fc00357d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f05f49e41fb1f170d36e02cffe5ebc991782bd236d1e9edafa0d36af3de38bb`

```dockerfile
```

-	Layers:
	-	`sha256:394afef8bb85ec6c69f19efabcddc608c825603d4cf61ceffdc415ceb5851332`  
		Last Modified: Mon, 18 Nov 2024 20:07:01 GMT  
		Size: 25.5 KB (25462 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.9.3`

```console
$ docker pull clickhouse@sha256:95917d87b6c57270af9abdfbeaa5d7b88d813a4a28d984d16207ed038818da86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.9.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:24c147a07e416691cef95aae7ffa58ea07439880fd3022fbff329329a74ac049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179305080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8481deefc73e3bcb2c21bd0d76d8c2415b41fcc564993e7621fd4940409c1db7`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.9.3.128
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e15b0b4d694bad5f3c6ca5e5744f61f6f07837e6dcf88c5dd86ce6646b65f39`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 8.8 MB (8802589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ba56f782ba1762e80edd7d2920b4b0970a37f738f8284be32d04ed9efddf2a`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 142.1 MB (142124154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5fd0be77bf5fef30f129aa2516620add4a583706017496cc11384924ce4ead`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecda6c4ae5ded0d521129071991a02ed0fee3c43f544a5358e77c6c89036ebf`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b2f8d34b2bbcca1e9b028a99c34b66a57c80d78d50151d2e7ed46daa6a7808`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217024fbf7f8b25ec8ce47d74c2a1ffead51e7364c018fd410c8fd180677b55f`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105b54b1cca978a37bee956925552d8b406dd1211ff113c1fd2ca37186190246`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:83e6726807428e467a209397221766017bd35c36cebd3291edaf23dfd4d4d876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b65aadce97ae243b0258cd77399b506f0ec9f6ce53229548cad3b054b85191`

```dockerfile
```

-	Layers:
	-	`sha256:d99e3dea25205bcee42d5ec71a98fa8c98d79fa3aabea5f6b207c80320136afc`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 25.3 KB (25274 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.9.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ff0663d28148ff37f407c0747c0ec2ee1daa7edf402902e297b9498e72f185d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172636079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9757d60d8ef45953a75e2064857bc2840a2e9852e16836453128270a67f0679`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.9.3.128
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54eee1a828755b8263fe2502b17ab154bf021d94eb2f403be0f11c9114c4fbdb`  
		Last Modified: Mon, 18 Nov 2024 20:07:04 GMT  
		Size: 137.1 MB (137132654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f774813cb7f9b1a6441941042f3066f75022a99edb91b1b2c957a7a3b61757`  
		Last Modified: Mon, 18 Nov 2024 20:07:01 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952515573b1c5460b81626a0a61476bb346e4e70b923a873661af0cbd18fabeb`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd67aeea5e6ea64c2f333b0a053da848613823a6f686d77d8e19696b1374f0a`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dbe23c4dcb320ba874bc91b536a8d51463d9ac61ba829ed901b1a2be327b36`  
		Last Modified: Mon, 18 Nov 2024 20:07:03 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe91bb7b2da741a03a2af4eb41773365e8ae5e4a499c68409bb27a146a04c261`  
		Last Modified: Mon, 18 Nov 2024 20:07:03 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1897282b473c2d034c8566a4d3d83039be197c92469ae5b61594cbc6fc00357d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f05f49e41fb1f170d36e02cffe5ebc991782bd236d1e9edafa0d36af3de38bb`

```dockerfile
```

-	Layers:
	-	`sha256:394afef8bb85ec6c69f19efabcddc608c825603d4cf61ceffdc415ceb5851332`  
		Last Modified: Mon, 18 Nov 2024 20:07:01 GMT  
		Size: 25.5 KB (25462 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.9.3-focal`

```console
$ docker pull clickhouse@sha256:95917d87b6c57270af9abdfbeaa5d7b88d813a4a28d984d16207ed038818da86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.9.3-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:24c147a07e416691cef95aae7ffa58ea07439880fd3022fbff329329a74ac049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179305080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8481deefc73e3bcb2c21bd0d76d8c2415b41fcc564993e7621fd4940409c1db7`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.9.3.128
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e15b0b4d694bad5f3c6ca5e5744f61f6f07837e6dcf88c5dd86ce6646b65f39`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 8.8 MB (8802589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ba56f782ba1762e80edd7d2920b4b0970a37f738f8284be32d04ed9efddf2a`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 142.1 MB (142124154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5fd0be77bf5fef30f129aa2516620add4a583706017496cc11384924ce4ead`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecda6c4ae5ded0d521129071991a02ed0fee3c43f544a5358e77c6c89036ebf`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b2f8d34b2bbcca1e9b028a99c34b66a57c80d78d50151d2e7ed46daa6a7808`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217024fbf7f8b25ec8ce47d74c2a1ffead51e7364c018fd410c8fd180677b55f`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105b54b1cca978a37bee956925552d8b406dd1211ff113c1fd2ca37186190246`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9.3-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:83e6726807428e467a209397221766017bd35c36cebd3291edaf23dfd4d4d876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b65aadce97ae243b0258cd77399b506f0ec9f6ce53229548cad3b054b85191`

```dockerfile
```

-	Layers:
	-	`sha256:d99e3dea25205bcee42d5ec71a98fa8c98d79fa3aabea5f6b207c80320136afc`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 25.3 KB (25274 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.9.3-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ff0663d28148ff37f407c0747c0ec2ee1daa7edf402902e297b9498e72f185d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172636079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9757d60d8ef45953a75e2064857bc2840a2e9852e16836453128270a67f0679`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.9.3.128
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54eee1a828755b8263fe2502b17ab154bf021d94eb2f403be0f11c9114c4fbdb`  
		Last Modified: Mon, 18 Nov 2024 20:07:04 GMT  
		Size: 137.1 MB (137132654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f774813cb7f9b1a6441941042f3066f75022a99edb91b1b2c957a7a3b61757`  
		Last Modified: Mon, 18 Nov 2024 20:07:01 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952515573b1c5460b81626a0a61476bb346e4e70b923a873661af0cbd18fabeb`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd67aeea5e6ea64c2f333b0a053da848613823a6f686d77d8e19696b1374f0a`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dbe23c4dcb320ba874bc91b536a8d51463d9ac61ba829ed901b1a2be327b36`  
		Last Modified: Mon, 18 Nov 2024 20:07:03 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe91bb7b2da741a03a2af4eb41773365e8ae5e4a499c68409bb27a146a04c261`  
		Last Modified: Mon, 18 Nov 2024 20:07:03 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9.3-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1897282b473c2d034c8566a4d3d83039be197c92469ae5b61594cbc6fc00357d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f05f49e41fb1f170d36e02cffe5ebc991782bd236d1e9edafa0d36af3de38bb`

```dockerfile
```

-	Layers:
	-	`sha256:394afef8bb85ec6c69f19efabcddc608c825603d4cf61ceffdc415ceb5851332`  
		Last Modified: Mon, 18 Nov 2024 20:07:01 GMT  
		Size: 25.5 KB (25462 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.9.3.128`

```console
$ docker pull clickhouse@sha256:95917d87b6c57270af9abdfbeaa5d7b88d813a4a28d984d16207ed038818da86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.9.3.128` - linux; amd64

```console
$ docker pull clickhouse@sha256:24c147a07e416691cef95aae7ffa58ea07439880fd3022fbff329329a74ac049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179305080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8481deefc73e3bcb2c21bd0d76d8c2415b41fcc564993e7621fd4940409c1db7`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.9.3.128
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e15b0b4d694bad5f3c6ca5e5744f61f6f07837e6dcf88c5dd86ce6646b65f39`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 8.8 MB (8802589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ba56f782ba1762e80edd7d2920b4b0970a37f738f8284be32d04ed9efddf2a`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 142.1 MB (142124154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5fd0be77bf5fef30f129aa2516620add4a583706017496cc11384924ce4ead`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecda6c4ae5ded0d521129071991a02ed0fee3c43f544a5358e77c6c89036ebf`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b2f8d34b2bbcca1e9b028a99c34b66a57c80d78d50151d2e7ed46daa6a7808`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217024fbf7f8b25ec8ce47d74c2a1ffead51e7364c018fd410c8fd180677b55f`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105b54b1cca978a37bee956925552d8b406dd1211ff113c1fd2ca37186190246`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9.3.128` - unknown; unknown

```console
$ docker pull clickhouse@sha256:83e6726807428e467a209397221766017bd35c36cebd3291edaf23dfd4d4d876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b65aadce97ae243b0258cd77399b506f0ec9f6ce53229548cad3b054b85191`

```dockerfile
```

-	Layers:
	-	`sha256:d99e3dea25205bcee42d5ec71a98fa8c98d79fa3aabea5f6b207c80320136afc`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 25.3 KB (25274 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.9.3.128` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ff0663d28148ff37f407c0747c0ec2ee1daa7edf402902e297b9498e72f185d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172636079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9757d60d8ef45953a75e2064857bc2840a2e9852e16836453128270a67f0679`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.9.3.128
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54eee1a828755b8263fe2502b17ab154bf021d94eb2f403be0f11c9114c4fbdb`  
		Last Modified: Mon, 18 Nov 2024 20:07:04 GMT  
		Size: 137.1 MB (137132654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f774813cb7f9b1a6441941042f3066f75022a99edb91b1b2c957a7a3b61757`  
		Last Modified: Mon, 18 Nov 2024 20:07:01 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952515573b1c5460b81626a0a61476bb346e4e70b923a873661af0cbd18fabeb`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd67aeea5e6ea64c2f333b0a053da848613823a6f686d77d8e19696b1374f0a`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dbe23c4dcb320ba874bc91b536a8d51463d9ac61ba829ed901b1a2be327b36`  
		Last Modified: Mon, 18 Nov 2024 20:07:03 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe91bb7b2da741a03a2af4eb41773365e8ae5e4a499c68409bb27a146a04c261`  
		Last Modified: Mon, 18 Nov 2024 20:07:03 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9.3.128` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1897282b473c2d034c8566a4d3d83039be197c92469ae5b61594cbc6fc00357d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f05f49e41fb1f170d36e02cffe5ebc991782bd236d1e9edafa0d36af3de38bb`

```dockerfile
```

-	Layers:
	-	`sha256:394afef8bb85ec6c69f19efabcddc608c825603d4cf61ceffdc415ceb5851332`  
		Last Modified: Mon, 18 Nov 2024 20:07:01 GMT  
		Size: 25.5 KB (25462 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.9.3.128-focal`

```console
$ docker pull clickhouse@sha256:95917d87b6c57270af9abdfbeaa5d7b88d813a4a28d984d16207ed038818da86
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.9.3.128-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:24c147a07e416691cef95aae7ffa58ea07439880fd3022fbff329329a74ac049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.3 MB (179305080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8481deefc73e3bcb2c21bd0d76d8c2415b41fcc564993e7621fd4940409c1db7`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.9.3.128
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e15b0b4d694bad5f3c6ca5e5744f61f6f07837e6dcf88c5dd86ce6646b65f39`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 8.8 MB (8802589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ba56f782ba1762e80edd7d2920b4b0970a37f738f8284be32d04ed9efddf2a`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 142.1 MB (142124154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5fd0be77bf5fef30f129aa2516620add4a583706017496cc11384924ce4ead`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecda6c4ae5ded0d521129071991a02ed0fee3c43f544a5358e77c6c89036ebf`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b2f8d34b2bbcca1e9b028a99c34b66a57c80d78d50151d2e7ed46daa6a7808`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217024fbf7f8b25ec8ce47d74c2a1ffead51e7364c018fd410c8fd180677b55f`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105b54b1cca978a37bee956925552d8b406dd1211ff113c1fd2ca37186190246`  
		Last Modified: Mon, 18 Nov 2024 20:06:14 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9.3.128-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:83e6726807428e467a209397221766017bd35c36cebd3291edaf23dfd4d4d876
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b65aadce97ae243b0258cd77399b506f0ec9f6ce53229548cad3b054b85191`

```dockerfile
```

-	Layers:
	-	`sha256:d99e3dea25205bcee42d5ec71a98fa8c98d79fa3aabea5f6b207c80320136afc`  
		Last Modified: Mon, 18 Nov 2024 20:06:13 GMT  
		Size: 25.3 KB (25274 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.9.3.128-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ff0663d28148ff37f407c0747c0ec2ee1daa7edf402902e297b9498e72f185d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.6 MB (172636079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9757d60d8ef45953a75e2064857bc2840a2e9852e16836453128270a67f0679`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.9.3.128
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.9.3.128 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54eee1a828755b8263fe2502b17ab154bf021d94eb2f403be0f11c9114c4fbdb`  
		Last Modified: Mon, 18 Nov 2024 20:07:04 GMT  
		Size: 137.1 MB (137132654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f774813cb7f9b1a6441941042f3066f75022a99edb91b1b2c957a7a3b61757`  
		Last Modified: Mon, 18 Nov 2024 20:07:01 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952515573b1c5460b81626a0a61476bb346e4e70b923a873661af0cbd18fabeb`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd67aeea5e6ea64c2f333b0a053da848613823a6f686d77d8e19696b1374f0a`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47dbe23c4dcb320ba874bc91b536a8d51463d9ac61ba829ed901b1a2be327b36`  
		Last Modified: Mon, 18 Nov 2024 20:07:03 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe91bb7b2da741a03a2af4eb41773365e8ae5e4a499c68409bb27a146a04c261`  
		Last Modified: Mon, 18 Nov 2024 20:07:03 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.9.3.128-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1897282b473c2d034c8566a4d3d83039be197c92469ae5b61594cbc6fc00357d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f05f49e41fb1f170d36e02cffe5ebc991782bd236d1e9edafa0d36af3de38bb`

```dockerfile
```

-	Layers:
	-	`sha256:394afef8bb85ec6c69f19efabcddc608c825603d4cf61ceffdc415ceb5851332`  
		Last Modified: Mon, 18 Nov 2024 20:07:01 GMT  
		Size: 25.5 KB (25462 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:focal`

```console
$ docker pull clickhouse@sha256:aa887dfaa8d915a18ad93d25cef0334138ffeeb386353600ed90ecf07ff4eb5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:3073efa0428c680834cf03dd2428fac3408a8a60310cd0613f51731eb25bcdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180553647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33410aa159ab43ebeaa868575df2dc69997cf9bbc495f419df632b5938060b2e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11845068165d574aa2798c6158bf4904622cd7aff2c5675c6643ff0ba4fda74`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 8.8 MB (8802587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5feec6ebdd2d272ba4886d83efac935f56f806e73e527a868a28138c61e67718`  
		Last Modified: Mon, 18 Nov 2024 21:06:08 GMT  
		Size: 143.4 MB (143372719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfeab913ab2cc5b1eae6e120652382b1e4419e753305cbecd10ed1fd65a4bc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1a6ccef3905d7f4b64758101a5566220595da9cd94b3a8efe3c7c3d500827`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52154b45f848fae4d6dc15923fd51d332c33b0e778b1c11e06eb83e661dd7a95`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b265890db07ff12d8c1d5226fa954754fc2424e3c212fb8ec6357953893fe05f`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff950eeed9b85019e89aaffe2962b82fdbc03b54f59941891af221eb1511d3a4`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:064a3c846ada78d4c69bda131ebe8c761653440c1cc0f3585a7a48d399021fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c888f3eb66030483fa7a082a00d60e89b78ac7a1f1e67da42a74eca0169fae`

```dockerfile
```

-	Layers:
	-	`sha256:f50539b9c37f17df612e4afdb20de110705ae3090a3db1da1b402faa4f251cc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:05 GMT  
		Size: 26.5 KB (26499 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f36884dc6d24d60a9bb6c320e8a052190ae2358d8f66efc4c71ad5ffa4638d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174195698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68ae827e8dcb485e903cb0057678535df1e43de4da3302cf7efd6fb2bcb936e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86846b838547ebb3f9804d50f4fe8eb4f6bfeff8d4821e1998c250e0dfd1a11`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 8.7 MB (8662233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7371f123ab3df4a130514d8f7597c2f06a212dda18e5943a8eb98574c2d0b52`  
		Last Modified: Mon, 18 Nov 2024 20:05:57 GMT  
		Size: 138.7 MB (138692361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a627ba3ba9c0dd7675bded26bee97be800d7ae7233b65cc5e87dec6385d6d684`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eab81eafda560d04753033a7793b0fbad07c01a37f4e1fa1b6cbb5d57fbe8d`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b4918a2555f120c31a57c5c66f22600ab0bc3d121542385b9eb52b639f3796`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6c7d5229f43bb415dcabb1c0fd300ecc1dbfed18d77c6e553ba203fcc0d0`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30b9bec89bc291fd156ad60a897a8bc119acda2d3294db0909a7abb9b7aa124`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2f77217c545db83c44c23cc6abdf4f34ce68265d9e261c4af075dc598e2811bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca457bdd672219881e4c7f28900a0fb3c0f87120ecf163a2c6fbfddd3eb9cf2d`

```dockerfile
```

-	Layers:
	-	`sha256:5791af50f4fcfa896eb3c0edf644ae24c07abc17fd5982c1cbb1724b8ede7636`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 26.7 KB (26735 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:aa887dfaa8d915a18ad93d25cef0334138ffeeb386353600ed90ecf07ff4eb5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:3073efa0428c680834cf03dd2428fac3408a8a60310cd0613f51731eb25bcdb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180553647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33410aa159ab43ebeaa868575df2dc69997cf9bbc495f419df632b5938060b2e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11845068165d574aa2798c6158bf4904622cd7aff2c5675c6643ff0ba4fda74`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 8.8 MB (8802587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5feec6ebdd2d272ba4886d83efac935f56f806e73e527a868a28138c61e67718`  
		Last Modified: Mon, 18 Nov 2024 21:06:08 GMT  
		Size: 143.4 MB (143372719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfeab913ab2cc5b1eae6e120652382b1e4419e753305cbecd10ed1fd65a4bc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e1a6ccef3905d7f4b64758101a5566220595da9cd94b3a8efe3c7c3d500827`  
		Last Modified: Mon, 18 Nov 2024 21:06:03 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52154b45f848fae4d6dc15923fd51d332c33b0e778b1c11e06eb83e661dd7a95`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b265890db07ff12d8c1d5226fa954754fc2424e3c212fb8ec6357953893fe05f`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff950eeed9b85019e89aaffe2962b82fdbc03b54f59941891af221eb1511d3a4`  
		Last Modified: Mon, 18 Nov 2024 21:06:04 GMT  
		Size: 3.1 KB (3143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:064a3c846ada78d4c69bda131ebe8c761653440c1cc0f3585a7a48d399021fad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c888f3eb66030483fa7a082a00d60e89b78ac7a1f1e67da42a74eca0169fae`

```dockerfile
```

-	Layers:
	-	`sha256:f50539b9c37f17df612e4afdb20de110705ae3090a3db1da1b402faa4f251cc6`  
		Last Modified: Mon, 18 Nov 2024 21:06:05 GMT  
		Size: 26.5 KB (26499 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f36884dc6d24d60a9bb6c320e8a052190ae2358d8f66efc4c71ad5ffa4638d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.2 MB (174195698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a68ae827e8dcb485e903cb0057678535df1e43de4da3302cf7efd6fb2bcb936e`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.10.2.80
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.10.2.80 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a86846b838547ebb3f9804d50f4fe8eb4f6bfeff8d4821e1998c250e0dfd1a11`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 8.7 MB (8662233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7371f123ab3df4a130514d8f7597c2f06a212dda18e5943a8eb98574c2d0b52`  
		Last Modified: Mon, 18 Nov 2024 20:05:57 GMT  
		Size: 138.7 MB (138692361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a627ba3ba9c0dd7675bded26bee97be800d7ae7233b65cc5e87dec6385d6d684`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7eab81eafda560d04753033a7793b0fbad07c01a37f4e1fa1b6cbb5d57fbe8d`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b4918a2555f120c31a57c5c66f22600ab0bc3d121542385b9eb52b639f3796`  
		Last Modified: Mon, 18 Nov 2024 20:05:54 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4db6c7d5229f43bb415dcabb1c0fd300ecc1dbfed18d77c6e553ba203fcc0d0`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30b9bec89bc291fd156ad60a897a8bc119acda2d3294db0909a7abb9b7aa124`  
		Last Modified: Mon, 18 Nov 2024 20:05:55 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2f77217c545db83c44c23cc6abdf4f34ce68265d9e261c4af075dc598e2811bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca457bdd672219881e4c7f28900a0fb3c0f87120ecf163a2c6fbfddd3eb9cf2d`

```dockerfile
```

-	Layers:
	-	`sha256:5791af50f4fcfa896eb3c0edf644ae24c07abc17fd5982c1cbb1724b8ede7636`  
		Last Modified: Mon, 18 Nov 2024 20:05:53 GMT  
		Size: 26.7 KB (26735 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:698363cd1136335696abf40a67f5546127dfdf5fe6ad2ca88fe60cd3ae7bdf2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:47cef6f2fbb1fb511670b86d9f4783ec9cfa3c072a40a59282a980cf38b6aa0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178812657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1387e7bdaf532e3d74a9b01fa5552a8d49c42257102256a8dd84a75943af949`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.8.7.41
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e67b6741df06aa8eb8d8fcb7c95e8cc10d7e92f9a3cb3181ae40f97bba8a4f2`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 8.8 MB (8802629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ba309f2e22dfad8a2676a95340a87935e01c40b10278c763606e6a38f8ae3f`  
		Last Modified: Mon, 18 Nov 2024 20:06:18 GMT  
		Size: 141.6 MB (141631685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48aef40100afaae89d86927eec76e4e414602914f5b5e776ca029cf0907bf538`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f960df628b7b0375c45e65adc733c6779004504ec3ef541e913e73cc895b07`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec64844717ad2ae00fe14780a6cc2f44eb95615036366e291852afabf464492f`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4d29135e7f625c0a17e60870a4120bf338bf85646c29a1281f4c26ef11796b`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cfd9c027f10cb6506f9e0695b3c98044eab94a91ebe1b125e9b3f95f4e54c9`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b101c6fca19411ff534750286eaf83eecb9bb127846c5077bbf85882c93b6d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c985ecdf74273a1483a770cc4add37729a95eaf93cd09b69b9f5433d9ab26f`

```dockerfile
```

-	Layers:
	-	`sha256:1c0ef4be653a14e13ddd9f068f8b7e943b538376f38f98b9a9c90b9ee1ceb60a`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d00c2769c76341b3cf1a4dc8e9f5a5b1ee9b893de45609ae576556ebab7882ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172188479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c08925b341a204c06bd134b161f7126a241b3031a0a0d2fc3ab207d2c58bef0`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.8.7.41
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03120df1d949cda902248b711ed24360e5f33e29ab93d0fcc3ad4f49f4c94663`  
		Last Modified: Mon, 18 Nov 2024 20:08:02 GMT  
		Size: 136.7 MB (136685053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05d90f88b9b12fdedfe65bc756bff7ebf2bcd74475f8002682c5912815c5ea0`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73efb287cd7a74820405dc5e4d603782ddab7a5d7675d8257e9b89562076788`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021af34596bc467a509c70e886da66789b1d1cbb835980cfb8d2e74962bd504a`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf8f562b370201341e7dfa04698b7cd723787c43682db929bc33aa4618dc511`  
		Last Modified: Mon, 18 Nov 2024 20:07:59 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127256b32943afe8f2b034ae5168c0037568ed72ab28fecb0336a496b56352bf`  
		Last Modified: Mon, 18 Nov 2024 20:07:59 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dee6a322dd46dd22fbcda8db3070427a0d203231dfafa78e92767b46a3a20ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4ccb8f250378ac75e417fc9c9f2ec26e248ad4d82ded701075407f0e6c2dab`

```dockerfile
```

-	Layers:
	-	`sha256:df1379770a3a3a41c884e93ea770d057adc7fb09481238e53c57279c24b95360`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-focal`

```console
$ docker pull clickhouse@sha256:698363cd1136335696abf40a67f5546127dfdf5fe6ad2ca88fe60cd3ae7bdf2e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:47cef6f2fbb1fb511670b86d9f4783ec9cfa3c072a40a59282a980cf38b6aa0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.8 MB (178812657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1387e7bdaf532e3d74a9b01fa5552a8d49c42257102256a8dd84a75943af949`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.8.7.41
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 11 Oct 2024 04:41:25 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e67b6741df06aa8eb8d8fcb7c95e8cc10d7e92f9a3cb3181ae40f97bba8a4f2`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 8.8 MB (8802629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ba309f2e22dfad8a2676a95340a87935e01c40b10278c763606e6a38f8ae3f`  
		Last Modified: Mon, 18 Nov 2024 20:06:18 GMT  
		Size: 141.6 MB (141631685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48aef40100afaae89d86927eec76e4e414602914f5b5e776ca029cf0907bf538`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f960df628b7b0375c45e65adc733c6779004504ec3ef541e913e73cc895b07`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec64844717ad2ae00fe14780a6cc2f44eb95615036366e291852afabf464492f`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4d29135e7f625c0a17e60870a4120bf338bf85646c29a1281f4c26ef11796b`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cfd9c027f10cb6506f9e0695b3c98044eab94a91ebe1b125e9b3f95f4e54c9`  
		Last Modified: Mon, 18 Nov 2024 20:06:16 GMT  
		Size: 3.1 KB (3142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b101c6fca19411ff534750286eaf83eecb9bb127846c5077bbf85882c93b6d5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c985ecdf74273a1483a770cc4add37729a95eaf93cd09b69b9f5433d9ab26f`

```dockerfile
```

-	Layers:
	-	`sha256:1c0ef4be653a14e13ddd9f068f8b7e943b538376f38f98b9a9c90b9ee1ceb60a`  
		Last Modified: Mon, 18 Nov 2024 20:06:15 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d00c2769c76341b3cf1a4dc8e9f5a5b1ee9b893de45609ae576556ebab7882ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172188479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c08925b341a204c06bd134b161f7126a241b3031a0a0d2fc3ab207d2c58bef0`
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
# Mon, 18 Nov 2024 17:56:28 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 18 Nov 2024 17:56:28 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPO_CHANNEL=stable
# Mon, 18 Nov 2024 17:56:28 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 18 Nov 2024 17:56:28 GMT
ARG VERSION=24.8.7.41
# Mon, 18 Nov 2024 17:56:28 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 18 Nov 2024 17:56:28 GMT
ENV TZ=UTC
# Mon, 18 Nov 2024 17:56:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.7.41 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 18 Nov 2024 17:56:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 18 Nov 2024 17:56:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 18 Nov 2024 17:56:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 18 Nov 2024 17:56:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5085ce1b8372caa58717960d0f8dcb37ae411893306a36fe2c4f69ced7d8b16`  
		Last Modified: Mon, 18 Nov 2024 20:07:02 GMT  
		Size: 8.7 MB (8662322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03120df1d949cda902248b711ed24360e5f33e29ab93d0fcc3ad4f49f4c94663`  
		Last Modified: Mon, 18 Nov 2024 20:08:02 GMT  
		Size: 136.7 MB (136685053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05d90f88b9b12fdedfe65bc756bff7ebf2bcd74475f8002682c5912815c5ea0`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73efb287cd7a74820405dc5e4d603782ddab7a5d7675d8257e9b89562076788`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021af34596bc467a509c70e886da66789b1d1cbb835980cfb8d2e74962bd504a`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf8f562b370201341e7dfa04698b7cd723787c43682db929bc33aa4618dc511`  
		Last Modified: Mon, 18 Nov 2024 20:07:59 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127256b32943afe8f2b034ae5168c0037568ed72ab28fecb0336a496b56352bf`  
		Last Modified: Mon, 18 Nov 2024 20:07:59 GMT  
		Size: 3.1 KB (3141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dee6a322dd46dd22fbcda8db3070427a0d203231dfafa78e92767b46a3a20ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f4ccb8f250378ac75e417fc9c9f2ec26e248ad4d82ded701075407f0e6c2dab`

```dockerfile
```

-	Layers:
	-	`sha256:df1379770a3a3a41c884e93ea770d057adc7fb09481238e53c57279c24b95360`  
		Last Modified: Mon, 18 Nov 2024 20:07:58 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json
