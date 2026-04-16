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
$ docker pull clickhouse@sha256:d08ef7e5c4e63e0eaeef28931d4bdb14b3a137b145f051ad0b412ad4177bd3d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:2c6a916521b336977982b4526b201da46c479186ba03ae22f4fefe4e5990908a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229199945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32184c254de283578043bd8bc12b1c9a24075169b6dd1b0f5e262fa644e532f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:09 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:09 GMT
ARG VERSION=25.8.21.7
# Wed, 15 Apr 2026 20:25:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:34 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:34 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:34 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca91fdcc0abda421ad01afd641f21a86e5aedeec12704c8ae17b0bc8abd7f3c4`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 7.6 MB (7599174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173eda4e42a7e303295d09d787f66b4ce7a1f60c576a2404868f44a9c3e3c358`  
		Last Modified: Wed, 15 Apr 2026 20:26:00 GMT  
		Size: 191.0 MB (190994252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f3de34b92920b427cfa577d6818c1ae2bc52bb4b740990b77ad22016a30795`  
		Last Modified: Wed, 15 Apr 2026 20:25:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ae818cf2593b3e9bd21cad01067297e382eea2ca6143c10b05d56c9d724b50`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bea843884b2f8c1fcfe1ca39e3df84e54d79dc529165b5521a79a405375ee8`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4de75be46064f44a11544c9a6c919e3d2767f7fc913fd8a665d22320cb3f918`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783dcf9319aa518231cffdb24c1cc4b4ad6968b63244f90e96f0664cca6c348b`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:aab03bc7e9d1359d915ea6ece8e208a609ee87e8cce9e20c2193d2d0ae707654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c466a2b1fcbaf9dcaf14221e19dfd68453432d74535cfd1e94a3a1766e89a6b`

```dockerfile
```

-	Layers:
	-	`sha256:195eeef671b51cd00fe7b76beabcde45643575fc10fb7e3e943b3adc6d97fa51`  
		Last Modified: Wed, 15 Apr 2026 20:25:55 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b12416eec37ab984ab05721df17517f8977a83022b52a1dbab8d565f3b36cbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214146936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28cd611923331ff8cc025f7c7aff0e78f37eaf4635661c1ec086dff61a66dcb6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:43 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:43 GMT
ARG VERSION=25.8.21.7
# Wed, 15 Apr 2026 20:24:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:17 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:17 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24772a921c5468694e52f31ef95c6f3838b85ba2d0b281dde1f121b542be9dfd`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 7.6 MB (7578842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9005a53f6c0a99e09d71101e29f5c22e4fb5f3bb43ecdf4b47f7750e807352bb`  
		Last Modified: Wed, 15 Apr 2026 20:25:45 GMT  
		Size: 178.1 MB (178091526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0448445e755843df85d2e503a2b4c3ee49cbc788cb3de60d5bf1dfcced704798`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6d60b7dec12989e85afe46c49b0aa33d18800737f00d87020988db7148295c`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8665be37a8553d3f13ece05b0cf49e22eb2e9455b7447cf49cb53059a6b133fe`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1540e63cc82538954ccd9d0a1695c3c9fa68873706490d9ed380a28ed18a0208`  
		Last Modified: Wed, 15 Apr 2026 20:25:38 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26a21419191f0f324aaabb8f0f963618b08a2426d1fbb9ccfbb4f4d2d1f04c6`  
		Last Modified: Wed, 15 Apr 2026 20:25:38 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:90be94b8fc0796e4fea05b3b48d4bda0b0baa136c307a7d4d255f9a3f5da086d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501facc23c4a02ef653bc8d51a2534485afa726194e086656743cf5684fd89e9`

```dockerfile
```

-	Layers:
	-	`sha256:bd776e838bd7ab1d599ecc3b7ece2a507838a4b50672db6c416b470aa9a469d4`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:d08ef7e5c4e63e0eaeef28931d4bdb14b3a137b145f051ad0b412ad4177bd3d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:2c6a916521b336977982b4526b201da46c479186ba03ae22f4fefe4e5990908a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229199945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32184c254de283578043bd8bc12b1c9a24075169b6dd1b0f5e262fa644e532f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:09 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:09 GMT
ARG VERSION=25.8.21.7
# Wed, 15 Apr 2026 20:25:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:34 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:34 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:34 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca91fdcc0abda421ad01afd641f21a86e5aedeec12704c8ae17b0bc8abd7f3c4`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 7.6 MB (7599174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173eda4e42a7e303295d09d787f66b4ce7a1f60c576a2404868f44a9c3e3c358`  
		Last Modified: Wed, 15 Apr 2026 20:26:00 GMT  
		Size: 191.0 MB (190994252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f3de34b92920b427cfa577d6818c1ae2bc52bb4b740990b77ad22016a30795`  
		Last Modified: Wed, 15 Apr 2026 20:25:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ae818cf2593b3e9bd21cad01067297e382eea2ca6143c10b05d56c9d724b50`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bea843884b2f8c1fcfe1ca39e3df84e54d79dc529165b5521a79a405375ee8`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4de75be46064f44a11544c9a6c919e3d2767f7fc913fd8a665d22320cb3f918`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783dcf9319aa518231cffdb24c1cc4b4ad6968b63244f90e96f0664cca6c348b`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:aab03bc7e9d1359d915ea6ece8e208a609ee87e8cce9e20c2193d2d0ae707654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c466a2b1fcbaf9dcaf14221e19dfd68453432d74535cfd1e94a3a1766e89a6b`

```dockerfile
```

-	Layers:
	-	`sha256:195eeef671b51cd00fe7b76beabcde45643575fc10fb7e3e943b3adc6d97fa51`  
		Last Modified: Wed, 15 Apr 2026 20:25:55 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b12416eec37ab984ab05721df17517f8977a83022b52a1dbab8d565f3b36cbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214146936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28cd611923331ff8cc025f7c7aff0e78f37eaf4635661c1ec086dff61a66dcb6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:43 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:43 GMT
ARG VERSION=25.8.21.7
# Wed, 15 Apr 2026 20:24:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:17 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:17 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24772a921c5468694e52f31ef95c6f3838b85ba2d0b281dde1f121b542be9dfd`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 7.6 MB (7578842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9005a53f6c0a99e09d71101e29f5c22e4fb5f3bb43ecdf4b47f7750e807352bb`  
		Last Modified: Wed, 15 Apr 2026 20:25:45 GMT  
		Size: 178.1 MB (178091526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0448445e755843df85d2e503a2b4c3ee49cbc788cb3de60d5bf1dfcced704798`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6d60b7dec12989e85afe46c49b0aa33d18800737f00d87020988db7148295c`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8665be37a8553d3f13ece05b0cf49e22eb2e9455b7447cf49cb53059a6b133fe`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1540e63cc82538954ccd9d0a1695c3c9fa68873706490d9ed380a28ed18a0208`  
		Last Modified: Wed, 15 Apr 2026 20:25:38 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26a21419191f0f324aaabb8f0f963618b08a2426d1fbb9ccfbb4f4d2d1f04c6`  
		Last Modified: Wed, 15 Apr 2026 20:25:38 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:90be94b8fc0796e4fea05b3b48d4bda0b0baa136c307a7d4d255f9a3f5da086d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501facc23c4a02ef653bc8d51a2534485afa726194e086656743cf5684fd89e9`

```dockerfile
```

-	Layers:
	-	`sha256:bd776e838bd7ab1d599ecc3b7ece2a507838a4b50672db6c416b470aa9a469d4`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.21`

```console
$ docker pull clickhouse@sha256:d08ef7e5c4e63e0eaeef28931d4bdb14b3a137b145f051ad0b412ad4177bd3d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.21` - linux; amd64

```console
$ docker pull clickhouse@sha256:2c6a916521b336977982b4526b201da46c479186ba03ae22f4fefe4e5990908a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229199945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32184c254de283578043bd8bc12b1c9a24075169b6dd1b0f5e262fa644e532f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:09 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:09 GMT
ARG VERSION=25.8.21.7
# Wed, 15 Apr 2026 20:25:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:34 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:34 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:34 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca91fdcc0abda421ad01afd641f21a86e5aedeec12704c8ae17b0bc8abd7f3c4`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 7.6 MB (7599174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173eda4e42a7e303295d09d787f66b4ce7a1f60c576a2404868f44a9c3e3c358`  
		Last Modified: Wed, 15 Apr 2026 20:26:00 GMT  
		Size: 191.0 MB (190994252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f3de34b92920b427cfa577d6818c1ae2bc52bb4b740990b77ad22016a30795`  
		Last Modified: Wed, 15 Apr 2026 20:25:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ae818cf2593b3e9bd21cad01067297e382eea2ca6143c10b05d56c9d724b50`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bea843884b2f8c1fcfe1ca39e3df84e54d79dc529165b5521a79a405375ee8`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4de75be46064f44a11544c9a6c919e3d2767f7fc913fd8a665d22320cb3f918`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783dcf9319aa518231cffdb24c1cc4b4ad6968b63244f90e96f0664cca6c348b`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.21` - unknown; unknown

```console
$ docker pull clickhouse@sha256:aab03bc7e9d1359d915ea6ece8e208a609ee87e8cce9e20c2193d2d0ae707654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c466a2b1fcbaf9dcaf14221e19dfd68453432d74535cfd1e94a3a1766e89a6b`

```dockerfile
```

-	Layers:
	-	`sha256:195eeef671b51cd00fe7b76beabcde45643575fc10fb7e3e943b3adc6d97fa51`  
		Last Modified: Wed, 15 Apr 2026 20:25:55 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.21` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b12416eec37ab984ab05721df17517f8977a83022b52a1dbab8d565f3b36cbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214146936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28cd611923331ff8cc025f7c7aff0e78f37eaf4635661c1ec086dff61a66dcb6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:43 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:43 GMT
ARG VERSION=25.8.21.7
# Wed, 15 Apr 2026 20:24:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:17 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:17 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24772a921c5468694e52f31ef95c6f3838b85ba2d0b281dde1f121b542be9dfd`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 7.6 MB (7578842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9005a53f6c0a99e09d71101e29f5c22e4fb5f3bb43ecdf4b47f7750e807352bb`  
		Last Modified: Wed, 15 Apr 2026 20:25:45 GMT  
		Size: 178.1 MB (178091526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0448445e755843df85d2e503a2b4c3ee49cbc788cb3de60d5bf1dfcced704798`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6d60b7dec12989e85afe46c49b0aa33d18800737f00d87020988db7148295c`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8665be37a8553d3f13ece05b0cf49e22eb2e9455b7447cf49cb53059a6b133fe`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1540e63cc82538954ccd9d0a1695c3c9fa68873706490d9ed380a28ed18a0208`  
		Last Modified: Wed, 15 Apr 2026 20:25:38 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26a21419191f0f324aaabb8f0f963618b08a2426d1fbb9ccfbb4f4d2d1f04c6`  
		Last Modified: Wed, 15 Apr 2026 20:25:38 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.21` - unknown; unknown

```console
$ docker pull clickhouse@sha256:90be94b8fc0796e4fea05b3b48d4bda0b0baa136c307a7d4d255f9a3f5da086d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501facc23c4a02ef653bc8d51a2534485afa726194e086656743cf5684fd89e9`

```dockerfile
```

-	Layers:
	-	`sha256:bd776e838bd7ab1d599ecc3b7ece2a507838a4b50672db6c416b470aa9a469d4`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.21-jammy`

```console
$ docker pull clickhouse@sha256:d08ef7e5c4e63e0eaeef28931d4bdb14b3a137b145f051ad0b412ad4177bd3d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.21-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:2c6a916521b336977982b4526b201da46c479186ba03ae22f4fefe4e5990908a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229199945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32184c254de283578043bd8bc12b1c9a24075169b6dd1b0f5e262fa644e532f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:09 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:09 GMT
ARG VERSION=25.8.21.7
# Wed, 15 Apr 2026 20:25:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:34 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:34 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:34 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca91fdcc0abda421ad01afd641f21a86e5aedeec12704c8ae17b0bc8abd7f3c4`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 7.6 MB (7599174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173eda4e42a7e303295d09d787f66b4ce7a1f60c576a2404868f44a9c3e3c358`  
		Last Modified: Wed, 15 Apr 2026 20:26:00 GMT  
		Size: 191.0 MB (190994252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f3de34b92920b427cfa577d6818c1ae2bc52bb4b740990b77ad22016a30795`  
		Last Modified: Wed, 15 Apr 2026 20:25:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ae818cf2593b3e9bd21cad01067297e382eea2ca6143c10b05d56c9d724b50`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bea843884b2f8c1fcfe1ca39e3df84e54d79dc529165b5521a79a405375ee8`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4de75be46064f44a11544c9a6c919e3d2767f7fc913fd8a665d22320cb3f918`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783dcf9319aa518231cffdb24c1cc4b4ad6968b63244f90e96f0664cca6c348b`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.21-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:aab03bc7e9d1359d915ea6ece8e208a609ee87e8cce9e20c2193d2d0ae707654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c466a2b1fcbaf9dcaf14221e19dfd68453432d74535cfd1e94a3a1766e89a6b`

```dockerfile
```

-	Layers:
	-	`sha256:195eeef671b51cd00fe7b76beabcde45643575fc10fb7e3e943b3adc6d97fa51`  
		Last Modified: Wed, 15 Apr 2026 20:25:55 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.21-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b12416eec37ab984ab05721df17517f8977a83022b52a1dbab8d565f3b36cbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214146936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28cd611923331ff8cc025f7c7aff0e78f37eaf4635661c1ec086dff61a66dcb6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:43 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:43 GMT
ARG VERSION=25.8.21.7
# Wed, 15 Apr 2026 20:24:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:17 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:17 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24772a921c5468694e52f31ef95c6f3838b85ba2d0b281dde1f121b542be9dfd`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 7.6 MB (7578842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9005a53f6c0a99e09d71101e29f5c22e4fb5f3bb43ecdf4b47f7750e807352bb`  
		Last Modified: Wed, 15 Apr 2026 20:25:45 GMT  
		Size: 178.1 MB (178091526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0448445e755843df85d2e503a2b4c3ee49cbc788cb3de60d5bf1dfcced704798`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6d60b7dec12989e85afe46c49b0aa33d18800737f00d87020988db7148295c`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8665be37a8553d3f13ece05b0cf49e22eb2e9455b7447cf49cb53059a6b133fe`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1540e63cc82538954ccd9d0a1695c3c9fa68873706490d9ed380a28ed18a0208`  
		Last Modified: Wed, 15 Apr 2026 20:25:38 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26a21419191f0f324aaabb8f0f963618b08a2426d1fbb9ccfbb4f4d2d1f04c6`  
		Last Modified: Wed, 15 Apr 2026 20:25:38 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.21-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:90be94b8fc0796e4fea05b3b48d4bda0b0baa136c307a7d4d255f9a3f5da086d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501facc23c4a02ef653bc8d51a2534485afa726194e086656743cf5684fd89e9`

```dockerfile
```

-	Layers:
	-	`sha256:bd776e838bd7ab1d599ecc3b7ece2a507838a4b50672db6c416b470aa9a469d4`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.21.7`

```console
$ docker pull clickhouse@sha256:d08ef7e5c4e63e0eaeef28931d4bdb14b3a137b145f051ad0b412ad4177bd3d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.21.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:2c6a916521b336977982b4526b201da46c479186ba03ae22f4fefe4e5990908a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229199945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32184c254de283578043bd8bc12b1c9a24075169b6dd1b0f5e262fa644e532f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:09 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:09 GMT
ARG VERSION=25.8.21.7
# Wed, 15 Apr 2026 20:25:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:34 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:34 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:34 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca91fdcc0abda421ad01afd641f21a86e5aedeec12704c8ae17b0bc8abd7f3c4`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 7.6 MB (7599174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173eda4e42a7e303295d09d787f66b4ce7a1f60c576a2404868f44a9c3e3c358`  
		Last Modified: Wed, 15 Apr 2026 20:26:00 GMT  
		Size: 191.0 MB (190994252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f3de34b92920b427cfa577d6818c1ae2bc52bb4b740990b77ad22016a30795`  
		Last Modified: Wed, 15 Apr 2026 20:25:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ae818cf2593b3e9bd21cad01067297e382eea2ca6143c10b05d56c9d724b50`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bea843884b2f8c1fcfe1ca39e3df84e54d79dc529165b5521a79a405375ee8`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4de75be46064f44a11544c9a6c919e3d2767f7fc913fd8a665d22320cb3f918`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783dcf9319aa518231cffdb24c1cc4b4ad6968b63244f90e96f0664cca6c348b`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.21.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:aab03bc7e9d1359d915ea6ece8e208a609ee87e8cce9e20c2193d2d0ae707654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c466a2b1fcbaf9dcaf14221e19dfd68453432d74535cfd1e94a3a1766e89a6b`

```dockerfile
```

-	Layers:
	-	`sha256:195eeef671b51cd00fe7b76beabcde45643575fc10fb7e3e943b3adc6d97fa51`  
		Last Modified: Wed, 15 Apr 2026 20:25:55 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.21.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b12416eec37ab984ab05721df17517f8977a83022b52a1dbab8d565f3b36cbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214146936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28cd611923331ff8cc025f7c7aff0e78f37eaf4635661c1ec086dff61a66dcb6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:43 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:43 GMT
ARG VERSION=25.8.21.7
# Wed, 15 Apr 2026 20:24:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:17 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:17 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24772a921c5468694e52f31ef95c6f3838b85ba2d0b281dde1f121b542be9dfd`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 7.6 MB (7578842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9005a53f6c0a99e09d71101e29f5c22e4fb5f3bb43ecdf4b47f7750e807352bb`  
		Last Modified: Wed, 15 Apr 2026 20:25:45 GMT  
		Size: 178.1 MB (178091526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0448445e755843df85d2e503a2b4c3ee49cbc788cb3de60d5bf1dfcced704798`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6d60b7dec12989e85afe46c49b0aa33d18800737f00d87020988db7148295c`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8665be37a8553d3f13ece05b0cf49e22eb2e9455b7447cf49cb53059a6b133fe`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1540e63cc82538954ccd9d0a1695c3c9fa68873706490d9ed380a28ed18a0208`  
		Last Modified: Wed, 15 Apr 2026 20:25:38 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26a21419191f0f324aaabb8f0f963618b08a2426d1fbb9ccfbb4f4d2d1f04c6`  
		Last Modified: Wed, 15 Apr 2026 20:25:38 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.21.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:90be94b8fc0796e4fea05b3b48d4bda0b0baa136c307a7d4d255f9a3f5da086d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501facc23c4a02ef653bc8d51a2534485afa726194e086656743cf5684fd89e9`

```dockerfile
```

-	Layers:
	-	`sha256:bd776e838bd7ab1d599ecc3b7ece2a507838a4b50672db6c416b470aa9a469d4`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.21.7-jammy`

```console
$ docker pull clickhouse@sha256:d08ef7e5c4e63e0eaeef28931d4bdb14b3a137b145f051ad0b412ad4177bd3d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.21.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:2c6a916521b336977982b4526b201da46c479186ba03ae22f4fefe4e5990908a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.2 MB (229199945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32184c254de283578043bd8bc12b1c9a24075169b6dd1b0f5e262fa644e532f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:09 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:09 GMT
ARG VERSION=25.8.21.7
# Wed, 15 Apr 2026 20:25:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:34 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:34 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:34 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca91fdcc0abda421ad01afd641f21a86e5aedeec12704c8ae17b0bc8abd7f3c4`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 7.6 MB (7599174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:173eda4e42a7e303295d09d787f66b4ce7a1f60c576a2404868f44a9c3e3c358`  
		Last Modified: Wed, 15 Apr 2026 20:26:00 GMT  
		Size: 191.0 MB (190994252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f3de34b92920b427cfa577d6818c1ae2bc52bb4b740990b77ad22016a30795`  
		Last Modified: Wed, 15 Apr 2026 20:25:55 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ae818cf2593b3e9bd21cad01067297e382eea2ca6143c10b05d56c9d724b50`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92bea843884b2f8c1fcfe1ca39e3df84e54d79dc529165b5521a79a405375ee8`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4de75be46064f44a11544c9a6c919e3d2767f7fc913fd8a665d22320cb3f918`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783dcf9319aa518231cffdb24c1cc4b4ad6968b63244f90e96f0664cca6c348b`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.21.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:aab03bc7e9d1359d915ea6ece8e208a609ee87e8cce9e20c2193d2d0ae707654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c466a2b1fcbaf9dcaf14221e19dfd68453432d74535cfd1e94a3a1766e89a6b`

```dockerfile
```

-	Layers:
	-	`sha256:195eeef671b51cd00fe7b76beabcde45643575fc10fb7e3e943b3adc6d97fa51`  
		Last Modified: Wed, 15 Apr 2026 20:25:55 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.21.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b12416eec37ab984ab05721df17517f8977a83022b52a1dbab8d565f3b36cbf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214146936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28cd611923331ff8cc025f7c7aff0e78f37eaf4635661c1ec086dff61a66dcb6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:43 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:43 GMT
ARG VERSION=25.8.21.7
# Wed, 15 Apr 2026 20:24:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:17 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.21.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:17 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24772a921c5468694e52f31ef95c6f3838b85ba2d0b281dde1f121b542be9dfd`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 7.6 MB (7578842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9005a53f6c0a99e09d71101e29f5c22e4fb5f3bb43ecdf4b47f7750e807352bb`  
		Last Modified: Wed, 15 Apr 2026 20:25:45 GMT  
		Size: 178.1 MB (178091526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0448445e755843df85d2e503a2b4c3ee49cbc788cb3de60d5bf1dfcced704798`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6d60b7dec12989e85afe46c49b0aa33d18800737f00d87020988db7148295c`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8665be37a8553d3f13ece05b0cf49e22eb2e9455b7447cf49cb53059a6b133fe`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1540e63cc82538954ccd9d0a1695c3c9fa68873706490d9ed380a28ed18a0208`  
		Last Modified: Wed, 15 Apr 2026 20:25:38 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b26a21419191f0f324aaabb8f0f963618b08a2426d1fbb9ccfbb4f4d2d1f04c6`  
		Last Modified: Wed, 15 Apr 2026 20:25:38 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.21.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:90be94b8fc0796e4fea05b3b48d4bda0b0baa136c307a7d4d255f9a3f5da086d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501facc23c4a02ef653bc8d51a2534485afa726194e086656743cf5684fd89e9`

```dockerfile
```

-	Layers:
	-	`sha256:bd776e838bd7ab1d599ecc3b7ece2a507838a4b50672db6c416b470aa9a469d4`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1`

```console
$ docker pull clickhouse@sha256:b46c3764bc520f836221d76a84b8412ab2f78dd117d2c98553206eef9ec9da94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:6df13de58ebf4dc3bfdc5e0abf3e492a36a8ad9fc1a21eb7d60b4128de328012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246285490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9783bac407cd594193577bef53695f2d23bc53fa207b40b629df173e3b19c14`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:03 GMT
ARG VERSION=26.1.7.13
# Wed, 15 Apr 2026 20:25:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:28 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:28 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972a6bf52f449bb35b593e34a77e1880b8e4affd66c8eb1d2e23cf64df538791`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 7.6 MB (7599161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786209235e874153335905df71e44a788e5e4123686fc9a4c31ad737d64e7d8`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 208.1 MB (208079781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd67376d31452720f67da7ab40ace125580e795aa828abf53a5724c23e1c80b`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe034f3553aa9ff5b44df08a41ee0f5aa49f16018a187d1393f75a934ede767`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1079d0bb47474d4eecf65c13217880033b3119d76c9dd260fe21c898f12546`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88835bbb7f8a531d2bf0bcdde771283b3a2e6aed28305e8994ab6d0faaf9ff9`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c97bd5f8e08990c3d880fbb8d495d1d26fbb9fa50fc433b5ebc4bae20487823`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f4ae8d5a03523b2c8db6394fa965e9e629e9be89c29112abd1a9cf78f048505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374f16996195479955b19538b3afe5432fa6c41d8003a05a74238cdf4eacbed7`

```dockerfile
```

-	Layers:
	-	`sha256:c260b81417924bc619d2333313eeca2b21e4bef65679396e1d1bf58674a4ffeb`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2047d755e70b10047be729059ccb96bf561436435675a663583653741f825e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228497155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce0ea1acbb77d7a57f131594631f01b9eaedb95f6af8bd1e360cd1039018122`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:40 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:40 GMT
ARG VERSION=26.1.7.13
# Wed, 15 Apr 2026 20:24:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:13 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:13 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:14 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8685268bd03ac954a83aa619fe2f8f20abe7cf820edf00ff9a91896076d7c60`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 7.6 MB (7578960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e3723d2e35a0730a68f1556d402a25415c555a94031d4e030d27a12910f791`  
		Last Modified: Wed, 15 Apr 2026 20:25:40 GMT  
		Size: 192.4 MB (192441604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814cc82a247d03560eed9c65572bbfd41b5f121a0c478af32f843acbea0e9b27`  
		Last Modified: Wed, 15 Apr 2026 20:25:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3da08941316046b11481f5e6fba8487ce6adcde027704e065e73925ecb7b48`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdf0f49199396b855bbc082e6bada6358991b680281824b221f45eb043546d3`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f18e4d5364cc29eb72bcc6f10e5a5dbbef14cac453e9560b34b98c59f8ceb0`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d016fa1ea1defff36c407eea0792e14fd472b690e4427163455d9d3fee26b9`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e810a5069e1786b1e2df8441ff07327b6edc30a52b6d82973667f5d2d3495c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5175c43b35ee332936bd1f2bd2aaf4d503b299205252855dd3e73e08417161bf`

```dockerfile
```

-	Layers:
	-	`sha256:efef047b3f0e44a465d190142e8aecbdb2aa1477ff465cf7bb2a537670d5f69b`  
		Last Modified: Wed, 15 Apr 2026 20:25:35 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1-jammy`

```console
$ docker pull clickhouse@sha256:b46c3764bc520f836221d76a84b8412ab2f78dd117d2c98553206eef9ec9da94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:6df13de58ebf4dc3bfdc5e0abf3e492a36a8ad9fc1a21eb7d60b4128de328012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246285490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9783bac407cd594193577bef53695f2d23bc53fa207b40b629df173e3b19c14`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:03 GMT
ARG VERSION=26.1.7.13
# Wed, 15 Apr 2026 20:25:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:28 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:28 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972a6bf52f449bb35b593e34a77e1880b8e4affd66c8eb1d2e23cf64df538791`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 7.6 MB (7599161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786209235e874153335905df71e44a788e5e4123686fc9a4c31ad737d64e7d8`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 208.1 MB (208079781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd67376d31452720f67da7ab40ace125580e795aa828abf53a5724c23e1c80b`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe034f3553aa9ff5b44df08a41ee0f5aa49f16018a187d1393f75a934ede767`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1079d0bb47474d4eecf65c13217880033b3119d76c9dd260fe21c898f12546`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88835bbb7f8a531d2bf0bcdde771283b3a2e6aed28305e8994ab6d0faaf9ff9`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c97bd5f8e08990c3d880fbb8d495d1d26fbb9fa50fc433b5ebc4bae20487823`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f4ae8d5a03523b2c8db6394fa965e9e629e9be89c29112abd1a9cf78f048505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374f16996195479955b19538b3afe5432fa6c41d8003a05a74238cdf4eacbed7`

```dockerfile
```

-	Layers:
	-	`sha256:c260b81417924bc619d2333313eeca2b21e4bef65679396e1d1bf58674a4ffeb`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2047d755e70b10047be729059ccb96bf561436435675a663583653741f825e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228497155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce0ea1acbb77d7a57f131594631f01b9eaedb95f6af8bd1e360cd1039018122`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:40 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:40 GMT
ARG VERSION=26.1.7.13
# Wed, 15 Apr 2026 20:24:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:13 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:13 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:14 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8685268bd03ac954a83aa619fe2f8f20abe7cf820edf00ff9a91896076d7c60`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 7.6 MB (7578960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e3723d2e35a0730a68f1556d402a25415c555a94031d4e030d27a12910f791`  
		Last Modified: Wed, 15 Apr 2026 20:25:40 GMT  
		Size: 192.4 MB (192441604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814cc82a247d03560eed9c65572bbfd41b5f121a0c478af32f843acbea0e9b27`  
		Last Modified: Wed, 15 Apr 2026 20:25:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3da08941316046b11481f5e6fba8487ce6adcde027704e065e73925ecb7b48`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdf0f49199396b855bbc082e6bada6358991b680281824b221f45eb043546d3`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f18e4d5364cc29eb72bcc6f10e5a5dbbef14cac453e9560b34b98c59f8ceb0`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d016fa1ea1defff36c407eea0792e14fd472b690e4427163455d9d3fee26b9`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e810a5069e1786b1e2df8441ff07327b6edc30a52b6d82973667f5d2d3495c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5175c43b35ee332936bd1f2bd2aaf4d503b299205252855dd3e73e08417161bf`

```dockerfile
```

-	Layers:
	-	`sha256:efef047b3f0e44a465d190142e8aecbdb2aa1477ff465cf7bb2a537670d5f69b`  
		Last Modified: Wed, 15 Apr 2026 20:25:35 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.7`

```console
$ docker pull clickhouse@sha256:b46c3764bc520f836221d76a84b8412ab2f78dd117d2c98553206eef9ec9da94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:6df13de58ebf4dc3bfdc5e0abf3e492a36a8ad9fc1a21eb7d60b4128de328012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246285490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9783bac407cd594193577bef53695f2d23bc53fa207b40b629df173e3b19c14`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:03 GMT
ARG VERSION=26.1.7.13
# Wed, 15 Apr 2026 20:25:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:28 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:28 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972a6bf52f449bb35b593e34a77e1880b8e4affd66c8eb1d2e23cf64df538791`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 7.6 MB (7599161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786209235e874153335905df71e44a788e5e4123686fc9a4c31ad737d64e7d8`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 208.1 MB (208079781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd67376d31452720f67da7ab40ace125580e795aa828abf53a5724c23e1c80b`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe034f3553aa9ff5b44df08a41ee0f5aa49f16018a187d1393f75a934ede767`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1079d0bb47474d4eecf65c13217880033b3119d76c9dd260fe21c898f12546`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88835bbb7f8a531d2bf0bcdde771283b3a2e6aed28305e8994ab6d0faaf9ff9`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c97bd5f8e08990c3d880fbb8d495d1d26fbb9fa50fc433b5ebc4bae20487823`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f4ae8d5a03523b2c8db6394fa965e9e629e9be89c29112abd1a9cf78f048505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374f16996195479955b19538b3afe5432fa6c41d8003a05a74238cdf4eacbed7`

```dockerfile
```

-	Layers:
	-	`sha256:c260b81417924bc619d2333313eeca2b21e4bef65679396e1d1bf58674a4ffeb`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2047d755e70b10047be729059ccb96bf561436435675a663583653741f825e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228497155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce0ea1acbb77d7a57f131594631f01b9eaedb95f6af8bd1e360cd1039018122`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:40 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:40 GMT
ARG VERSION=26.1.7.13
# Wed, 15 Apr 2026 20:24:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:13 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:13 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:14 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8685268bd03ac954a83aa619fe2f8f20abe7cf820edf00ff9a91896076d7c60`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 7.6 MB (7578960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e3723d2e35a0730a68f1556d402a25415c555a94031d4e030d27a12910f791`  
		Last Modified: Wed, 15 Apr 2026 20:25:40 GMT  
		Size: 192.4 MB (192441604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814cc82a247d03560eed9c65572bbfd41b5f121a0c478af32f843acbea0e9b27`  
		Last Modified: Wed, 15 Apr 2026 20:25:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3da08941316046b11481f5e6fba8487ce6adcde027704e065e73925ecb7b48`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdf0f49199396b855bbc082e6bada6358991b680281824b221f45eb043546d3`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f18e4d5364cc29eb72bcc6f10e5a5dbbef14cac453e9560b34b98c59f8ceb0`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d016fa1ea1defff36c407eea0792e14fd472b690e4427163455d9d3fee26b9`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e810a5069e1786b1e2df8441ff07327b6edc30a52b6d82973667f5d2d3495c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5175c43b35ee332936bd1f2bd2aaf4d503b299205252855dd3e73e08417161bf`

```dockerfile
```

-	Layers:
	-	`sha256:efef047b3f0e44a465d190142e8aecbdb2aa1477ff465cf7bb2a537670d5f69b`  
		Last Modified: Wed, 15 Apr 2026 20:25:35 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.7-jammy`

```console
$ docker pull clickhouse@sha256:b46c3764bc520f836221d76a84b8412ab2f78dd117d2c98553206eef9ec9da94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:6df13de58ebf4dc3bfdc5e0abf3e492a36a8ad9fc1a21eb7d60b4128de328012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246285490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9783bac407cd594193577bef53695f2d23bc53fa207b40b629df173e3b19c14`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:03 GMT
ARG VERSION=26.1.7.13
# Wed, 15 Apr 2026 20:25:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:28 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:28 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972a6bf52f449bb35b593e34a77e1880b8e4affd66c8eb1d2e23cf64df538791`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 7.6 MB (7599161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786209235e874153335905df71e44a788e5e4123686fc9a4c31ad737d64e7d8`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 208.1 MB (208079781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd67376d31452720f67da7ab40ace125580e795aa828abf53a5724c23e1c80b`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe034f3553aa9ff5b44df08a41ee0f5aa49f16018a187d1393f75a934ede767`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1079d0bb47474d4eecf65c13217880033b3119d76c9dd260fe21c898f12546`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88835bbb7f8a531d2bf0bcdde771283b3a2e6aed28305e8994ab6d0faaf9ff9`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c97bd5f8e08990c3d880fbb8d495d1d26fbb9fa50fc433b5ebc4bae20487823`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f4ae8d5a03523b2c8db6394fa965e9e629e9be89c29112abd1a9cf78f048505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374f16996195479955b19538b3afe5432fa6c41d8003a05a74238cdf4eacbed7`

```dockerfile
```

-	Layers:
	-	`sha256:c260b81417924bc619d2333313eeca2b21e4bef65679396e1d1bf58674a4ffeb`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2047d755e70b10047be729059ccb96bf561436435675a663583653741f825e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228497155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce0ea1acbb77d7a57f131594631f01b9eaedb95f6af8bd1e360cd1039018122`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:40 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:40 GMT
ARG VERSION=26.1.7.13
# Wed, 15 Apr 2026 20:24:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:13 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:13 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:14 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8685268bd03ac954a83aa619fe2f8f20abe7cf820edf00ff9a91896076d7c60`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 7.6 MB (7578960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e3723d2e35a0730a68f1556d402a25415c555a94031d4e030d27a12910f791`  
		Last Modified: Wed, 15 Apr 2026 20:25:40 GMT  
		Size: 192.4 MB (192441604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814cc82a247d03560eed9c65572bbfd41b5f121a0c478af32f843acbea0e9b27`  
		Last Modified: Wed, 15 Apr 2026 20:25:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3da08941316046b11481f5e6fba8487ce6adcde027704e065e73925ecb7b48`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdf0f49199396b855bbc082e6bada6358991b680281824b221f45eb043546d3`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f18e4d5364cc29eb72bcc6f10e5a5dbbef14cac453e9560b34b98c59f8ceb0`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d016fa1ea1defff36c407eea0792e14fd472b690e4427163455d9d3fee26b9`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e810a5069e1786b1e2df8441ff07327b6edc30a52b6d82973667f5d2d3495c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5175c43b35ee332936bd1f2bd2aaf4d503b299205252855dd3e73e08417161bf`

```dockerfile
```

-	Layers:
	-	`sha256:efef047b3f0e44a465d190142e8aecbdb2aa1477ff465cf7bb2a537670d5f69b`  
		Last Modified: Wed, 15 Apr 2026 20:25:35 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.7.13`

```console
$ docker pull clickhouse@sha256:b46c3764bc520f836221d76a84b8412ab2f78dd117d2c98553206eef9ec9da94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.7.13` - linux; amd64

```console
$ docker pull clickhouse@sha256:6df13de58ebf4dc3bfdc5e0abf3e492a36a8ad9fc1a21eb7d60b4128de328012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246285490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9783bac407cd594193577bef53695f2d23bc53fa207b40b629df173e3b19c14`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:03 GMT
ARG VERSION=26.1.7.13
# Wed, 15 Apr 2026 20:25:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:28 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:28 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972a6bf52f449bb35b593e34a77e1880b8e4affd66c8eb1d2e23cf64df538791`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 7.6 MB (7599161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786209235e874153335905df71e44a788e5e4123686fc9a4c31ad737d64e7d8`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 208.1 MB (208079781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd67376d31452720f67da7ab40ace125580e795aa828abf53a5724c23e1c80b`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe034f3553aa9ff5b44df08a41ee0f5aa49f16018a187d1393f75a934ede767`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1079d0bb47474d4eecf65c13217880033b3119d76c9dd260fe21c898f12546`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88835bbb7f8a531d2bf0bcdde771283b3a2e6aed28305e8994ab6d0faaf9ff9`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c97bd5f8e08990c3d880fbb8d495d1d26fbb9fa50fc433b5ebc4bae20487823`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.7.13` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f4ae8d5a03523b2c8db6394fa965e9e629e9be89c29112abd1a9cf78f048505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374f16996195479955b19538b3afe5432fa6c41d8003a05a74238cdf4eacbed7`

```dockerfile
```

-	Layers:
	-	`sha256:c260b81417924bc619d2333313eeca2b21e4bef65679396e1d1bf58674a4ffeb`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.7.13` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2047d755e70b10047be729059ccb96bf561436435675a663583653741f825e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228497155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce0ea1acbb77d7a57f131594631f01b9eaedb95f6af8bd1e360cd1039018122`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:40 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:40 GMT
ARG VERSION=26.1.7.13
# Wed, 15 Apr 2026 20:24:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:13 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:13 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:14 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8685268bd03ac954a83aa619fe2f8f20abe7cf820edf00ff9a91896076d7c60`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 7.6 MB (7578960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e3723d2e35a0730a68f1556d402a25415c555a94031d4e030d27a12910f791`  
		Last Modified: Wed, 15 Apr 2026 20:25:40 GMT  
		Size: 192.4 MB (192441604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814cc82a247d03560eed9c65572bbfd41b5f121a0c478af32f843acbea0e9b27`  
		Last Modified: Wed, 15 Apr 2026 20:25:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3da08941316046b11481f5e6fba8487ce6adcde027704e065e73925ecb7b48`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdf0f49199396b855bbc082e6bada6358991b680281824b221f45eb043546d3`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f18e4d5364cc29eb72bcc6f10e5a5dbbef14cac453e9560b34b98c59f8ceb0`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d016fa1ea1defff36c407eea0792e14fd472b690e4427163455d9d3fee26b9`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.7.13` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e810a5069e1786b1e2df8441ff07327b6edc30a52b6d82973667f5d2d3495c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5175c43b35ee332936bd1f2bd2aaf4d503b299205252855dd3e73e08417161bf`

```dockerfile
```

-	Layers:
	-	`sha256:efef047b3f0e44a465d190142e8aecbdb2aa1477ff465cf7bb2a537670d5f69b`  
		Last Modified: Wed, 15 Apr 2026 20:25:35 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.7.13-jammy`

```console
$ docker pull clickhouse@sha256:b46c3764bc520f836221d76a84b8412ab2f78dd117d2c98553206eef9ec9da94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.7.13-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:6df13de58ebf4dc3bfdc5e0abf3e492a36a8ad9fc1a21eb7d60b4128de328012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246285490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9783bac407cd594193577bef53695f2d23bc53fa207b40b629df173e3b19c14`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:03 GMT
ARG VERSION=26.1.7.13
# Wed, 15 Apr 2026 20:25:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:28 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:28 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972a6bf52f449bb35b593e34a77e1880b8e4affd66c8eb1d2e23cf64df538791`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 7.6 MB (7599161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5786209235e874153335905df71e44a788e5e4123686fc9a4c31ad737d64e7d8`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 208.1 MB (208079781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd67376d31452720f67da7ab40ace125580e795aa828abf53a5724c23e1c80b`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe034f3553aa9ff5b44df08a41ee0f5aa49f16018a187d1393f75a934ede767`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1079d0bb47474d4eecf65c13217880033b3119d76c9dd260fe21c898f12546`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88835bbb7f8a531d2bf0bcdde771283b3a2e6aed28305e8994ab6d0faaf9ff9`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c97bd5f8e08990c3d880fbb8d495d1d26fbb9fa50fc433b5ebc4bae20487823`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.7.13-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f4ae8d5a03523b2c8db6394fa965e9e629e9be89c29112abd1a9cf78f048505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374f16996195479955b19538b3afe5432fa6c41d8003a05a74238cdf4eacbed7`

```dockerfile
```

-	Layers:
	-	`sha256:c260b81417924bc619d2333313eeca2b21e4bef65679396e1d1bf58674a4ffeb`  
		Last Modified: Wed, 15 Apr 2026 20:25:50 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.7.13-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2047d755e70b10047be729059ccb96bf561436435675a663583653741f825e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228497155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ce0ea1acbb77d7a57f131594631f01b9eaedb95f6af8bd1e360cd1039018122`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:40 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:40 GMT
ARG VERSION=26.1.7.13
# Wed, 15 Apr 2026 20:24:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:13 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:13 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.7.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:14 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8685268bd03ac954a83aa619fe2f8f20abe7cf820edf00ff9a91896076d7c60`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 7.6 MB (7578960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e3723d2e35a0730a68f1556d402a25415c555a94031d4e030d27a12910f791`  
		Last Modified: Wed, 15 Apr 2026 20:25:40 GMT  
		Size: 192.4 MB (192441604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814cc82a247d03560eed9c65572bbfd41b5f121a0c478af32f843acbea0e9b27`  
		Last Modified: Wed, 15 Apr 2026 20:25:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3da08941316046b11481f5e6fba8487ce6adcde027704e065e73925ecb7b48`  
		Last Modified: Wed, 15 Apr 2026 20:25:36 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bdf0f49199396b855bbc082e6bada6358991b680281824b221f45eb043546d3`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f18e4d5364cc29eb72bcc6f10e5a5dbbef14cac453e9560b34b98c59f8ceb0`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d016fa1ea1defff36c407eea0792e14fd472b690e4427163455d9d3fee26b9`  
		Last Modified: Wed, 15 Apr 2026 20:25:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.7.13-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e810a5069e1786b1e2df8441ff07327b6edc30a52b6d82973667f5d2d3495c99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5175c43b35ee332936bd1f2bd2aaf4d503b299205252855dd3e73e08417161bf`

```dockerfile
```

-	Layers:
	-	`sha256:efef047b3f0e44a465d190142e8aecbdb2aa1477ff465cf7bb2a537670d5f69b`  
		Last Modified: Wed, 15 Apr 2026 20:25:35 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2`

```console
$ docker pull clickhouse@sha256:b68dc5edfc42aab4a2612f7f01e15031bb4251b69a4b235cfb357654c59bd155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:fb965781d98117efd983d8d49e62fbd9b01ec7e8505b7dab473bc8729d796bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253861950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0f12e59d57f5001084b18ee1625d2c20552f5ad189dfb32868ef7775691175`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:04 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:04 GMT
ARG VERSION=26.2.7.17
# Wed, 15 Apr 2026 20:25:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:31 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:31 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:31 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1029c477964f660003af9c7f57ac02b440c54bb1dca48eb947df8710dcf6f4`  
		Last Modified: Wed, 15 Apr 2026 20:25:58 GMT  
		Size: 7.6 MB (7599184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890a2da3ad05dda7d7364721f606155188b2b84ca22419a55caeaebc2d0ddec4`  
		Last Modified: Wed, 15 Apr 2026 20:26:03 GMT  
		Size: 215.7 MB (215656218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ed0152941a28f79776ffb4d8186b9a0c16111d6c5f59fc16af5d052228be9`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f033c2b0fd835cae33e458881e6ac4bb8723ef40bb32e8a0f77845b9bae671`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92ef9d9a3356b8499665e2b198bb6a34d1273c00a8bb7922adbc4282e5da9da`  
		Last Modified: Wed, 15 Apr 2026 20:25:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e8464bc497f3f61c69742ef93d89fc41c028a04880117fdcfcc4574d15ac7d`  
		Last Modified: Wed, 15 Apr 2026 20:25:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c97bd5f8e08990c3d880fbb8d495d1d26fbb9fa50fc433b5ebc4bae20487823`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:83d3f8fad165aaf382ad4926aa62a640e49fa127e721f63cb0b2a1897e195583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8178081eb8f8a24a8cf7b3572976da4f9323b718a38906099b3835e8f1f7d381`

```dockerfile
```

-	Layers:
	-	`sha256:554663692d031d9f5ed67e28305bfe307af8346726c32ddc22d0c79a64ed4d2e`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:531345467d17415bd136828158948139cc0b794adf030e63ec8484f66c616d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237425113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b196ec333f355da2d3f33ff2dd41354df17d3bc0043fc89ad4873e8f812f5e79`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:27 GMT
ARG VERSION=26.2.7.17
# Wed, 15 Apr 2026 20:24:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:03 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:03 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5566d979569df320165bfca160e10b1e75ee9d249e5f84c4889c1f0c44db0622`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 7.6 MB (7578954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e96efb956a992993b7c35d33d86935b5bdec269083c0ed090413f5d55d1ee4d`  
		Last Modified: Wed, 15 Apr 2026 20:25:30 GMT  
		Size: 201.4 MB (201369568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920d7ed9085b16b0ed2ef4c95e0ed567c1bf00f4ad9aac05b7eca7e03ba907ae`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6b3b3b6329eee184e2be0bdee84a63f668706cb0d2c89df75563a687a03338`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ac7bcb8008b23320acdab54a71930ce32bf845f35a5aa68d4bc43421d1da51`  
		Last Modified: Wed, 15 Apr 2026 20:25:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b848e209f118a8aca5f59a8803dde3c298bedf9d077f31da76a19f816d65a7ce`  
		Last Modified: Wed, 15 Apr 2026 20:25:26 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897f7a260882224afe17e976ef2d5ab166e190a02fff30e9d28493fe92cb8bf3`  
		Last Modified: Wed, 15 Apr 2026 20:25:27 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a9fcdd60016e6eca050ae90f0d1e044501064ed79fc853118c1c3a140862be6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbb8cc87c4090c6b760a8c8f9e62a1f30b7bbc5ad9da290c7a89d5adfd24883`

```dockerfile
```

-	Layers:
	-	`sha256:905e51f3175d1d8fa9fb179d72b9255dc43c1613a91daf8f90d52003fe2a4bed`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2-jammy`

```console
$ docker pull clickhouse@sha256:b68dc5edfc42aab4a2612f7f01e15031bb4251b69a4b235cfb357654c59bd155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:fb965781d98117efd983d8d49e62fbd9b01ec7e8505b7dab473bc8729d796bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253861950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0f12e59d57f5001084b18ee1625d2c20552f5ad189dfb32868ef7775691175`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:04 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:04 GMT
ARG VERSION=26.2.7.17
# Wed, 15 Apr 2026 20:25:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:31 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:31 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:31 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1029c477964f660003af9c7f57ac02b440c54bb1dca48eb947df8710dcf6f4`  
		Last Modified: Wed, 15 Apr 2026 20:25:58 GMT  
		Size: 7.6 MB (7599184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890a2da3ad05dda7d7364721f606155188b2b84ca22419a55caeaebc2d0ddec4`  
		Last Modified: Wed, 15 Apr 2026 20:26:03 GMT  
		Size: 215.7 MB (215656218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ed0152941a28f79776ffb4d8186b9a0c16111d6c5f59fc16af5d052228be9`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f033c2b0fd835cae33e458881e6ac4bb8723ef40bb32e8a0f77845b9bae671`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92ef9d9a3356b8499665e2b198bb6a34d1273c00a8bb7922adbc4282e5da9da`  
		Last Modified: Wed, 15 Apr 2026 20:25:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e8464bc497f3f61c69742ef93d89fc41c028a04880117fdcfcc4574d15ac7d`  
		Last Modified: Wed, 15 Apr 2026 20:25:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c97bd5f8e08990c3d880fbb8d495d1d26fbb9fa50fc433b5ebc4bae20487823`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:83d3f8fad165aaf382ad4926aa62a640e49fa127e721f63cb0b2a1897e195583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8178081eb8f8a24a8cf7b3572976da4f9323b718a38906099b3835e8f1f7d381`

```dockerfile
```

-	Layers:
	-	`sha256:554663692d031d9f5ed67e28305bfe307af8346726c32ddc22d0c79a64ed4d2e`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:531345467d17415bd136828158948139cc0b794adf030e63ec8484f66c616d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237425113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b196ec333f355da2d3f33ff2dd41354df17d3bc0043fc89ad4873e8f812f5e79`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:27 GMT
ARG VERSION=26.2.7.17
# Wed, 15 Apr 2026 20:24:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:03 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:03 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5566d979569df320165bfca160e10b1e75ee9d249e5f84c4889c1f0c44db0622`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 7.6 MB (7578954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e96efb956a992993b7c35d33d86935b5bdec269083c0ed090413f5d55d1ee4d`  
		Last Modified: Wed, 15 Apr 2026 20:25:30 GMT  
		Size: 201.4 MB (201369568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920d7ed9085b16b0ed2ef4c95e0ed567c1bf00f4ad9aac05b7eca7e03ba907ae`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6b3b3b6329eee184e2be0bdee84a63f668706cb0d2c89df75563a687a03338`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ac7bcb8008b23320acdab54a71930ce32bf845f35a5aa68d4bc43421d1da51`  
		Last Modified: Wed, 15 Apr 2026 20:25:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b848e209f118a8aca5f59a8803dde3c298bedf9d077f31da76a19f816d65a7ce`  
		Last Modified: Wed, 15 Apr 2026 20:25:26 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897f7a260882224afe17e976ef2d5ab166e190a02fff30e9d28493fe92cb8bf3`  
		Last Modified: Wed, 15 Apr 2026 20:25:27 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a9fcdd60016e6eca050ae90f0d1e044501064ed79fc853118c1c3a140862be6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbb8cc87c4090c6b760a8c8f9e62a1f30b7bbc5ad9da290c7a89d5adfd24883`

```dockerfile
```

-	Layers:
	-	`sha256:905e51f3175d1d8fa9fb179d72b9255dc43c1613a91daf8f90d52003fe2a4bed`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.7`

```console
$ docker pull clickhouse@sha256:b68dc5edfc42aab4a2612f7f01e15031bb4251b69a4b235cfb357654c59bd155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:fb965781d98117efd983d8d49e62fbd9b01ec7e8505b7dab473bc8729d796bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253861950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0f12e59d57f5001084b18ee1625d2c20552f5ad189dfb32868ef7775691175`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:04 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:04 GMT
ARG VERSION=26.2.7.17
# Wed, 15 Apr 2026 20:25:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:31 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:31 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:31 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1029c477964f660003af9c7f57ac02b440c54bb1dca48eb947df8710dcf6f4`  
		Last Modified: Wed, 15 Apr 2026 20:25:58 GMT  
		Size: 7.6 MB (7599184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890a2da3ad05dda7d7364721f606155188b2b84ca22419a55caeaebc2d0ddec4`  
		Last Modified: Wed, 15 Apr 2026 20:26:03 GMT  
		Size: 215.7 MB (215656218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ed0152941a28f79776ffb4d8186b9a0c16111d6c5f59fc16af5d052228be9`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f033c2b0fd835cae33e458881e6ac4bb8723ef40bb32e8a0f77845b9bae671`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92ef9d9a3356b8499665e2b198bb6a34d1273c00a8bb7922adbc4282e5da9da`  
		Last Modified: Wed, 15 Apr 2026 20:25:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e8464bc497f3f61c69742ef93d89fc41c028a04880117fdcfcc4574d15ac7d`  
		Last Modified: Wed, 15 Apr 2026 20:25:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c97bd5f8e08990c3d880fbb8d495d1d26fbb9fa50fc433b5ebc4bae20487823`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:83d3f8fad165aaf382ad4926aa62a640e49fa127e721f63cb0b2a1897e195583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8178081eb8f8a24a8cf7b3572976da4f9323b718a38906099b3835e8f1f7d381`

```dockerfile
```

-	Layers:
	-	`sha256:554663692d031d9f5ed67e28305bfe307af8346726c32ddc22d0c79a64ed4d2e`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:531345467d17415bd136828158948139cc0b794adf030e63ec8484f66c616d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237425113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b196ec333f355da2d3f33ff2dd41354df17d3bc0043fc89ad4873e8f812f5e79`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:27 GMT
ARG VERSION=26.2.7.17
# Wed, 15 Apr 2026 20:24:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:03 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:03 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5566d979569df320165bfca160e10b1e75ee9d249e5f84c4889c1f0c44db0622`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 7.6 MB (7578954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e96efb956a992993b7c35d33d86935b5bdec269083c0ed090413f5d55d1ee4d`  
		Last Modified: Wed, 15 Apr 2026 20:25:30 GMT  
		Size: 201.4 MB (201369568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920d7ed9085b16b0ed2ef4c95e0ed567c1bf00f4ad9aac05b7eca7e03ba907ae`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6b3b3b6329eee184e2be0bdee84a63f668706cb0d2c89df75563a687a03338`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ac7bcb8008b23320acdab54a71930ce32bf845f35a5aa68d4bc43421d1da51`  
		Last Modified: Wed, 15 Apr 2026 20:25:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b848e209f118a8aca5f59a8803dde3c298bedf9d077f31da76a19f816d65a7ce`  
		Last Modified: Wed, 15 Apr 2026 20:25:26 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897f7a260882224afe17e976ef2d5ab166e190a02fff30e9d28493fe92cb8bf3`  
		Last Modified: Wed, 15 Apr 2026 20:25:27 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a9fcdd60016e6eca050ae90f0d1e044501064ed79fc853118c1c3a140862be6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbb8cc87c4090c6b760a8c8f9e62a1f30b7bbc5ad9da290c7a89d5adfd24883`

```dockerfile
```

-	Layers:
	-	`sha256:905e51f3175d1d8fa9fb179d72b9255dc43c1613a91daf8f90d52003fe2a4bed`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.7-jammy`

```console
$ docker pull clickhouse@sha256:b68dc5edfc42aab4a2612f7f01e15031bb4251b69a4b235cfb357654c59bd155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:fb965781d98117efd983d8d49e62fbd9b01ec7e8505b7dab473bc8729d796bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253861950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0f12e59d57f5001084b18ee1625d2c20552f5ad189dfb32868ef7775691175`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:04 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:04 GMT
ARG VERSION=26.2.7.17
# Wed, 15 Apr 2026 20:25:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:31 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:31 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:31 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1029c477964f660003af9c7f57ac02b440c54bb1dca48eb947df8710dcf6f4`  
		Last Modified: Wed, 15 Apr 2026 20:25:58 GMT  
		Size: 7.6 MB (7599184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890a2da3ad05dda7d7364721f606155188b2b84ca22419a55caeaebc2d0ddec4`  
		Last Modified: Wed, 15 Apr 2026 20:26:03 GMT  
		Size: 215.7 MB (215656218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ed0152941a28f79776ffb4d8186b9a0c16111d6c5f59fc16af5d052228be9`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f033c2b0fd835cae33e458881e6ac4bb8723ef40bb32e8a0f77845b9bae671`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92ef9d9a3356b8499665e2b198bb6a34d1273c00a8bb7922adbc4282e5da9da`  
		Last Modified: Wed, 15 Apr 2026 20:25:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e8464bc497f3f61c69742ef93d89fc41c028a04880117fdcfcc4574d15ac7d`  
		Last Modified: Wed, 15 Apr 2026 20:25:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c97bd5f8e08990c3d880fbb8d495d1d26fbb9fa50fc433b5ebc4bae20487823`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:83d3f8fad165aaf382ad4926aa62a640e49fa127e721f63cb0b2a1897e195583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8178081eb8f8a24a8cf7b3572976da4f9323b718a38906099b3835e8f1f7d381`

```dockerfile
```

-	Layers:
	-	`sha256:554663692d031d9f5ed67e28305bfe307af8346726c32ddc22d0c79a64ed4d2e`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:531345467d17415bd136828158948139cc0b794adf030e63ec8484f66c616d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237425113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b196ec333f355da2d3f33ff2dd41354df17d3bc0043fc89ad4873e8f812f5e79`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:27 GMT
ARG VERSION=26.2.7.17
# Wed, 15 Apr 2026 20:24:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:03 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:03 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5566d979569df320165bfca160e10b1e75ee9d249e5f84c4889c1f0c44db0622`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 7.6 MB (7578954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e96efb956a992993b7c35d33d86935b5bdec269083c0ed090413f5d55d1ee4d`  
		Last Modified: Wed, 15 Apr 2026 20:25:30 GMT  
		Size: 201.4 MB (201369568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920d7ed9085b16b0ed2ef4c95e0ed567c1bf00f4ad9aac05b7eca7e03ba907ae`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6b3b3b6329eee184e2be0bdee84a63f668706cb0d2c89df75563a687a03338`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ac7bcb8008b23320acdab54a71930ce32bf845f35a5aa68d4bc43421d1da51`  
		Last Modified: Wed, 15 Apr 2026 20:25:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b848e209f118a8aca5f59a8803dde3c298bedf9d077f31da76a19f816d65a7ce`  
		Last Modified: Wed, 15 Apr 2026 20:25:26 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897f7a260882224afe17e976ef2d5ab166e190a02fff30e9d28493fe92cb8bf3`  
		Last Modified: Wed, 15 Apr 2026 20:25:27 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a9fcdd60016e6eca050ae90f0d1e044501064ed79fc853118c1c3a140862be6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbb8cc87c4090c6b760a8c8f9e62a1f30b7bbc5ad9da290c7a89d5adfd24883`

```dockerfile
```

-	Layers:
	-	`sha256:905e51f3175d1d8fa9fb179d72b9255dc43c1613a91daf8f90d52003fe2a4bed`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.7.17`

```console
$ docker pull clickhouse@sha256:b68dc5edfc42aab4a2612f7f01e15031bb4251b69a4b235cfb357654c59bd155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.7.17` - linux; amd64

```console
$ docker pull clickhouse@sha256:fb965781d98117efd983d8d49e62fbd9b01ec7e8505b7dab473bc8729d796bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253861950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0f12e59d57f5001084b18ee1625d2c20552f5ad189dfb32868ef7775691175`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:04 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:04 GMT
ARG VERSION=26.2.7.17
# Wed, 15 Apr 2026 20:25:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:31 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:31 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:31 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1029c477964f660003af9c7f57ac02b440c54bb1dca48eb947df8710dcf6f4`  
		Last Modified: Wed, 15 Apr 2026 20:25:58 GMT  
		Size: 7.6 MB (7599184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890a2da3ad05dda7d7364721f606155188b2b84ca22419a55caeaebc2d0ddec4`  
		Last Modified: Wed, 15 Apr 2026 20:26:03 GMT  
		Size: 215.7 MB (215656218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ed0152941a28f79776ffb4d8186b9a0c16111d6c5f59fc16af5d052228be9`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f033c2b0fd835cae33e458881e6ac4bb8723ef40bb32e8a0f77845b9bae671`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92ef9d9a3356b8499665e2b198bb6a34d1273c00a8bb7922adbc4282e5da9da`  
		Last Modified: Wed, 15 Apr 2026 20:25:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e8464bc497f3f61c69742ef93d89fc41c028a04880117fdcfcc4574d15ac7d`  
		Last Modified: Wed, 15 Apr 2026 20:25:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c97bd5f8e08990c3d880fbb8d495d1d26fbb9fa50fc433b5ebc4bae20487823`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.7.17` - unknown; unknown

```console
$ docker pull clickhouse@sha256:83d3f8fad165aaf382ad4926aa62a640e49fa127e721f63cb0b2a1897e195583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8178081eb8f8a24a8cf7b3572976da4f9323b718a38906099b3835e8f1f7d381`

```dockerfile
```

-	Layers:
	-	`sha256:554663692d031d9f5ed67e28305bfe307af8346726c32ddc22d0c79a64ed4d2e`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.7.17` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:531345467d17415bd136828158948139cc0b794adf030e63ec8484f66c616d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237425113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b196ec333f355da2d3f33ff2dd41354df17d3bc0043fc89ad4873e8f812f5e79`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:27 GMT
ARG VERSION=26.2.7.17
# Wed, 15 Apr 2026 20:24:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:03 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:03 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5566d979569df320165bfca160e10b1e75ee9d249e5f84c4889c1f0c44db0622`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 7.6 MB (7578954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e96efb956a992993b7c35d33d86935b5bdec269083c0ed090413f5d55d1ee4d`  
		Last Modified: Wed, 15 Apr 2026 20:25:30 GMT  
		Size: 201.4 MB (201369568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920d7ed9085b16b0ed2ef4c95e0ed567c1bf00f4ad9aac05b7eca7e03ba907ae`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6b3b3b6329eee184e2be0bdee84a63f668706cb0d2c89df75563a687a03338`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ac7bcb8008b23320acdab54a71930ce32bf845f35a5aa68d4bc43421d1da51`  
		Last Modified: Wed, 15 Apr 2026 20:25:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b848e209f118a8aca5f59a8803dde3c298bedf9d077f31da76a19f816d65a7ce`  
		Last Modified: Wed, 15 Apr 2026 20:25:26 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897f7a260882224afe17e976ef2d5ab166e190a02fff30e9d28493fe92cb8bf3`  
		Last Modified: Wed, 15 Apr 2026 20:25:27 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.7.17` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a9fcdd60016e6eca050ae90f0d1e044501064ed79fc853118c1c3a140862be6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbb8cc87c4090c6b760a8c8f9e62a1f30b7bbc5ad9da290c7a89d5adfd24883`

```dockerfile
```

-	Layers:
	-	`sha256:905e51f3175d1d8fa9fb179d72b9255dc43c1613a91daf8f90d52003fe2a4bed`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.7.17-jammy`

```console
$ docker pull clickhouse@sha256:b68dc5edfc42aab4a2612f7f01e15031bb4251b69a4b235cfb357654c59bd155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.7.17-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:fb965781d98117efd983d8d49e62fbd9b01ec7e8505b7dab473bc8729d796bf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.9 MB (253861950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0f12e59d57f5001084b18ee1625d2c20552f5ad189dfb32868ef7775691175`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:25:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:25:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:25:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:25:04 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:25:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:25:04 GMT
ARG VERSION=26.2.7.17
# Wed, 15 Apr 2026 20:25:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:30 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:31 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:31 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:31 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:31 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1029c477964f660003af9c7f57ac02b440c54bb1dca48eb947df8710dcf6f4`  
		Last Modified: Wed, 15 Apr 2026 20:25:58 GMT  
		Size: 7.6 MB (7599184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890a2da3ad05dda7d7364721f606155188b2b84ca22419a55caeaebc2d0ddec4`  
		Last Modified: Wed, 15 Apr 2026 20:26:03 GMT  
		Size: 215.7 MB (215656218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865ed0152941a28f79776ffb4d8186b9a0c16111d6c5f59fc16af5d052228be9`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f033c2b0fd835cae33e458881e6ac4bb8723ef40bb32e8a0f77845b9bae671`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92ef9d9a3356b8499665e2b198bb6a34d1273c00a8bb7922adbc4282e5da9da`  
		Last Modified: Wed, 15 Apr 2026 20:25:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e8464bc497f3f61c69742ef93d89fc41c028a04880117fdcfcc4574d15ac7d`  
		Last Modified: Wed, 15 Apr 2026 20:25:59 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c97bd5f8e08990c3d880fbb8d495d1d26fbb9fa50fc433b5ebc4bae20487823`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.7.17-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:83d3f8fad165aaf382ad4926aa62a640e49fa127e721f63cb0b2a1897e195583
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8178081eb8f8a24a8cf7b3572976da4f9323b718a38906099b3835e8f1f7d381`

```dockerfile
```

-	Layers:
	-	`sha256:554663692d031d9f5ed67e28305bfe307af8346726c32ddc22d0c79a64ed4d2e`  
		Last Modified: Wed, 15 Apr 2026 20:25:57 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.7.17-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:531345467d17415bd136828158948139cc0b794adf030e63ec8484f66c616d66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237425113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b196ec333f355da2d3f33ff2dd41354df17d3bc0043fc89ad4873e8f812f5e79`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:27 GMT
ARG VERSION=26.2.7.17
# Wed, 15 Apr 2026 20:24:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:03 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.7.17 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:03 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5566d979569df320165bfca160e10b1e75ee9d249e5f84c4889c1f0c44db0622`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 7.6 MB (7578954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e96efb956a992993b7c35d33d86935b5bdec269083c0ed090413f5d55d1ee4d`  
		Last Modified: Wed, 15 Apr 2026 20:25:30 GMT  
		Size: 201.4 MB (201369568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920d7ed9085b16b0ed2ef4c95e0ed567c1bf00f4ad9aac05b7eca7e03ba907ae`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e6b3b3b6329eee184e2be0bdee84a63f668706cb0d2c89df75563a687a03338`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ac7bcb8008b23320acdab54a71930ce32bf845f35a5aa68d4bc43421d1da51`  
		Last Modified: Wed, 15 Apr 2026 20:25:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b848e209f118a8aca5f59a8803dde3c298bedf9d077f31da76a19f816d65a7ce`  
		Last Modified: Wed, 15 Apr 2026 20:25:26 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:897f7a260882224afe17e976ef2d5ab166e190a02fff30e9d28493fe92cb8bf3`  
		Last Modified: Wed, 15 Apr 2026 20:25:27 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.7.17-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a9fcdd60016e6eca050ae90f0d1e044501064ed79fc853118c1c3a140862be6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dbb8cc87c4090c6b760a8c8f9e62a1f30b7bbc5ad9da290c7a89d5adfd24883`

```dockerfile
```

-	Layers:
	-	`sha256:905e51f3175d1d8fa9fb179d72b9255dc43c1613a91daf8f90d52003fe2a4bed`  
		Last Modified: Wed, 15 Apr 2026 20:25:25 GMT  
		Size: 25.6 KB (25606 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3`

```console
$ docker pull clickhouse@sha256:c98cd387ebbe177d46681821b27a1e70c1fe06e1f2e614f7d953abe79d7a731f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:b6560b27e33b96278382599b66d8d2161a41fd89a154a82935cf495d7d814a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731ab736c36671e82c6606f0f3cd6b1af362be69de49f50d3cd78b495e388173`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:54 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:27 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:28 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184db4edfe1ecda9d7215a133c852cacb50bc407aef7a7041782a744574d4b4f`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 7.6 MB (7599209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892804c99da2eb22d3a17ce667ae9df934a12df98c874481aae68a597e9f66bd`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 224.2 MB (224151118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f4de0f0f46f6f39ae2deff043679d084ad2d69213869c918723b39cce01c2c`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f989ec8d387b332193da1e00fd0219fc0287aafb1789dcb489939d7a22b8c2dc`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1079d0bb47474d4eecf65c13217880033b3119d76c9dd260fe21c898f12546`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6085e23d131e694e8d87883a8257ca8cea4c2bc5a011f39a84dbe55ad0df91c9`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f043a76906fc5ee30c1b204882a6a0d2c326b58f0cef679847c4f28733a367`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee585e6338cc9e831cf594930343cc74ed783781e191b24fb36a55656b5e9ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8b125abbd8cd0a8776985a16888b0db86eb754038d90ce2b626fb72e96f0eb`

```dockerfile
```

-	Layers:
	-	`sha256:8c004776de518b87a4ddfcd0b26be044f43460f47b1866f2b8618631e18bb4f6`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 26.6 KB (26640 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9fd1bd16df149727211c238dd9a7fcece83fe63f826d22709ba69d9fb297d0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd7ff9be253700a19fd344c5f17055f0230b4909adfac55fbb51078467e9c47`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:27 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:24:59 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:24:59 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:24:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:24:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4aac67ee3eff26f92253505feda9b1944c36f19ece5f4de8cab901a8b24a817`  
		Last Modified: Wed, 15 Apr 2026 20:25:22 GMT  
		Size: 7.6 MB (7578964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb8b6007d81605ea73351c9c18da03ae1dbfcacd6938a4d8f86c2431aaaf1b1`  
		Last Modified: Wed, 15 Apr 2026 20:25:31 GMT  
		Size: 208.5 MB (208543446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b4c70e779a1595652f22320645f6628a1a8612833e85d3544d96e4f6d9c4b9`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b5f1555dfec5bbb8889a60a1121ecad64701357955b18d8b14cb24473518d4`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb34b8e136acb52e509be954109bb21a4832c55f1ae93ed21752ba2593931018`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9f2fdd0451e012c59d398bb90a0632e09b1ac8ee23a086dc21c960b96aef4a`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd43e2436b53031ecfbb5f2e1adb61fb5fb0a6a87862ed771b70d6fd06f53e`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 3.6 KB (3633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e4d5b486057d0352b9a406a8ce4e6822f5a23de2e27bd42a977c1a977b992cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08973f705a2acccad2809a52e3e37fa822366d9348e367a21267bf345e47ff39`

```dockerfile
```

-	Layers:
	-	`sha256:28c4b5d9d9a00c68cbcb4825ecd2e93d67f709f905f1db60c8536b6cd86f3f3c`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 26.9 KB (26876 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3-jammy`

```console
$ docker pull clickhouse@sha256:c98cd387ebbe177d46681821b27a1e70c1fe06e1f2e614f7d953abe79d7a731f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:b6560b27e33b96278382599b66d8d2161a41fd89a154a82935cf495d7d814a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731ab736c36671e82c6606f0f3cd6b1af362be69de49f50d3cd78b495e388173`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:54 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:27 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:28 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184db4edfe1ecda9d7215a133c852cacb50bc407aef7a7041782a744574d4b4f`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 7.6 MB (7599209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892804c99da2eb22d3a17ce667ae9df934a12df98c874481aae68a597e9f66bd`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 224.2 MB (224151118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f4de0f0f46f6f39ae2deff043679d084ad2d69213869c918723b39cce01c2c`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f989ec8d387b332193da1e00fd0219fc0287aafb1789dcb489939d7a22b8c2dc`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1079d0bb47474d4eecf65c13217880033b3119d76c9dd260fe21c898f12546`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6085e23d131e694e8d87883a8257ca8cea4c2bc5a011f39a84dbe55ad0df91c9`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f043a76906fc5ee30c1b204882a6a0d2c326b58f0cef679847c4f28733a367`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee585e6338cc9e831cf594930343cc74ed783781e191b24fb36a55656b5e9ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8b125abbd8cd0a8776985a16888b0db86eb754038d90ce2b626fb72e96f0eb`

```dockerfile
```

-	Layers:
	-	`sha256:8c004776de518b87a4ddfcd0b26be044f43460f47b1866f2b8618631e18bb4f6`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 26.6 KB (26640 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9fd1bd16df149727211c238dd9a7fcece83fe63f826d22709ba69d9fb297d0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd7ff9be253700a19fd344c5f17055f0230b4909adfac55fbb51078467e9c47`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:27 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:24:59 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:24:59 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:24:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:24:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4aac67ee3eff26f92253505feda9b1944c36f19ece5f4de8cab901a8b24a817`  
		Last Modified: Wed, 15 Apr 2026 20:25:22 GMT  
		Size: 7.6 MB (7578964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb8b6007d81605ea73351c9c18da03ae1dbfcacd6938a4d8f86c2431aaaf1b1`  
		Last Modified: Wed, 15 Apr 2026 20:25:31 GMT  
		Size: 208.5 MB (208543446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b4c70e779a1595652f22320645f6628a1a8612833e85d3544d96e4f6d9c4b9`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b5f1555dfec5bbb8889a60a1121ecad64701357955b18d8b14cb24473518d4`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb34b8e136acb52e509be954109bb21a4832c55f1ae93ed21752ba2593931018`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9f2fdd0451e012c59d398bb90a0632e09b1ac8ee23a086dc21c960b96aef4a`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd43e2436b53031ecfbb5f2e1adb61fb5fb0a6a87862ed771b70d6fd06f53e`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 3.6 KB (3633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e4d5b486057d0352b9a406a8ce4e6822f5a23de2e27bd42a977c1a977b992cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08973f705a2acccad2809a52e3e37fa822366d9348e367a21267bf345e47ff39`

```dockerfile
```

-	Layers:
	-	`sha256:28c4b5d9d9a00c68cbcb4825ecd2e93d67f709f905f1db60c8536b6cd86f3f3c`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 26.9 KB (26876 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.3`

```console
$ docker pull clickhouse@sha256:c98cd387ebbe177d46681821b27a1e70c1fe06e1f2e614f7d953abe79d7a731f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:b6560b27e33b96278382599b66d8d2161a41fd89a154a82935cf495d7d814a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731ab736c36671e82c6606f0f3cd6b1af362be69de49f50d3cd78b495e388173`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:54 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:27 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:28 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184db4edfe1ecda9d7215a133c852cacb50bc407aef7a7041782a744574d4b4f`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 7.6 MB (7599209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892804c99da2eb22d3a17ce667ae9df934a12df98c874481aae68a597e9f66bd`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 224.2 MB (224151118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f4de0f0f46f6f39ae2deff043679d084ad2d69213869c918723b39cce01c2c`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f989ec8d387b332193da1e00fd0219fc0287aafb1789dcb489939d7a22b8c2dc`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1079d0bb47474d4eecf65c13217880033b3119d76c9dd260fe21c898f12546`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6085e23d131e694e8d87883a8257ca8cea4c2bc5a011f39a84dbe55ad0df91c9`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f043a76906fc5ee30c1b204882a6a0d2c326b58f0cef679847c4f28733a367`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee585e6338cc9e831cf594930343cc74ed783781e191b24fb36a55656b5e9ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8b125abbd8cd0a8776985a16888b0db86eb754038d90ce2b626fb72e96f0eb`

```dockerfile
```

-	Layers:
	-	`sha256:8c004776de518b87a4ddfcd0b26be044f43460f47b1866f2b8618631e18bb4f6`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 26.6 KB (26640 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9fd1bd16df149727211c238dd9a7fcece83fe63f826d22709ba69d9fb297d0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd7ff9be253700a19fd344c5f17055f0230b4909adfac55fbb51078467e9c47`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:27 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:24:59 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:24:59 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:24:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:24:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4aac67ee3eff26f92253505feda9b1944c36f19ece5f4de8cab901a8b24a817`  
		Last Modified: Wed, 15 Apr 2026 20:25:22 GMT  
		Size: 7.6 MB (7578964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb8b6007d81605ea73351c9c18da03ae1dbfcacd6938a4d8f86c2431aaaf1b1`  
		Last Modified: Wed, 15 Apr 2026 20:25:31 GMT  
		Size: 208.5 MB (208543446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b4c70e779a1595652f22320645f6628a1a8612833e85d3544d96e4f6d9c4b9`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b5f1555dfec5bbb8889a60a1121ecad64701357955b18d8b14cb24473518d4`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb34b8e136acb52e509be954109bb21a4832c55f1ae93ed21752ba2593931018`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9f2fdd0451e012c59d398bb90a0632e09b1ac8ee23a086dc21c960b96aef4a`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd43e2436b53031ecfbb5f2e1adb61fb5fb0a6a87862ed771b70d6fd06f53e`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 3.6 KB (3633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e4d5b486057d0352b9a406a8ce4e6822f5a23de2e27bd42a977c1a977b992cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08973f705a2acccad2809a52e3e37fa822366d9348e367a21267bf345e47ff39`

```dockerfile
```

-	Layers:
	-	`sha256:28c4b5d9d9a00c68cbcb4825ecd2e93d67f709f905f1db60c8536b6cd86f3f3c`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 26.9 KB (26876 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.3-jammy`

```console
$ docker pull clickhouse@sha256:c98cd387ebbe177d46681821b27a1e70c1fe06e1f2e614f7d953abe79d7a731f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:b6560b27e33b96278382599b66d8d2161a41fd89a154a82935cf495d7d814a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731ab736c36671e82c6606f0f3cd6b1af362be69de49f50d3cd78b495e388173`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:54 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:27 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:28 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184db4edfe1ecda9d7215a133c852cacb50bc407aef7a7041782a744574d4b4f`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 7.6 MB (7599209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892804c99da2eb22d3a17ce667ae9df934a12df98c874481aae68a597e9f66bd`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 224.2 MB (224151118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f4de0f0f46f6f39ae2deff043679d084ad2d69213869c918723b39cce01c2c`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f989ec8d387b332193da1e00fd0219fc0287aafb1789dcb489939d7a22b8c2dc`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1079d0bb47474d4eecf65c13217880033b3119d76c9dd260fe21c898f12546`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6085e23d131e694e8d87883a8257ca8cea4c2bc5a011f39a84dbe55ad0df91c9`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f043a76906fc5ee30c1b204882a6a0d2c326b58f0cef679847c4f28733a367`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee585e6338cc9e831cf594930343cc74ed783781e191b24fb36a55656b5e9ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8b125abbd8cd0a8776985a16888b0db86eb754038d90ce2b626fb72e96f0eb`

```dockerfile
```

-	Layers:
	-	`sha256:8c004776de518b87a4ddfcd0b26be044f43460f47b1866f2b8618631e18bb4f6`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 26.6 KB (26640 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9fd1bd16df149727211c238dd9a7fcece83fe63f826d22709ba69d9fb297d0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd7ff9be253700a19fd344c5f17055f0230b4909adfac55fbb51078467e9c47`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:27 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:24:59 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:24:59 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:24:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:24:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4aac67ee3eff26f92253505feda9b1944c36f19ece5f4de8cab901a8b24a817`  
		Last Modified: Wed, 15 Apr 2026 20:25:22 GMT  
		Size: 7.6 MB (7578964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb8b6007d81605ea73351c9c18da03ae1dbfcacd6938a4d8f86c2431aaaf1b1`  
		Last Modified: Wed, 15 Apr 2026 20:25:31 GMT  
		Size: 208.5 MB (208543446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b4c70e779a1595652f22320645f6628a1a8612833e85d3544d96e4f6d9c4b9`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b5f1555dfec5bbb8889a60a1121ecad64701357955b18d8b14cb24473518d4`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb34b8e136acb52e509be954109bb21a4832c55f1ae93ed21752ba2593931018`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9f2fdd0451e012c59d398bb90a0632e09b1ac8ee23a086dc21c960b96aef4a`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd43e2436b53031ecfbb5f2e1adb61fb5fb0a6a87862ed771b70d6fd06f53e`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 3.6 KB (3633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e4d5b486057d0352b9a406a8ce4e6822f5a23de2e27bd42a977c1a977b992cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08973f705a2acccad2809a52e3e37fa822366d9348e367a21267bf345e47ff39`

```dockerfile
```

-	Layers:
	-	`sha256:28c4b5d9d9a00c68cbcb4825ecd2e93d67f709f905f1db60c8536b6cd86f3f3c`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 26.9 KB (26876 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.3.20`

```console
$ docker pull clickhouse@sha256:c98cd387ebbe177d46681821b27a1e70c1fe06e1f2e614f7d953abe79d7a731f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.3.20` - linux; amd64

```console
$ docker pull clickhouse@sha256:b6560b27e33b96278382599b66d8d2161a41fd89a154a82935cf495d7d814a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731ab736c36671e82c6606f0f3cd6b1af362be69de49f50d3cd78b495e388173`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:54 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:27 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:28 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184db4edfe1ecda9d7215a133c852cacb50bc407aef7a7041782a744574d4b4f`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 7.6 MB (7599209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892804c99da2eb22d3a17ce667ae9df934a12df98c874481aae68a597e9f66bd`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 224.2 MB (224151118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f4de0f0f46f6f39ae2deff043679d084ad2d69213869c918723b39cce01c2c`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f989ec8d387b332193da1e00fd0219fc0287aafb1789dcb489939d7a22b8c2dc`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1079d0bb47474d4eecf65c13217880033b3119d76c9dd260fe21c898f12546`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6085e23d131e694e8d87883a8257ca8cea4c2bc5a011f39a84dbe55ad0df91c9`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f043a76906fc5ee30c1b204882a6a0d2c326b58f0cef679847c4f28733a367`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.3.20` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee585e6338cc9e831cf594930343cc74ed783781e191b24fb36a55656b5e9ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8b125abbd8cd0a8776985a16888b0db86eb754038d90ce2b626fb72e96f0eb`

```dockerfile
```

-	Layers:
	-	`sha256:8c004776de518b87a4ddfcd0b26be044f43460f47b1866f2b8618631e18bb4f6`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 26.6 KB (26640 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.3.20` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9fd1bd16df149727211c238dd9a7fcece83fe63f826d22709ba69d9fb297d0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd7ff9be253700a19fd344c5f17055f0230b4909adfac55fbb51078467e9c47`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:27 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:24:59 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:24:59 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:24:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:24:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4aac67ee3eff26f92253505feda9b1944c36f19ece5f4de8cab901a8b24a817`  
		Last Modified: Wed, 15 Apr 2026 20:25:22 GMT  
		Size: 7.6 MB (7578964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb8b6007d81605ea73351c9c18da03ae1dbfcacd6938a4d8f86c2431aaaf1b1`  
		Last Modified: Wed, 15 Apr 2026 20:25:31 GMT  
		Size: 208.5 MB (208543446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b4c70e779a1595652f22320645f6628a1a8612833e85d3544d96e4f6d9c4b9`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b5f1555dfec5bbb8889a60a1121ecad64701357955b18d8b14cb24473518d4`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb34b8e136acb52e509be954109bb21a4832c55f1ae93ed21752ba2593931018`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9f2fdd0451e012c59d398bb90a0632e09b1ac8ee23a086dc21c960b96aef4a`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd43e2436b53031ecfbb5f2e1adb61fb5fb0a6a87862ed771b70d6fd06f53e`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 3.6 KB (3633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.3.20` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e4d5b486057d0352b9a406a8ce4e6822f5a23de2e27bd42a977c1a977b992cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08973f705a2acccad2809a52e3e37fa822366d9348e367a21267bf345e47ff39`

```dockerfile
```

-	Layers:
	-	`sha256:28c4b5d9d9a00c68cbcb4825ecd2e93d67f709f905f1db60c8536b6cd86f3f3c`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 26.9 KB (26876 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.3.20-jammy`

```console
$ docker pull clickhouse@sha256:c98cd387ebbe177d46681821b27a1e70c1fe06e1f2e614f7d953abe79d7a731f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.3.20-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:b6560b27e33b96278382599b66d8d2161a41fd89a154a82935cf495d7d814a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731ab736c36671e82c6606f0f3cd6b1af362be69de49f50d3cd78b495e388173`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:54 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:27 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:28 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184db4edfe1ecda9d7215a133c852cacb50bc407aef7a7041782a744574d4b4f`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 7.6 MB (7599209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892804c99da2eb22d3a17ce667ae9df934a12df98c874481aae68a597e9f66bd`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 224.2 MB (224151118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f4de0f0f46f6f39ae2deff043679d084ad2d69213869c918723b39cce01c2c`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f989ec8d387b332193da1e00fd0219fc0287aafb1789dcb489939d7a22b8c2dc`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1079d0bb47474d4eecf65c13217880033b3119d76c9dd260fe21c898f12546`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6085e23d131e694e8d87883a8257ca8cea4c2bc5a011f39a84dbe55ad0df91c9`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f043a76906fc5ee30c1b204882a6a0d2c326b58f0cef679847c4f28733a367`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.3.20-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee585e6338cc9e831cf594930343cc74ed783781e191b24fb36a55656b5e9ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8b125abbd8cd0a8776985a16888b0db86eb754038d90ce2b626fb72e96f0eb`

```dockerfile
```

-	Layers:
	-	`sha256:8c004776de518b87a4ddfcd0b26be044f43460f47b1866f2b8618631e18bb4f6`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 26.6 KB (26640 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.3.20-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9fd1bd16df149727211c238dd9a7fcece83fe63f826d22709ba69d9fb297d0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd7ff9be253700a19fd344c5f17055f0230b4909adfac55fbb51078467e9c47`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:27 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:24:59 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:24:59 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:24:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:24:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4aac67ee3eff26f92253505feda9b1944c36f19ece5f4de8cab901a8b24a817`  
		Last Modified: Wed, 15 Apr 2026 20:25:22 GMT  
		Size: 7.6 MB (7578964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb8b6007d81605ea73351c9c18da03ae1dbfcacd6938a4d8f86c2431aaaf1b1`  
		Last Modified: Wed, 15 Apr 2026 20:25:31 GMT  
		Size: 208.5 MB (208543446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b4c70e779a1595652f22320645f6628a1a8612833e85d3544d96e4f6d9c4b9`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b5f1555dfec5bbb8889a60a1121ecad64701357955b18d8b14cb24473518d4`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb34b8e136acb52e509be954109bb21a4832c55f1ae93ed21752ba2593931018`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9f2fdd0451e012c59d398bb90a0632e09b1ac8ee23a086dc21c960b96aef4a`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd43e2436b53031ecfbb5f2e1adb61fb5fb0a6a87862ed771b70d6fd06f53e`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 3.6 KB (3633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.3.20-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e4d5b486057d0352b9a406a8ce4e6822f5a23de2e27bd42a977c1a977b992cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08973f705a2acccad2809a52e3e37fa822366d9348e367a21267bf345e47ff39`

```dockerfile
```

-	Layers:
	-	`sha256:28c4b5d9d9a00c68cbcb4825ecd2e93d67f709f905f1db60c8536b6cd86f3f3c`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 26.9 KB (26876 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:c98cd387ebbe177d46681821b27a1e70c1fe06e1f2e614f7d953abe79d7a731f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:b6560b27e33b96278382599b66d8d2161a41fd89a154a82935cf495d7d814a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731ab736c36671e82c6606f0f3cd6b1af362be69de49f50d3cd78b495e388173`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:54 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:27 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:28 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184db4edfe1ecda9d7215a133c852cacb50bc407aef7a7041782a744574d4b4f`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 7.6 MB (7599209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892804c99da2eb22d3a17ce667ae9df934a12df98c874481aae68a597e9f66bd`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 224.2 MB (224151118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f4de0f0f46f6f39ae2deff043679d084ad2d69213869c918723b39cce01c2c`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f989ec8d387b332193da1e00fd0219fc0287aafb1789dcb489939d7a22b8c2dc`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1079d0bb47474d4eecf65c13217880033b3119d76c9dd260fe21c898f12546`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6085e23d131e694e8d87883a8257ca8cea4c2bc5a011f39a84dbe55ad0df91c9`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f043a76906fc5ee30c1b204882a6a0d2c326b58f0cef679847c4f28733a367`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee585e6338cc9e831cf594930343cc74ed783781e191b24fb36a55656b5e9ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8b125abbd8cd0a8776985a16888b0db86eb754038d90ce2b626fb72e96f0eb`

```dockerfile
```

-	Layers:
	-	`sha256:8c004776de518b87a4ddfcd0b26be044f43460f47b1866f2b8618631e18bb4f6`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 26.6 KB (26640 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9fd1bd16df149727211c238dd9a7fcece83fe63f826d22709ba69d9fb297d0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd7ff9be253700a19fd344c5f17055f0230b4909adfac55fbb51078467e9c47`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:27 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:24:59 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:24:59 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:24:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:24:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4aac67ee3eff26f92253505feda9b1944c36f19ece5f4de8cab901a8b24a817`  
		Last Modified: Wed, 15 Apr 2026 20:25:22 GMT  
		Size: 7.6 MB (7578964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb8b6007d81605ea73351c9c18da03ae1dbfcacd6938a4d8f86c2431aaaf1b1`  
		Last Modified: Wed, 15 Apr 2026 20:25:31 GMT  
		Size: 208.5 MB (208543446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b4c70e779a1595652f22320645f6628a1a8612833e85d3544d96e4f6d9c4b9`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b5f1555dfec5bbb8889a60a1121ecad64701357955b18d8b14cb24473518d4`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb34b8e136acb52e509be954109bb21a4832c55f1ae93ed21752ba2593931018`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9f2fdd0451e012c59d398bb90a0632e09b1ac8ee23a086dc21c960b96aef4a`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd43e2436b53031ecfbb5f2e1adb61fb5fb0a6a87862ed771b70d6fd06f53e`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 3.6 KB (3633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e4d5b486057d0352b9a406a8ce4e6822f5a23de2e27bd42a977c1a977b992cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08973f705a2acccad2809a52e3e37fa822366d9348e367a21267bf345e47ff39`

```dockerfile
```

-	Layers:
	-	`sha256:28c4b5d9d9a00c68cbcb4825ecd2e93d67f709f905f1db60c8536b6cd86f3f3c`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 26.9 KB (26876 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:c98cd387ebbe177d46681821b27a1e70c1fe06e1f2e614f7d953abe79d7a731f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:b6560b27e33b96278382599b66d8d2161a41fd89a154a82935cf495d7d814a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731ab736c36671e82c6606f0f3cd6b1af362be69de49f50d3cd78b495e388173`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:54 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:27 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:28 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184db4edfe1ecda9d7215a133c852cacb50bc407aef7a7041782a744574d4b4f`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 7.6 MB (7599209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892804c99da2eb22d3a17ce667ae9df934a12df98c874481aae68a597e9f66bd`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 224.2 MB (224151118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f4de0f0f46f6f39ae2deff043679d084ad2d69213869c918723b39cce01c2c`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f989ec8d387b332193da1e00fd0219fc0287aafb1789dcb489939d7a22b8c2dc`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1079d0bb47474d4eecf65c13217880033b3119d76c9dd260fe21c898f12546`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6085e23d131e694e8d87883a8257ca8cea4c2bc5a011f39a84dbe55ad0df91c9`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f043a76906fc5ee30c1b204882a6a0d2c326b58f0cef679847c4f28733a367`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee585e6338cc9e831cf594930343cc74ed783781e191b24fb36a55656b5e9ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8b125abbd8cd0a8776985a16888b0db86eb754038d90ce2b626fb72e96f0eb`

```dockerfile
```

-	Layers:
	-	`sha256:8c004776de518b87a4ddfcd0b26be044f43460f47b1866f2b8618631e18bb4f6`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 26.6 KB (26640 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9fd1bd16df149727211c238dd9a7fcece83fe63f826d22709ba69d9fb297d0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd7ff9be253700a19fd344c5f17055f0230b4909adfac55fbb51078467e9c47`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:27 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:24:59 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:24:59 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:24:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:24:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4aac67ee3eff26f92253505feda9b1944c36f19ece5f4de8cab901a8b24a817`  
		Last Modified: Wed, 15 Apr 2026 20:25:22 GMT  
		Size: 7.6 MB (7578964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb8b6007d81605ea73351c9c18da03ae1dbfcacd6938a4d8f86c2431aaaf1b1`  
		Last Modified: Wed, 15 Apr 2026 20:25:31 GMT  
		Size: 208.5 MB (208543446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b4c70e779a1595652f22320645f6628a1a8612833e85d3544d96e4f6d9c4b9`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b5f1555dfec5bbb8889a60a1121ecad64701357955b18d8b14cb24473518d4`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb34b8e136acb52e509be954109bb21a4832c55f1ae93ed21752ba2593931018`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9f2fdd0451e012c59d398bb90a0632e09b1ac8ee23a086dc21c960b96aef4a`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd43e2436b53031ecfbb5f2e1adb61fb5fb0a6a87862ed771b70d6fd06f53e`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 3.6 KB (3633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e4d5b486057d0352b9a406a8ce4e6822f5a23de2e27bd42a977c1a977b992cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08973f705a2acccad2809a52e3e37fa822366d9348e367a21267bf345e47ff39`

```dockerfile
```

-	Layers:
	-	`sha256:28c4b5d9d9a00c68cbcb4825ecd2e93d67f709f905f1db60c8536b6cd86f3f3c`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 26.9 KB (26876 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:c98cd387ebbe177d46681821b27a1e70c1fe06e1f2e614f7d953abe79d7a731f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:b6560b27e33b96278382599b66d8d2161a41fd89a154a82935cf495d7d814a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731ab736c36671e82c6606f0f3cd6b1af362be69de49f50d3cd78b495e388173`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:54 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:27 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:28 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184db4edfe1ecda9d7215a133c852cacb50bc407aef7a7041782a744574d4b4f`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 7.6 MB (7599209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892804c99da2eb22d3a17ce667ae9df934a12df98c874481aae68a597e9f66bd`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 224.2 MB (224151118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f4de0f0f46f6f39ae2deff043679d084ad2d69213869c918723b39cce01c2c`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f989ec8d387b332193da1e00fd0219fc0287aafb1789dcb489939d7a22b8c2dc`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1079d0bb47474d4eecf65c13217880033b3119d76c9dd260fe21c898f12546`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6085e23d131e694e8d87883a8257ca8cea4c2bc5a011f39a84dbe55ad0df91c9`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f043a76906fc5ee30c1b204882a6a0d2c326b58f0cef679847c4f28733a367`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee585e6338cc9e831cf594930343cc74ed783781e191b24fb36a55656b5e9ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8b125abbd8cd0a8776985a16888b0db86eb754038d90ce2b626fb72e96f0eb`

```dockerfile
```

-	Layers:
	-	`sha256:8c004776de518b87a4ddfcd0b26be044f43460f47b1866f2b8618631e18bb4f6`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 26.6 KB (26640 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9fd1bd16df149727211c238dd9a7fcece83fe63f826d22709ba69d9fb297d0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd7ff9be253700a19fd344c5f17055f0230b4909adfac55fbb51078467e9c47`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:27 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:24:59 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:24:59 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:24:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:24:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4aac67ee3eff26f92253505feda9b1944c36f19ece5f4de8cab901a8b24a817`  
		Last Modified: Wed, 15 Apr 2026 20:25:22 GMT  
		Size: 7.6 MB (7578964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb8b6007d81605ea73351c9c18da03ae1dbfcacd6938a4d8f86c2431aaaf1b1`  
		Last Modified: Wed, 15 Apr 2026 20:25:31 GMT  
		Size: 208.5 MB (208543446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b4c70e779a1595652f22320645f6628a1a8612833e85d3544d96e4f6d9c4b9`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b5f1555dfec5bbb8889a60a1121ecad64701357955b18d8b14cb24473518d4`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb34b8e136acb52e509be954109bb21a4832c55f1ae93ed21752ba2593931018`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9f2fdd0451e012c59d398bb90a0632e09b1ac8ee23a086dc21c960b96aef4a`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd43e2436b53031ecfbb5f2e1adb61fb5fb0a6a87862ed771b70d6fd06f53e`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 3.6 KB (3633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e4d5b486057d0352b9a406a8ce4e6822f5a23de2e27bd42a977c1a977b992cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08973f705a2acccad2809a52e3e37fa822366d9348e367a21267bf345e47ff39`

```dockerfile
```

-	Layers:
	-	`sha256:28c4b5d9d9a00c68cbcb4825ecd2e93d67f709f905f1db60c8536b6cd86f3f3c`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 26.9 KB (26876 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:c98cd387ebbe177d46681821b27a1e70c1fe06e1f2e614f7d953abe79d7a731f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:b6560b27e33b96278382599b66d8d2161a41fd89a154a82935cf495d7d814a9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.4 MB (262356866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731ab736c36671e82c6606f0f3cd6b1af362be69de49f50d3cd78b495e388173`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:47:41 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:47:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:47:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:47:43 GMT
ADD file:da2cd86408d9354e8bd817c8a4b8635a1d788cd20d0d70061ce02a173e8cf902 in / 
# Fri, 10 Apr 2026 09:47:44 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:54 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:54 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:54 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:54 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:54 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:25:27 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:25:27 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:25:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:25:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:25:28 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:25:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:25:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:184db4edfe1ecda9d7215a133c852cacb50bc407aef7a7041782a744574d4b4f`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 7.6 MB (7599209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:892804c99da2eb22d3a17ce667ae9df934a12df98c874481aae68a597e9f66bd`  
		Last Modified: Wed, 15 Apr 2026 20:25:56 GMT  
		Size: 224.2 MB (224151118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f4de0f0f46f6f39ae2deff043679d084ad2d69213869c918723b39cce01c2c`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f989ec8d387b332193da1e00fd0219fc0287aafb1789dcb489939d7a22b8c2dc`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b1079d0bb47474d4eecf65c13217880033b3119d76c9dd260fe21c898f12546`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6085e23d131e694e8d87883a8257ca8cea4c2bc5a011f39a84dbe55ad0df91c9`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f043a76906fc5ee30c1b204882a6a0d2c326b58f0cef679847c4f28733a367`  
		Last Modified: Wed, 15 Apr 2026 20:25:52 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ee585e6338cc9e831cf594930343cc74ed783781e191b24fb36a55656b5e9ef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8b125abbd8cd0a8776985a16888b0db86eb754038d90ce2b626fb72e96f0eb`

```dockerfile
```

-	Layers:
	-	`sha256:8c004776de518b87a4ddfcd0b26be044f43460f47b1866f2b8618631e18bb4f6`  
		Last Modified: Wed, 15 Apr 2026 20:25:51 GMT  
		Size: 26.6 KB (26640 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9fd1bd16df149727211c238dd9a7fcece83fe63f826d22709ba69d9fb297d0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244599001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd7ff9be253700a19fd344c5f17055f0230b4909adfac55fbb51078467e9c47`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Apr 2026 09:49:11 GMT
ARG RELEASE
# Fri, 10 Apr 2026 09:49:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 09:49:11 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 10 Apr 2026 09:49:13 GMT
ADD file:94ca084e2c34d90b4443d18fa6a7d983767fa1575d4bd2c06f6e31adfea270da in / 
# Fri, 10 Apr 2026 09:49:13 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 20:24:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Wed, 15 Apr 2026 20:24:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Wed, 15 Apr 2026 20:24:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPO_CHANNEL=stable
# Wed, 15 Apr 2026 20:24:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Wed, 15 Apr 2026 20:24:27 GMT
ARG VERSION=26.3.3.20
# Wed, 15 Apr 2026 20:24:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
ENV LANG=en_US.UTF-8
# Wed, 15 Apr 2026 20:24:59 GMT
ENV TZ=UTC
# Wed, 15 Apr 2026 20:24:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.3.20 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 15 Apr 2026 20:24:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Wed, 15 Apr 2026 20:24:59 GMT
VOLUME [/var/lib/clickhouse]
# Wed, 15 Apr 2026 20:24:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Wed, 15 Apr 2026 20:24:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4aac67ee3eff26f92253505feda9b1944c36f19ece5f4de8cab901a8b24a817`  
		Last Modified: Wed, 15 Apr 2026 20:25:22 GMT  
		Size: 7.6 MB (7578964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bb8b6007d81605ea73351c9c18da03ae1dbfcacd6938a4d8f86c2431aaaf1b1`  
		Last Modified: Wed, 15 Apr 2026 20:25:31 GMT  
		Size: 208.5 MB (208543446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b4c70e779a1595652f22320645f6628a1a8612833e85d3544d96e4f6d9c4b9`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b5f1555dfec5bbb8889a60a1121ecad64701357955b18d8b14cb24473518d4`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb34b8e136acb52e509be954109bb21a4832c55f1ae93ed21752ba2593931018`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed9f2fdd0451e012c59d398bb90a0632e09b1ac8ee23a086dc21c960b96aef4a`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bd43e2436b53031ecfbb5f2e1adb61fb5fb0a6a87862ed771b70d6fd06f53e`  
		Last Modified: Wed, 15 Apr 2026 20:25:23 GMT  
		Size: 3.6 KB (3633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e4d5b486057d0352b9a406a8ce4e6822f5a23de2e27bd42a977c1a977b992cfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08973f705a2acccad2809a52e3e37fa822366d9348e367a21267bf345e47ff39`

```dockerfile
```

-	Layers:
	-	`sha256:28c4b5d9d9a00c68cbcb4825ecd2e93d67f709f905f1db60c8536b6cd86f3f3c`  
		Last Modified: Wed, 15 Apr 2026 20:25:21 GMT  
		Size: 26.9 KB (26876 bytes)  
		MIME: application/vnd.in-toto+json
