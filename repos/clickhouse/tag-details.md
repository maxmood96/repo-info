<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.22`](#clickhouse25822)
-	[`clickhouse:25.8.22-jammy`](#clickhouse25822-jammy)
-	[`clickhouse:25.8.22.28`](#clickhouse2582228)
-	[`clickhouse:25.8.22.28-jammy`](#clickhouse2582228-jammy)
-	[`clickhouse:26.1`](#clickhouse261)
-	[`clickhouse:26.1-jammy`](#clickhouse261-jammy)
-	[`clickhouse:26.1.11`](#clickhouse26111)
-	[`clickhouse:26.1.11-jammy`](#clickhouse26111-jammy)
-	[`clickhouse:26.1.11.9`](#clickhouse261119)
-	[`clickhouse:26.1.11.9-jammy`](#clickhouse261119-jammy)
-	[`clickhouse:26.2`](#clickhouse262)
-	[`clickhouse:26.2-jammy`](#clickhouse262-jammy)
-	[`clickhouse:26.2.16`](#clickhouse26216)
-	[`clickhouse:26.2.16-jammy`](#clickhouse26216-jammy)
-	[`clickhouse:26.2.16.4`](#clickhouse262164)
-	[`clickhouse:26.2.16.4-jammy`](#clickhouse262164-jammy)
-	[`clickhouse:26.3`](#clickhouse263)
-	[`clickhouse:26.3-jammy`](#clickhouse263-jammy)
-	[`clickhouse:26.3.9`](#clickhouse2639)
-	[`clickhouse:26.3.9-jammy`](#clickhouse2639-jammy)
-	[`clickhouse:26.3.9.8`](#clickhouse26398)
-	[`clickhouse:26.3.9.8-jammy`](#clickhouse26398-jammy)
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

## `clickhouse:25.8.22`

**does not exist** (yet?)

## `clickhouse:25.8.22-jammy`

**does not exist** (yet?)

## `clickhouse:25.8.22.28`

**does not exist** (yet?)

## `clickhouse:25.8.22.28-jammy`

**does not exist** (yet?)

## `clickhouse:26.1`

```console
$ docker pull clickhouse@sha256:8e406990c24b9746b4df002dca6edf475d99144644eeb756daf8a3001850716e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:46728d1226717b46ed6c0fe0c1a34d9e8a3d07ccb9d5525baee06123b46c80e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246133274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6c5ac80f2293c61ad662cb446d2ae3e182485a94b3863acda78202010a9254`
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
# Fri, 17 Apr 2026 22:05:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:46 GMT
ARG VERSION=26.1.11.9
# Fri, 17 Apr 2026 22:05:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:17 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa516dc0cf58e41d3131c5590b68c1c4ed1970705fad57ba2f6508efb5575fa0`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 7.6 MB (7599232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8724d6501cda50c6475cfd7d6013e22bfb890a591470f2c2841852aea37b14ad`  
		Last Modified: Fri, 17 Apr 2026 22:07:43 GMT  
		Size: 207.9 MB (207927496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7a9fe2261492d12b27a7686d78251c95515a231e54e6cdca5a76ae4fbafa4b`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbda75a56450eeef99af7f2c5b0d0511abda9bde8c1f6f43f51dbb87ef7540c3`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0101d486fb124e2eab1731b18c8fee511a3e2c67a04b3898c6dbe7fcacd98977`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6409bdf776019f55d7a6991f644d472bd57af629459a36d65e0d7e47092fbc9`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83ac261baa130756b0c7c7e1b67753f50a2d0bd4837134f93edcbc8efb57a27`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4046eac517485413cc2a2e599e8f276d8831efc32c7d12de0d432e9408af38eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af675c2f03728c8573d10581400842a9e7b8581b6313aea484867d48a649892`

```dockerfile
```

-	Layers:
	-	`sha256:738b583ad67b54d964f377899497b2a10c6441864131fd384d7c3a00d1bbea26`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:baf054b83ff58c5346a885ae393bc73bb59a5d86c824b20923c9bb7c33eda4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228453914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cd75424023bcdbb4cede67f0ff31a96988724966a8f459ff64399ad750f016`
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
# Fri, 17 Apr 2026 22:05:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:42 GMT
ARG VERSION=26.1.11.9
# Fri, 17 Apr 2026 22:05:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:17 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1064ba074b4a7ef351d2ac68ef66dc2d125fc9824514b010408b891b663fa`  
		Last Modified: Fri, 17 Apr 2026 22:06:34 GMT  
		Size: 7.6 MB (7578923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23dd0e906d78ba651aee3189798dab7246769471e0ef8194907ed8d837764e9`  
		Last Modified: Fri, 17 Apr 2026 22:07:43 GMT  
		Size: 192.4 MB (192398399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b70bde7f639ae489a3fb6087a82f87d35d52866200680f0feb5396a744aa799`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259fc971c8776d05df2e20e7a8b37eee1b497afc70220c09b75ea7b2431979c2`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0101d486fb124e2eab1731b18c8fee511a3e2c67a04b3898c6dbe7fcacd98977`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dae73d27430ec24cdba37f6d9058eecea4c4f02740a7f732275fb30064d530c`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed93eaec3e36586306d22974ca1cf7502c2a65667ef51cb1f720d1d274747ce`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:46bc7fe227ff2c7be4f7568f432f95574e72037e22f2320c24ae53f3718bbd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad8d5e050d7e2d03760f79547f061774bfd3c8cd88816ca32a0db277ede94c5`

```dockerfile
```

-	Layers:
	-	`sha256:9f729f2964c88930f1c8f06df8736bff765edaef9c90a2ebd57e5f83baaba97d`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1-jammy`

```console
$ docker pull clickhouse@sha256:8e406990c24b9746b4df002dca6edf475d99144644eeb756daf8a3001850716e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:46728d1226717b46ed6c0fe0c1a34d9e8a3d07ccb9d5525baee06123b46c80e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246133274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6c5ac80f2293c61ad662cb446d2ae3e182485a94b3863acda78202010a9254`
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
# Fri, 17 Apr 2026 22:05:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:46 GMT
ARG VERSION=26.1.11.9
# Fri, 17 Apr 2026 22:05:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:17 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa516dc0cf58e41d3131c5590b68c1c4ed1970705fad57ba2f6508efb5575fa0`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 7.6 MB (7599232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8724d6501cda50c6475cfd7d6013e22bfb890a591470f2c2841852aea37b14ad`  
		Last Modified: Fri, 17 Apr 2026 22:07:43 GMT  
		Size: 207.9 MB (207927496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7a9fe2261492d12b27a7686d78251c95515a231e54e6cdca5a76ae4fbafa4b`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbda75a56450eeef99af7f2c5b0d0511abda9bde8c1f6f43f51dbb87ef7540c3`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0101d486fb124e2eab1731b18c8fee511a3e2c67a04b3898c6dbe7fcacd98977`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6409bdf776019f55d7a6991f644d472bd57af629459a36d65e0d7e47092fbc9`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83ac261baa130756b0c7c7e1b67753f50a2d0bd4837134f93edcbc8efb57a27`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4046eac517485413cc2a2e599e8f276d8831efc32c7d12de0d432e9408af38eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af675c2f03728c8573d10581400842a9e7b8581b6313aea484867d48a649892`

```dockerfile
```

-	Layers:
	-	`sha256:738b583ad67b54d964f377899497b2a10c6441864131fd384d7c3a00d1bbea26`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:baf054b83ff58c5346a885ae393bc73bb59a5d86c824b20923c9bb7c33eda4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228453914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cd75424023bcdbb4cede67f0ff31a96988724966a8f459ff64399ad750f016`
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
# Fri, 17 Apr 2026 22:05:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:42 GMT
ARG VERSION=26.1.11.9
# Fri, 17 Apr 2026 22:05:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:17 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1064ba074b4a7ef351d2ac68ef66dc2d125fc9824514b010408b891b663fa`  
		Last Modified: Fri, 17 Apr 2026 22:06:34 GMT  
		Size: 7.6 MB (7578923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23dd0e906d78ba651aee3189798dab7246769471e0ef8194907ed8d837764e9`  
		Last Modified: Fri, 17 Apr 2026 22:07:43 GMT  
		Size: 192.4 MB (192398399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b70bde7f639ae489a3fb6087a82f87d35d52866200680f0feb5396a744aa799`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259fc971c8776d05df2e20e7a8b37eee1b497afc70220c09b75ea7b2431979c2`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0101d486fb124e2eab1731b18c8fee511a3e2c67a04b3898c6dbe7fcacd98977`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dae73d27430ec24cdba37f6d9058eecea4c4f02740a7f732275fb30064d530c`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed93eaec3e36586306d22974ca1cf7502c2a65667ef51cb1f720d1d274747ce`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:46bc7fe227ff2c7be4f7568f432f95574e72037e22f2320c24ae53f3718bbd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad8d5e050d7e2d03760f79547f061774bfd3c8cd88816ca32a0db277ede94c5`

```dockerfile
```

-	Layers:
	-	`sha256:9f729f2964c88930f1c8f06df8736bff765edaef9c90a2ebd57e5f83baaba97d`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.11`

```console
$ docker pull clickhouse@sha256:8e406990c24b9746b4df002dca6edf475d99144644eeb756daf8a3001850716e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:46728d1226717b46ed6c0fe0c1a34d9e8a3d07ccb9d5525baee06123b46c80e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246133274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6c5ac80f2293c61ad662cb446d2ae3e182485a94b3863acda78202010a9254`
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
# Fri, 17 Apr 2026 22:05:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:46 GMT
ARG VERSION=26.1.11.9
# Fri, 17 Apr 2026 22:05:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:17 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa516dc0cf58e41d3131c5590b68c1c4ed1970705fad57ba2f6508efb5575fa0`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 7.6 MB (7599232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8724d6501cda50c6475cfd7d6013e22bfb890a591470f2c2841852aea37b14ad`  
		Last Modified: Fri, 17 Apr 2026 22:07:43 GMT  
		Size: 207.9 MB (207927496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7a9fe2261492d12b27a7686d78251c95515a231e54e6cdca5a76ae4fbafa4b`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbda75a56450eeef99af7f2c5b0d0511abda9bde8c1f6f43f51dbb87ef7540c3`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0101d486fb124e2eab1731b18c8fee511a3e2c67a04b3898c6dbe7fcacd98977`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6409bdf776019f55d7a6991f644d472bd57af629459a36d65e0d7e47092fbc9`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83ac261baa130756b0c7c7e1b67753f50a2d0bd4837134f93edcbc8efb57a27`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4046eac517485413cc2a2e599e8f276d8831efc32c7d12de0d432e9408af38eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af675c2f03728c8573d10581400842a9e7b8581b6313aea484867d48a649892`

```dockerfile
```

-	Layers:
	-	`sha256:738b583ad67b54d964f377899497b2a10c6441864131fd384d7c3a00d1bbea26`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:baf054b83ff58c5346a885ae393bc73bb59a5d86c824b20923c9bb7c33eda4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228453914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cd75424023bcdbb4cede67f0ff31a96988724966a8f459ff64399ad750f016`
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
# Fri, 17 Apr 2026 22:05:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:42 GMT
ARG VERSION=26.1.11.9
# Fri, 17 Apr 2026 22:05:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:17 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1064ba074b4a7ef351d2ac68ef66dc2d125fc9824514b010408b891b663fa`  
		Last Modified: Fri, 17 Apr 2026 22:06:34 GMT  
		Size: 7.6 MB (7578923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23dd0e906d78ba651aee3189798dab7246769471e0ef8194907ed8d837764e9`  
		Last Modified: Fri, 17 Apr 2026 22:07:43 GMT  
		Size: 192.4 MB (192398399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b70bde7f639ae489a3fb6087a82f87d35d52866200680f0feb5396a744aa799`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259fc971c8776d05df2e20e7a8b37eee1b497afc70220c09b75ea7b2431979c2`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0101d486fb124e2eab1731b18c8fee511a3e2c67a04b3898c6dbe7fcacd98977`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dae73d27430ec24cdba37f6d9058eecea4c4f02740a7f732275fb30064d530c`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed93eaec3e36586306d22974ca1cf7502c2a65667ef51cb1f720d1d274747ce`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:46bc7fe227ff2c7be4f7568f432f95574e72037e22f2320c24ae53f3718bbd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad8d5e050d7e2d03760f79547f061774bfd3c8cd88816ca32a0db277ede94c5`

```dockerfile
```

-	Layers:
	-	`sha256:9f729f2964c88930f1c8f06df8736bff765edaef9c90a2ebd57e5f83baaba97d`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.11-jammy`

```console
$ docker pull clickhouse@sha256:8e406990c24b9746b4df002dca6edf475d99144644eeb756daf8a3001850716e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:46728d1226717b46ed6c0fe0c1a34d9e8a3d07ccb9d5525baee06123b46c80e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246133274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6c5ac80f2293c61ad662cb446d2ae3e182485a94b3863acda78202010a9254`
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
# Fri, 17 Apr 2026 22:05:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:46 GMT
ARG VERSION=26.1.11.9
# Fri, 17 Apr 2026 22:05:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:17 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa516dc0cf58e41d3131c5590b68c1c4ed1970705fad57ba2f6508efb5575fa0`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 7.6 MB (7599232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8724d6501cda50c6475cfd7d6013e22bfb890a591470f2c2841852aea37b14ad`  
		Last Modified: Fri, 17 Apr 2026 22:07:43 GMT  
		Size: 207.9 MB (207927496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7a9fe2261492d12b27a7686d78251c95515a231e54e6cdca5a76ae4fbafa4b`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbda75a56450eeef99af7f2c5b0d0511abda9bde8c1f6f43f51dbb87ef7540c3`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0101d486fb124e2eab1731b18c8fee511a3e2c67a04b3898c6dbe7fcacd98977`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6409bdf776019f55d7a6991f644d472bd57af629459a36d65e0d7e47092fbc9`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83ac261baa130756b0c7c7e1b67753f50a2d0bd4837134f93edcbc8efb57a27`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4046eac517485413cc2a2e599e8f276d8831efc32c7d12de0d432e9408af38eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af675c2f03728c8573d10581400842a9e7b8581b6313aea484867d48a649892`

```dockerfile
```

-	Layers:
	-	`sha256:738b583ad67b54d964f377899497b2a10c6441864131fd384d7c3a00d1bbea26`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:baf054b83ff58c5346a885ae393bc73bb59a5d86c824b20923c9bb7c33eda4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228453914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cd75424023bcdbb4cede67f0ff31a96988724966a8f459ff64399ad750f016`
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
# Fri, 17 Apr 2026 22:05:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:42 GMT
ARG VERSION=26.1.11.9
# Fri, 17 Apr 2026 22:05:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:17 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1064ba074b4a7ef351d2ac68ef66dc2d125fc9824514b010408b891b663fa`  
		Last Modified: Fri, 17 Apr 2026 22:06:34 GMT  
		Size: 7.6 MB (7578923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23dd0e906d78ba651aee3189798dab7246769471e0ef8194907ed8d837764e9`  
		Last Modified: Fri, 17 Apr 2026 22:07:43 GMT  
		Size: 192.4 MB (192398399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b70bde7f639ae489a3fb6087a82f87d35d52866200680f0feb5396a744aa799`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259fc971c8776d05df2e20e7a8b37eee1b497afc70220c09b75ea7b2431979c2`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0101d486fb124e2eab1731b18c8fee511a3e2c67a04b3898c6dbe7fcacd98977`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dae73d27430ec24cdba37f6d9058eecea4c4f02740a7f732275fb30064d530c`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed93eaec3e36586306d22974ca1cf7502c2a65667ef51cb1f720d1d274747ce`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:46bc7fe227ff2c7be4f7568f432f95574e72037e22f2320c24ae53f3718bbd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad8d5e050d7e2d03760f79547f061774bfd3c8cd88816ca32a0db277ede94c5`

```dockerfile
```

-	Layers:
	-	`sha256:9f729f2964c88930f1c8f06df8736bff765edaef9c90a2ebd57e5f83baaba97d`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.11.9`

```console
$ docker pull clickhouse@sha256:8e406990c24b9746b4df002dca6edf475d99144644eeb756daf8a3001850716e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.11.9` - linux; amd64

```console
$ docker pull clickhouse@sha256:46728d1226717b46ed6c0fe0c1a34d9e8a3d07ccb9d5525baee06123b46c80e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246133274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6c5ac80f2293c61ad662cb446d2ae3e182485a94b3863acda78202010a9254`
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
# Fri, 17 Apr 2026 22:05:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:46 GMT
ARG VERSION=26.1.11.9
# Fri, 17 Apr 2026 22:05:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:17 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa516dc0cf58e41d3131c5590b68c1c4ed1970705fad57ba2f6508efb5575fa0`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 7.6 MB (7599232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8724d6501cda50c6475cfd7d6013e22bfb890a591470f2c2841852aea37b14ad`  
		Last Modified: Fri, 17 Apr 2026 22:07:43 GMT  
		Size: 207.9 MB (207927496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7a9fe2261492d12b27a7686d78251c95515a231e54e6cdca5a76ae4fbafa4b`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbda75a56450eeef99af7f2c5b0d0511abda9bde8c1f6f43f51dbb87ef7540c3`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0101d486fb124e2eab1731b18c8fee511a3e2c67a04b3898c6dbe7fcacd98977`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6409bdf776019f55d7a6991f644d472bd57af629459a36d65e0d7e47092fbc9`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83ac261baa130756b0c7c7e1b67753f50a2d0bd4837134f93edcbc8efb57a27`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.11.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4046eac517485413cc2a2e599e8f276d8831efc32c7d12de0d432e9408af38eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af675c2f03728c8573d10581400842a9e7b8581b6313aea484867d48a649892`

```dockerfile
```

-	Layers:
	-	`sha256:738b583ad67b54d964f377899497b2a10c6441864131fd384d7c3a00d1bbea26`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.11.9` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:baf054b83ff58c5346a885ae393bc73bb59a5d86c824b20923c9bb7c33eda4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228453914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cd75424023bcdbb4cede67f0ff31a96988724966a8f459ff64399ad750f016`
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
# Fri, 17 Apr 2026 22:05:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:42 GMT
ARG VERSION=26.1.11.9
# Fri, 17 Apr 2026 22:05:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:17 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1064ba074b4a7ef351d2ac68ef66dc2d125fc9824514b010408b891b663fa`  
		Last Modified: Fri, 17 Apr 2026 22:06:34 GMT  
		Size: 7.6 MB (7578923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23dd0e906d78ba651aee3189798dab7246769471e0ef8194907ed8d837764e9`  
		Last Modified: Fri, 17 Apr 2026 22:07:43 GMT  
		Size: 192.4 MB (192398399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b70bde7f639ae489a3fb6087a82f87d35d52866200680f0feb5396a744aa799`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259fc971c8776d05df2e20e7a8b37eee1b497afc70220c09b75ea7b2431979c2`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0101d486fb124e2eab1731b18c8fee511a3e2c67a04b3898c6dbe7fcacd98977`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dae73d27430ec24cdba37f6d9058eecea4c4f02740a7f732275fb30064d530c`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed93eaec3e36586306d22974ca1cf7502c2a65667ef51cb1f720d1d274747ce`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.11.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:46bc7fe227ff2c7be4f7568f432f95574e72037e22f2320c24ae53f3718bbd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad8d5e050d7e2d03760f79547f061774bfd3c8cd88816ca32a0db277ede94c5`

```dockerfile
```

-	Layers:
	-	`sha256:9f729f2964c88930f1c8f06df8736bff765edaef9c90a2ebd57e5f83baaba97d`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.11.9-jammy`

```console
$ docker pull clickhouse@sha256:8e406990c24b9746b4df002dca6edf475d99144644eeb756daf8a3001850716e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.11.9-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:46728d1226717b46ed6c0fe0c1a34d9e8a3d07ccb9d5525baee06123b46c80e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.1 MB (246133274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b6c5ac80f2293c61ad662cb446d2ae3e182485a94b3863acda78202010a9254`
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
# Fri, 17 Apr 2026 22:05:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:46 GMT
ARG VERSION=26.1.11.9
# Fri, 17 Apr 2026 22:05:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:17 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa516dc0cf58e41d3131c5590b68c1c4ed1970705fad57ba2f6508efb5575fa0`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 7.6 MB (7599232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8724d6501cda50c6475cfd7d6013e22bfb890a591470f2c2841852aea37b14ad`  
		Last Modified: Fri, 17 Apr 2026 22:07:43 GMT  
		Size: 207.9 MB (207927496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7a9fe2261492d12b27a7686d78251c95515a231e54e6cdca5a76ae4fbafa4b`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbda75a56450eeef99af7f2c5b0d0511abda9bde8c1f6f43f51dbb87ef7540c3`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0101d486fb124e2eab1731b18c8fee511a3e2c67a04b3898c6dbe7fcacd98977`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6409bdf776019f55d7a6991f644d472bd57af629459a36d65e0d7e47092fbc9`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83ac261baa130756b0c7c7e1b67753f50a2d0bd4837134f93edcbc8efb57a27`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.11.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4046eac517485413cc2a2e599e8f276d8831efc32c7d12de0d432e9408af38eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af675c2f03728c8573d10581400842a9e7b8581b6313aea484867d48a649892`

```dockerfile
```

-	Layers:
	-	`sha256:738b583ad67b54d964f377899497b2a10c6441864131fd384d7c3a00d1bbea26`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.11.9-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:baf054b83ff58c5346a885ae393bc73bb59a5d86c824b20923c9bb7c33eda4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228453914 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cd75424023bcdbb4cede67f0ff31a96988724966a8f459ff64399ad750f016`
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
# Fri, 17 Apr 2026 22:05:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:42 GMT
ARG VERSION=26.1.11.9
# Fri, 17 Apr 2026 22:05:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:17 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.11.9 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:17 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1064ba074b4a7ef351d2ac68ef66dc2d125fc9824514b010408b891b663fa`  
		Last Modified: Fri, 17 Apr 2026 22:06:34 GMT  
		Size: 7.6 MB (7578923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23dd0e906d78ba651aee3189798dab7246769471e0ef8194907ed8d837764e9`  
		Last Modified: Fri, 17 Apr 2026 22:07:43 GMT  
		Size: 192.4 MB (192398399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b70bde7f639ae489a3fb6087a82f87d35d52866200680f0feb5396a744aa799`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259fc971c8776d05df2e20e7a8b37eee1b497afc70220c09b75ea7b2431979c2`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0101d486fb124e2eab1731b18c8fee511a3e2c67a04b3898c6dbe7fcacd98977`  
		Last Modified: Fri, 17 Apr 2026 22:07:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dae73d27430ec24cdba37f6d9058eecea4c4f02740a7f732275fb30064d530c`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ed93eaec3e36586306d22974ca1cf7502c2a65667ef51cb1f720d1d274747ce`  
		Last Modified: Fri, 17 Apr 2026 22:07:40 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.11.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:46bc7fe227ff2c7be4f7568f432f95574e72037e22f2320c24ae53f3718bbd6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad8d5e050d7e2d03760f79547f061774bfd3c8cd88816ca32a0db277ede94c5`

```dockerfile
```

-	Layers:
	-	`sha256:9f729f2964c88930f1c8f06df8736bff765edaef9c90a2ebd57e5f83baaba97d`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2`

```console
$ docker pull clickhouse@sha256:1453b6ab1857216b43760238336380ddabcfd5e416e6167278e073f560d0f1ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:92fb8ea39dd453c70bc86be2c9b5a73edb60a740d08c60bd8e47a56646772442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253830585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b513d85741e83176a48236568571e8879b4350a7b6aaf82838fddad57e09304`
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
# Fri, 17 Apr 2026 22:07:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:07:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:07:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:07:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:07:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:07:06 GMT
ARG VERSION=26.2.16.4
# Fri, 17 Apr 2026 22:07:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:32 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01bdb5d2a628dea0acfb3a0f962d17b3d97b2c862e93e6ecab64cf6943a2f6a`  
		Last Modified: Fri, 17 Apr 2026 22:07:59 GMT  
		Size: 7.6 MB (7599214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f188d80b5b481669330e710965b7acee1c44223c077e2f6f5adf65c9714d9b6`  
		Last Modified: Fri, 17 Apr 2026 22:08:03 GMT  
		Size: 215.6 MB (215624823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b6f1c1ca3ff0226c1d1d92c5c685d5af768c486abcdbc9c3a36fbad18ac647`  
		Last Modified: Fri, 17 Apr 2026 22:07:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8b84d6dabbb5c51c1d8d5133aa4323fff6723f02b104f0a3e27e388e8b49ec`  
		Last Modified: Fri, 17 Apr 2026 22:07:59 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c68a35929641ccf224d3fb3cf513739fcf207281919d19ac2cbc38c965dc4f`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23f4631fd8c64d22d30c6aa66d1e23a6d97bd2954043fb88f5cadc02fdad43f`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e93245e5d7b9764b4ed0d5f95e8a25390093ca82c3cca35f23c858599403625`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:44430fe5d3669d53c4a5037e3e3fc3d8ea4746d60fb88c042806f69d20b8af4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad793367a7d3ce314feb997fd37641bd91457eadb855faa2fe889d4125aafeb`

```dockerfile
```

-	Layers:
	-	`sha256:58842fec13862da5dd378a4c9c98178417048dab4ca3107915e2e3d78dbcdf46`  
		Last Modified: Fri, 17 Apr 2026 22:07:58 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5f52020d08054ca798259aaaa6510e487a9f57ee05b2b4b36f5cf2c7d73fc050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237437149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db925c3d2c03fafde59f42f7513ff65134f6d402db9eb7d45e56f8b898e7fd3`
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
# Fri, 17 Apr 2026 22:06:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:06:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:06:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:06:41 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:06:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:06:41 GMT
ARG VERSION=26.2.16.4
# Fri, 17 Apr 2026 22:06:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:13 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ae12d48f236019c295900390e1ceb855dfe05c314ab849676907b15a9c4ebc`  
		Last Modified: Fri, 17 Apr 2026 22:07:35 GMT  
		Size: 7.6 MB (7578919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36015caf58d26cfa1de22a680973f1b8a4f179317b3352737fbdcc0953d30e`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 201.4 MB (201381643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509ba50b3ca3ed5b64a18713c4acc271dcd4196f191d169677c38d78232154f`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1a925d213fadc69265d5041ec56b46b91d1b54bbc7c03896ca78b24d5f10f0`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7e990ea1b082c50a71e079f518bb3fb723e0c2a3b5261ffe4b455c93b61295`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d78832a6751b94381befce0ed24999782298fc00603c386bb32bda1b3c470b9`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1617559b4ee402f4116fcc94a469e93f584096241e61b894daea2b60bf6e3a6d`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:66534d382f7a6a13d8a4885d6b7cf2c06a2c3e66e71c7baa743cdc21793ec2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cd130aabed220cee03160dac7e730ccfccac963e2ea4ba938d339006be775e`

```dockerfile
```

-	Layers:
	-	`sha256:c067fc9792e56d42cc9f3a66ac0d00944427be165606b822b7b0108b4881af0f`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2-jammy`

```console
$ docker pull clickhouse@sha256:1453b6ab1857216b43760238336380ddabcfd5e416e6167278e073f560d0f1ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:92fb8ea39dd453c70bc86be2c9b5a73edb60a740d08c60bd8e47a56646772442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253830585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b513d85741e83176a48236568571e8879b4350a7b6aaf82838fddad57e09304`
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
# Fri, 17 Apr 2026 22:07:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:07:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:07:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:07:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:07:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:07:06 GMT
ARG VERSION=26.2.16.4
# Fri, 17 Apr 2026 22:07:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:32 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01bdb5d2a628dea0acfb3a0f962d17b3d97b2c862e93e6ecab64cf6943a2f6a`  
		Last Modified: Fri, 17 Apr 2026 22:07:59 GMT  
		Size: 7.6 MB (7599214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f188d80b5b481669330e710965b7acee1c44223c077e2f6f5adf65c9714d9b6`  
		Last Modified: Fri, 17 Apr 2026 22:08:03 GMT  
		Size: 215.6 MB (215624823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b6f1c1ca3ff0226c1d1d92c5c685d5af768c486abcdbc9c3a36fbad18ac647`  
		Last Modified: Fri, 17 Apr 2026 22:07:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8b84d6dabbb5c51c1d8d5133aa4323fff6723f02b104f0a3e27e388e8b49ec`  
		Last Modified: Fri, 17 Apr 2026 22:07:59 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c68a35929641ccf224d3fb3cf513739fcf207281919d19ac2cbc38c965dc4f`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23f4631fd8c64d22d30c6aa66d1e23a6d97bd2954043fb88f5cadc02fdad43f`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e93245e5d7b9764b4ed0d5f95e8a25390093ca82c3cca35f23c858599403625`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:44430fe5d3669d53c4a5037e3e3fc3d8ea4746d60fb88c042806f69d20b8af4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad793367a7d3ce314feb997fd37641bd91457eadb855faa2fe889d4125aafeb`

```dockerfile
```

-	Layers:
	-	`sha256:58842fec13862da5dd378a4c9c98178417048dab4ca3107915e2e3d78dbcdf46`  
		Last Modified: Fri, 17 Apr 2026 22:07:58 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5f52020d08054ca798259aaaa6510e487a9f57ee05b2b4b36f5cf2c7d73fc050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237437149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db925c3d2c03fafde59f42f7513ff65134f6d402db9eb7d45e56f8b898e7fd3`
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
# Fri, 17 Apr 2026 22:06:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:06:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:06:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:06:41 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:06:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:06:41 GMT
ARG VERSION=26.2.16.4
# Fri, 17 Apr 2026 22:06:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:13 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ae12d48f236019c295900390e1ceb855dfe05c314ab849676907b15a9c4ebc`  
		Last Modified: Fri, 17 Apr 2026 22:07:35 GMT  
		Size: 7.6 MB (7578919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36015caf58d26cfa1de22a680973f1b8a4f179317b3352737fbdcc0953d30e`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 201.4 MB (201381643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509ba50b3ca3ed5b64a18713c4acc271dcd4196f191d169677c38d78232154f`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1a925d213fadc69265d5041ec56b46b91d1b54bbc7c03896ca78b24d5f10f0`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7e990ea1b082c50a71e079f518bb3fb723e0c2a3b5261ffe4b455c93b61295`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d78832a6751b94381befce0ed24999782298fc00603c386bb32bda1b3c470b9`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1617559b4ee402f4116fcc94a469e93f584096241e61b894daea2b60bf6e3a6d`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:66534d382f7a6a13d8a4885d6b7cf2c06a2c3e66e71c7baa743cdc21793ec2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cd130aabed220cee03160dac7e730ccfccac963e2ea4ba938d339006be775e`

```dockerfile
```

-	Layers:
	-	`sha256:c067fc9792e56d42cc9f3a66ac0d00944427be165606b822b7b0108b4881af0f`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.16`

```console
$ docker pull clickhouse@sha256:1453b6ab1857216b43760238336380ddabcfd5e416e6167278e073f560d0f1ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.16` - linux; amd64

```console
$ docker pull clickhouse@sha256:92fb8ea39dd453c70bc86be2c9b5a73edb60a740d08c60bd8e47a56646772442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253830585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b513d85741e83176a48236568571e8879b4350a7b6aaf82838fddad57e09304`
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
# Fri, 17 Apr 2026 22:07:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:07:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:07:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:07:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:07:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:07:06 GMT
ARG VERSION=26.2.16.4
# Fri, 17 Apr 2026 22:07:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:32 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01bdb5d2a628dea0acfb3a0f962d17b3d97b2c862e93e6ecab64cf6943a2f6a`  
		Last Modified: Fri, 17 Apr 2026 22:07:59 GMT  
		Size: 7.6 MB (7599214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f188d80b5b481669330e710965b7acee1c44223c077e2f6f5adf65c9714d9b6`  
		Last Modified: Fri, 17 Apr 2026 22:08:03 GMT  
		Size: 215.6 MB (215624823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b6f1c1ca3ff0226c1d1d92c5c685d5af768c486abcdbc9c3a36fbad18ac647`  
		Last Modified: Fri, 17 Apr 2026 22:07:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8b84d6dabbb5c51c1d8d5133aa4323fff6723f02b104f0a3e27e388e8b49ec`  
		Last Modified: Fri, 17 Apr 2026 22:07:59 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c68a35929641ccf224d3fb3cf513739fcf207281919d19ac2cbc38c965dc4f`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23f4631fd8c64d22d30c6aa66d1e23a6d97bd2954043fb88f5cadc02fdad43f`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e93245e5d7b9764b4ed0d5f95e8a25390093ca82c3cca35f23c858599403625`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.16` - unknown; unknown

```console
$ docker pull clickhouse@sha256:44430fe5d3669d53c4a5037e3e3fc3d8ea4746d60fb88c042806f69d20b8af4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad793367a7d3ce314feb997fd37641bd91457eadb855faa2fe889d4125aafeb`

```dockerfile
```

-	Layers:
	-	`sha256:58842fec13862da5dd378a4c9c98178417048dab4ca3107915e2e3d78dbcdf46`  
		Last Modified: Fri, 17 Apr 2026 22:07:58 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.16` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5f52020d08054ca798259aaaa6510e487a9f57ee05b2b4b36f5cf2c7d73fc050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237437149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db925c3d2c03fafde59f42f7513ff65134f6d402db9eb7d45e56f8b898e7fd3`
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
# Fri, 17 Apr 2026 22:06:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:06:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:06:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:06:41 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:06:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:06:41 GMT
ARG VERSION=26.2.16.4
# Fri, 17 Apr 2026 22:06:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:13 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ae12d48f236019c295900390e1ceb855dfe05c314ab849676907b15a9c4ebc`  
		Last Modified: Fri, 17 Apr 2026 22:07:35 GMT  
		Size: 7.6 MB (7578919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36015caf58d26cfa1de22a680973f1b8a4f179317b3352737fbdcc0953d30e`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 201.4 MB (201381643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509ba50b3ca3ed5b64a18713c4acc271dcd4196f191d169677c38d78232154f`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1a925d213fadc69265d5041ec56b46b91d1b54bbc7c03896ca78b24d5f10f0`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7e990ea1b082c50a71e079f518bb3fb723e0c2a3b5261ffe4b455c93b61295`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d78832a6751b94381befce0ed24999782298fc00603c386bb32bda1b3c470b9`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1617559b4ee402f4116fcc94a469e93f584096241e61b894daea2b60bf6e3a6d`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.16` - unknown; unknown

```console
$ docker pull clickhouse@sha256:66534d382f7a6a13d8a4885d6b7cf2c06a2c3e66e71c7baa743cdc21793ec2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cd130aabed220cee03160dac7e730ccfccac963e2ea4ba938d339006be775e`

```dockerfile
```

-	Layers:
	-	`sha256:c067fc9792e56d42cc9f3a66ac0d00944427be165606b822b7b0108b4881af0f`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.16-jammy`

```console
$ docker pull clickhouse@sha256:1453b6ab1857216b43760238336380ddabcfd5e416e6167278e073f560d0f1ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.16-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:92fb8ea39dd453c70bc86be2c9b5a73edb60a740d08c60bd8e47a56646772442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253830585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b513d85741e83176a48236568571e8879b4350a7b6aaf82838fddad57e09304`
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
# Fri, 17 Apr 2026 22:07:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:07:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:07:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:07:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:07:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:07:06 GMT
ARG VERSION=26.2.16.4
# Fri, 17 Apr 2026 22:07:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:32 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01bdb5d2a628dea0acfb3a0f962d17b3d97b2c862e93e6ecab64cf6943a2f6a`  
		Last Modified: Fri, 17 Apr 2026 22:07:59 GMT  
		Size: 7.6 MB (7599214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f188d80b5b481669330e710965b7acee1c44223c077e2f6f5adf65c9714d9b6`  
		Last Modified: Fri, 17 Apr 2026 22:08:03 GMT  
		Size: 215.6 MB (215624823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b6f1c1ca3ff0226c1d1d92c5c685d5af768c486abcdbc9c3a36fbad18ac647`  
		Last Modified: Fri, 17 Apr 2026 22:07:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8b84d6dabbb5c51c1d8d5133aa4323fff6723f02b104f0a3e27e388e8b49ec`  
		Last Modified: Fri, 17 Apr 2026 22:07:59 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c68a35929641ccf224d3fb3cf513739fcf207281919d19ac2cbc38c965dc4f`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23f4631fd8c64d22d30c6aa66d1e23a6d97bd2954043fb88f5cadc02fdad43f`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e93245e5d7b9764b4ed0d5f95e8a25390093ca82c3cca35f23c858599403625`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.16-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:44430fe5d3669d53c4a5037e3e3fc3d8ea4746d60fb88c042806f69d20b8af4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad793367a7d3ce314feb997fd37641bd91457eadb855faa2fe889d4125aafeb`

```dockerfile
```

-	Layers:
	-	`sha256:58842fec13862da5dd378a4c9c98178417048dab4ca3107915e2e3d78dbcdf46`  
		Last Modified: Fri, 17 Apr 2026 22:07:58 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.16-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5f52020d08054ca798259aaaa6510e487a9f57ee05b2b4b36f5cf2c7d73fc050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237437149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db925c3d2c03fafde59f42f7513ff65134f6d402db9eb7d45e56f8b898e7fd3`
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
# Fri, 17 Apr 2026 22:06:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:06:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:06:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:06:41 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:06:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:06:41 GMT
ARG VERSION=26.2.16.4
# Fri, 17 Apr 2026 22:06:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:13 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ae12d48f236019c295900390e1ceb855dfe05c314ab849676907b15a9c4ebc`  
		Last Modified: Fri, 17 Apr 2026 22:07:35 GMT  
		Size: 7.6 MB (7578919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36015caf58d26cfa1de22a680973f1b8a4f179317b3352737fbdcc0953d30e`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 201.4 MB (201381643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509ba50b3ca3ed5b64a18713c4acc271dcd4196f191d169677c38d78232154f`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1a925d213fadc69265d5041ec56b46b91d1b54bbc7c03896ca78b24d5f10f0`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7e990ea1b082c50a71e079f518bb3fb723e0c2a3b5261ffe4b455c93b61295`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d78832a6751b94381befce0ed24999782298fc00603c386bb32bda1b3c470b9`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1617559b4ee402f4116fcc94a469e93f584096241e61b894daea2b60bf6e3a6d`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.16-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:66534d382f7a6a13d8a4885d6b7cf2c06a2c3e66e71c7baa743cdc21793ec2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cd130aabed220cee03160dac7e730ccfccac963e2ea4ba938d339006be775e`

```dockerfile
```

-	Layers:
	-	`sha256:c067fc9792e56d42cc9f3a66ac0d00944427be165606b822b7b0108b4881af0f`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.16.4`

```console
$ docker pull clickhouse@sha256:1453b6ab1857216b43760238336380ddabcfd5e416e6167278e073f560d0f1ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.16.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:92fb8ea39dd453c70bc86be2c9b5a73edb60a740d08c60bd8e47a56646772442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253830585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b513d85741e83176a48236568571e8879b4350a7b6aaf82838fddad57e09304`
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
# Fri, 17 Apr 2026 22:07:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:07:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:07:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:07:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:07:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:07:06 GMT
ARG VERSION=26.2.16.4
# Fri, 17 Apr 2026 22:07:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:32 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01bdb5d2a628dea0acfb3a0f962d17b3d97b2c862e93e6ecab64cf6943a2f6a`  
		Last Modified: Fri, 17 Apr 2026 22:07:59 GMT  
		Size: 7.6 MB (7599214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f188d80b5b481669330e710965b7acee1c44223c077e2f6f5adf65c9714d9b6`  
		Last Modified: Fri, 17 Apr 2026 22:08:03 GMT  
		Size: 215.6 MB (215624823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b6f1c1ca3ff0226c1d1d92c5c685d5af768c486abcdbc9c3a36fbad18ac647`  
		Last Modified: Fri, 17 Apr 2026 22:07:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8b84d6dabbb5c51c1d8d5133aa4323fff6723f02b104f0a3e27e388e8b49ec`  
		Last Modified: Fri, 17 Apr 2026 22:07:59 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c68a35929641ccf224d3fb3cf513739fcf207281919d19ac2cbc38c965dc4f`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23f4631fd8c64d22d30c6aa66d1e23a6d97bd2954043fb88f5cadc02fdad43f`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e93245e5d7b9764b4ed0d5f95e8a25390093ca82c3cca35f23c858599403625`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.16.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:44430fe5d3669d53c4a5037e3e3fc3d8ea4746d60fb88c042806f69d20b8af4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad793367a7d3ce314feb997fd37641bd91457eadb855faa2fe889d4125aafeb`

```dockerfile
```

-	Layers:
	-	`sha256:58842fec13862da5dd378a4c9c98178417048dab4ca3107915e2e3d78dbcdf46`  
		Last Modified: Fri, 17 Apr 2026 22:07:58 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.16.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5f52020d08054ca798259aaaa6510e487a9f57ee05b2b4b36f5cf2c7d73fc050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237437149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db925c3d2c03fafde59f42f7513ff65134f6d402db9eb7d45e56f8b898e7fd3`
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
# Fri, 17 Apr 2026 22:06:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:06:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:06:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:06:41 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:06:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:06:41 GMT
ARG VERSION=26.2.16.4
# Fri, 17 Apr 2026 22:06:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:13 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ae12d48f236019c295900390e1ceb855dfe05c314ab849676907b15a9c4ebc`  
		Last Modified: Fri, 17 Apr 2026 22:07:35 GMT  
		Size: 7.6 MB (7578919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36015caf58d26cfa1de22a680973f1b8a4f179317b3352737fbdcc0953d30e`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 201.4 MB (201381643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509ba50b3ca3ed5b64a18713c4acc271dcd4196f191d169677c38d78232154f`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1a925d213fadc69265d5041ec56b46b91d1b54bbc7c03896ca78b24d5f10f0`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7e990ea1b082c50a71e079f518bb3fb723e0c2a3b5261ffe4b455c93b61295`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d78832a6751b94381befce0ed24999782298fc00603c386bb32bda1b3c470b9`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1617559b4ee402f4116fcc94a469e93f584096241e61b894daea2b60bf6e3a6d`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.16.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:66534d382f7a6a13d8a4885d6b7cf2c06a2c3e66e71c7baa743cdc21793ec2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cd130aabed220cee03160dac7e730ccfccac963e2ea4ba938d339006be775e`

```dockerfile
```

-	Layers:
	-	`sha256:c067fc9792e56d42cc9f3a66ac0d00944427be165606b822b7b0108b4881af0f`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.16.4-jammy`

```console
$ docker pull clickhouse@sha256:1453b6ab1857216b43760238336380ddabcfd5e416e6167278e073f560d0f1ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.16.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:92fb8ea39dd453c70bc86be2c9b5a73edb60a740d08c60bd8e47a56646772442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253830585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b513d85741e83176a48236568571e8879b4350a7b6aaf82838fddad57e09304`
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
# Fri, 17 Apr 2026 22:07:06 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:07:06 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:07:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:07:06 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:07:06 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:07:06 GMT
ARG VERSION=26.2.16.4
# Fri, 17 Apr 2026 22:07:06 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:32 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:32 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:33 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f01bdb5d2a628dea0acfb3a0f962d17b3d97b2c862e93e6ecab64cf6943a2f6a`  
		Last Modified: Fri, 17 Apr 2026 22:07:59 GMT  
		Size: 7.6 MB (7599214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f188d80b5b481669330e710965b7acee1c44223c077e2f6f5adf65c9714d9b6`  
		Last Modified: Fri, 17 Apr 2026 22:08:03 GMT  
		Size: 215.6 MB (215624823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b6f1c1ca3ff0226c1d1d92c5c685d5af768c486abcdbc9c3a36fbad18ac647`  
		Last Modified: Fri, 17 Apr 2026 22:07:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8b84d6dabbb5c51c1d8d5133aa4323fff6723f02b104f0a3e27e388e8b49ec`  
		Last Modified: Fri, 17 Apr 2026 22:07:59 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c68a35929641ccf224d3fb3cf513739fcf207281919d19ac2cbc38c965dc4f`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23f4631fd8c64d22d30c6aa66d1e23a6d97bd2954043fb88f5cadc02fdad43f`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e93245e5d7b9764b4ed0d5f95e8a25390093ca82c3cca35f23c858599403625`  
		Last Modified: Fri, 17 Apr 2026 22:08:00 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.16.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:44430fe5d3669d53c4a5037e3e3fc3d8ea4746d60fb88c042806f69d20b8af4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ad793367a7d3ce314feb997fd37641bd91457eadb855faa2fe889d4125aafeb`

```dockerfile
```

-	Layers:
	-	`sha256:58842fec13862da5dd378a4c9c98178417048dab4ca3107915e2e3d78dbcdf46`  
		Last Modified: Fri, 17 Apr 2026 22:07:58 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.16.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5f52020d08054ca798259aaaa6510e487a9f57ee05b2b4b36f5cf2c7d73fc050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237437149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db925c3d2c03fafde59f42f7513ff65134f6d402db9eb7d45e56f8b898e7fd3`
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
# Fri, 17 Apr 2026 22:06:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:06:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:06:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:06:41 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:06:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:06:41 GMT
ARG VERSION=26.2.16.4
# Fri, 17 Apr 2026 22:06:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:07:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:07:13 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:07:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.16.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:07:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:07:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:07:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:07:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6ae12d48f236019c295900390e1ceb855dfe05c314ab849676907b15a9c4ebc`  
		Last Modified: Fri, 17 Apr 2026 22:07:35 GMT  
		Size: 7.6 MB (7578919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36015caf58d26cfa1de22a680973f1b8a4f179317b3352737fbdcc0953d30e`  
		Last Modified: Fri, 17 Apr 2026 22:07:39 GMT  
		Size: 201.4 MB (201381643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509ba50b3ca3ed5b64a18713c4acc271dcd4196f191d169677c38d78232154f`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d1a925d213fadc69265d5041ec56b46b91d1b54bbc7c03896ca78b24d5f10f0`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7e990ea1b082c50a71e079f518bb3fb723e0c2a3b5261ffe4b455c93b61295`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d78832a6751b94381befce0ed24999782298fc00603c386bb32bda1b3c470b9`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1617559b4ee402f4116fcc94a469e93f584096241e61b894daea2b60bf6e3a6d`  
		Last Modified: Fri, 17 Apr 2026 22:07:36 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.16.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:66534d382f7a6a13d8a4885d6b7cf2c06a2c3e66e71c7baa743cdc21793ec2fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cd130aabed220cee03160dac7e730ccfccac963e2ea4ba938d339006be775e`

```dockerfile
```

-	Layers:
	-	`sha256:c067fc9792e56d42cc9f3a66ac0d00944427be165606b822b7b0108b4881af0f`  
		Last Modified: Fri, 17 Apr 2026 22:07:34 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3`

```console
$ docker pull clickhouse@sha256:ffe2549bd940fdca6e1244b43e12607b563c105a7cfbb5b97de76b1c4b09efc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:87329f094ea41b9673cb6101e1acad62b8a0f47b2f6ee1d37d90e6c78f2cea59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262318472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81bd89b4722bc0c2ba08e53e25dda6d4f9cc138e39e9960e9646fcb1ef4b2b0`
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
# Fri, 17 Apr 2026 22:05:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:46 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:14 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa516dc0cf58e41d3131c5590b68c1c4ed1970705fad57ba2f6508efb5575fa0`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 7.6 MB (7599232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c8357a6e3993c2a8fc5ca7e729f20a087178c0f3467067555d681df1324f7`  
		Last Modified: Fri, 17 Apr 2026 22:06:43 GMT  
		Size: 224.1 MB (224112692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11849c834161c582418bf3b2ffa5caf4ee0b75cf885da14199ad86a5a3cd70d8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bd25b69add95a223f17cfbdda806c97ec07eaf0577cda7a30b5739e39fffb8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a1b522e255539ca8776fb1fe4719d8fe403769784f0247ab67047df041066f`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832d64788dbccaf2c61e4c06508220c06386e7af677bf97b1002f856cdcb1171`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2152e07e2660dbbbf06b957ee32e92e63c41894c159e6fe533121c81493b11`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:566e04909b5206b2609c1f9b70eed719b8065c1b3c79f6f6ec4c6a8009fa2567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a705115398293659917b7c9158599cdea0e7f04d0d02e5937fee255ff40c02`

```dockerfile
```

-	Layers:
	-	`sha256:8e6619019b474dc48f0d7f8c22c5b6fc182fc1484abd78eccec8c0d6142d337b`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 26.6 KB (26629 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9f74978fbe5304dd0cce6d765cab6561807e08d4802596950d7eb7e10767136c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244554228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d343c3636431f0994f216c45255604394a50d8c4fdad8b6f450f1b545d8eba`
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
# Fri, 17 Apr 2026 22:05:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:42 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:11 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:12 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1064ba074b4a7ef351d2ac68ef66dc2d125fc9824514b010408b891b663fa`  
		Last Modified: Fri, 17 Apr 2026 22:06:34 GMT  
		Size: 7.6 MB (7578923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2cc870af3c6969e747fd46c71acb1fc968be8256572d572feaeea020748966`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 208.5 MB (208498714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd309dd15521a92d8f216a8241c2e38006ae92335eba2ae7372e00fea36e8638`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f7f66088bb1e55d672d02219b720feca5249e9152abfa1abb4a37f109e9db`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57244f2db207fd19c6e7c7ab3c699b6b77b9b49d0db40257d85c3dadfc5d211`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf058ee907becc54cd510c6a44379579be857f4b6e54b927ad2342fd2ce31fd`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf65e091a2f8e62ec2e3f74b984968b89e91b151a98392d6eb7a1eb99513f1c`  
		Last Modified: Fri, 17 Apr 2026 22:06:36 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7c57c80aaccd4c7c1ae00005a7f67677a24a518a408228de2315e6bf285983fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a880907a0ec3e5dd3cd59b449dd701fe1a63bdc5546350daf398ce4797745ad`

```dockerfile
```

-	Layers:
	-	`sha256:5b5b0d76a54c6d2e21b83d0d2c1207a69021dafe250d28959184d199751e0666`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 26.9 KB (26865 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3-jammy`

```console
$ docker pull clickhouse@sha256:ffe2549bd940fdca6e1244b43e12607b563c105a7cfbb5b97de76b1c4b09efc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:87329f094ea41b9673cb6101e1acad62b8a0f47b2f6ee1d37d90e6c78f2cea59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262318472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81bd89b4722bc0c2ba08e53e25dda6d4f9cc138e39e9960e9646fcb1ef4b2b0`
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
# Fri, 17 Apr 2026 22:05:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:46 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:14 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa516dc0cf58e41d3131c5590b68c1c4ed1970705fad57ba2f6508efb5575fa0`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 7.6 MB (7599232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c8357a6e3993c2a8fc5ca7e729f20a087178c0f3467067555d681df1324f7`  
		Last Modified: Fri, 17 Apr 2026 22:06:43 GMT  
		Size: 224.1 MB (224112692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11849c834161c582418bf3b2ffa5caf4ee0b75cf885da14199ad86a5a3cd70d8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bd25b69add95a223f17cfbdda806c97ec07eaf0577cda7a30b5739e39fffb8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a1b522e255539ca8776fb1fe4719d8fe403769784f0247ab67047df041066f`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832d64788dbccaf2c61e4c06508220c06386e7af677bf97b1002f856cdcb1171`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2152e07e2660dbbbf06b957ee32e92e63c41894c159e6fe533121c81493b11`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:566e04909b5206b2609c1f9b70eed719b8065c1b3c79f6f6ec4c6a8009fa2567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a705115398293659917b7c9158599cdea0e7f04d0d02e5937fee255ff40c02`

```dockerfile
```

-	Layers:
	-	`sha256:8e6619019b474dc48f0d7f8c22c5b6fc182fc1484abd78eccec8c0d6142d337b`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 26.6 KB (26629 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9f74978fbe5304dd0cce6d765cab6561807e08d4802596950d7eb7e10767136c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244554228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d343c3636431f0994f216c45255604394a50d8c4fdad8b6f450f1b545d8eba`
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
# Fri, 17 Apr 2026 22:05:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:42 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:11 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:12 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1064ba074b4a7ef351d2ac68ef66dc2d125fc9824514b010408b891b663fa`  
		Last Modified: Fri, 17 Apr 2026 22:06:34 GMT  
		Size: 7.6 MB (7578923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2cc870af3c6969e747fd46c71acb1fc968be8256572d572feaeea020748966`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 208.5 MB (208498714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd309dd15521a92d8f216a8241c2e38006ae92335eba2ae7372e00fea36e8638`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f7f66088bb1e55d672d02219b720feca5249e9152abfa1abb4a37f109e9db`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57244f2db207fd19c6e7c7ab3c699b6b77b9b49d0db40257d85c3dadfc5d211`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf058ee907becc54cd510c6a44379579be857f4b6e54b927ad2342fd2ce31fd`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf65e091a2f8e62ec2e3f74b984968b89e91b151a98392d6eb7a1eb99513f1c`  
		Last Modified: Fri, 17 Apr 2026 22:06:36 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7c57c80aaccd4c7c1ae00005a7f67677a24a518a408228de2315e6bf285983fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a880907a0ec3e5dd3cd59b449dd701fe1a63bdc5546350daf398ce4797745ad`

```dockerfile
```

-	Layers:
	-	`sha256:5b5b0d76a54c6d2e21b83d0d2c1207a69021dafe250d28959184d199751e0666`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 26.9 KB (26865 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.9`

```console
$ docker pull clickhouse@sha256:ffe2549bd940fdca6e1244b43e12607b563c105a7cfbb5b97de76b1c4b09efc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.9` - linux; amd64

```console
$ docker pull clickhouse@sha256:87329f094ea41b9673cb6101e1acad62b8a0f47b2f6ee1d37d90e6c78f2cea59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262318472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81bd89b4722bc0c2ba08e53e25dda6d4f9cc138e39e9960e9646fcb1ef4b2b0`
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
# Fri, 17 Apr 2026 22:05:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:46 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:14 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa516dc0cf58e41d3131c5590b68c1c4ed1970705fad57ba2f6508efb5575fa0`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 7.6 MB (7599232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c8357a6e3993c2a8fc5ca7e729f20a087178c0f3467067555d681df1324f7`  
		Last Modified: Fri, 17 Apr 2026 22:06:43 GMT  
		Size: 224.1 MB (224112692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11849c834161c582418bf3b2ffa5caf4ee0b75cf885da14199ad86a5a3cd70d8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bd25b69add95a223f17cfbdda806c97ec07eaf0577cda7a30b5739e39fffb8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a1b522e255539ca8776fb1fe4719d8fe403769784f0247ab67047df041066f`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832d64788dbccaf2c61e4c06508220c06386e7af677bf97b1002f856cdcb1171`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2152e07e2660dbbbf06b957ee32e92e63c41894c159e6fe533121c81493b11`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:566e04909b5206b2609c1f9b70eed719b8065c1b3c79f6f6ec4c6a8009fa2567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a705115398293659917b7c9158599cdea0e7f04d0d02e5937fee255ff40c02`

```dockerfile
```

-	Layers:
	-	`sha256:8e6619019b474dc48f0d7f8c22c5b6fc182fc1484abd78eccec8c0d6142d337b`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 26.6 KB (26629 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.9` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9f74978fbe5304dd0cce6d765cab6561807e08d4802596950d7eb7e10767136c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244554228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d343c3636431f0994f216c45255604394a50d8c4fdad8b6f450f1b545d8eba`
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
# Fri, 17 Apr 2026 22:05:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:42 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:11 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:12 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1064ba074b4a7ef351d2ac68ef66dc2d125fc9824514b010408b891b663fa`  
		Last Modified: Fri, 17 Apr 2026 22:06:34 GMT  
		Size: 7.6 MB (7578923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2cc870af3c6969e747fd46c71acb1fc968be8256572d572feaeea020748966`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 208.5 MB (208498714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd309dd15521a92d8f216a8241c2e38006ae92335eba2ae7372e00fea36e8638`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f7f66088bb1e55d672d02219b720feca5249e9152abfa1abb4a37f109e9db`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57244f2db207fd19c6e7c7ab3c699b6b77b9b49d0db40257d85c3dadfc5d211`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf058ee907becc54cd510c6a44379579be857f4b6e54b927ad2342fd2ce31fd`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf65e091a2f8e62ec2e3f74b984968b89e91b151a98392d6eb7a1eb99513f1c`  
		Last Modified: Fri, 17 Apr 2026 22:06:36 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7c57c80aaccd4c7c1ae00005a7f67677a24a518a408228de2315e6bf285983fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a880907a0ec3e5dd3cd59b449dd701fe1a63bdc5546350daf398ce4797745ad`

```dockerfile
```

-	Layers:
	-	`sha256:5b5b0d76a54c6d2e21b83d0d2c1207a69021dafe250d28959184d199751e0666`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 26.9 KB (26865 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.9-jammy`

```console
$ docker pull clickhouse@sha256:ffe2549bd940fdca6e1244b43e12607b563c105a7cfbb5b97de76b1c4b09efc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.9-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:87329f094ea41b9673cb6101e1acad62b8a0f47b2f6ee1d37d90e6c78f2cea59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262318472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81bd89b4722bc0c2ba08e53e25dda6d4f9cc138e39e9960e9646fcb1ef4b2b0`
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
# Fri, 17 Apr 2026 22:05:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:46 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:14 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa516dc0cf58e41d3131c5590b68c1c4ed1970705fad57ba2f6508efb5575fa0`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 7.6 MB (7599232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c8357a6e3993c2a8fc5ca7e729f20a087178c0f3467067555d681df1324f7`  
		Last Modified: Fri, 17 Apr 2026 22:06:43 GMT  
		Size: 224.1 MB (224112692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11849c834161c582418bf3b2ffa5caf4ee0b75cf885da14199ad86a5a3cd70d8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bd25b69add95a223f17cfbdda806c97ec07eaf0577cda7a30b5739e39fffb8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a1b522e255539ca8776fb1fe4719d8fe403769784f0247ab67047df041066f`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832d64788dbccaf2c61e4c06508220c06386e7af677bf97b1002f856cdcb1171`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2152e07e2660dbbbf06b957ee32e92e63c41894c159e6fe533121c81493b11`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:566e04909b5206b2609c1f9b70eed719b8065c1b3c79f6f6ec4c6a8009fa2567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a705115398293659917b7c9158599cdea0e7f04d0d02e5937fee255ff40c02`

```dockerfile
```

-	Layers:
	-	`sha256:8e6619019b474dc48f0d7f8c22c5b6fc182fc1484abd78eccec8c0d6142d337b`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 26.6 KB (26629 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.9-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9f74978fbe5304dd0cce6d765cab6561807e08d4802596950d7eb7e10767136c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244554228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d343c3636431f0994f216c45255604394a50d8c4fdad8b6f450f1b545d8eba`
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
# Fri, 17 Apr 2026 22:05:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:42 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:11 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:12 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1064ba074b4a7ef351d2ac68ef66dc2d125fc9824514b010408b891b663fa`  
		Last Modified: Fri, 17 Apr 2026 22:06:34 GMT  
		Size: 7.6 MB (7578923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2cc870af3c6969e747fd46c71acb1fc968be8256572d572feaeea020748966`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 208.5 MB (208498714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd309dd15521a92d8f216a8241c2e38006ae92335eba2ae7372e00fea36e8638`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f7f66088bb1e55d672d02219b720feca5249e9152abfa1abb4a37f109e9db`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57244f2db207fd19c6e7c7ab3c699b6b77b9b49d0db40257d85c3dadfc5d211`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf058ee907becc54cd510c6a44379579be857f4b6e54b927ad2342fd2ce31fd`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf65e091a2f8e62ec2e3f74b984968b89e91b151a98392d6eb7a1eb99513f1c`  
		Last Modified: Fri, 17 Apr 2026 22:06:36 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7c57c80aaccd4c7c1ae00005a7f67677a24a518a408228de2315e6bf285983fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a880907a0ec3e5dd3cd59b449dd701fe1a63bdc5546350daf398ce4797745ad`

```dockerfile
```

-	Layers:
	-	`sha256:5b5b0d76a54c6d2e21b83d0d2c1207a69021dafe250d28959184d199751e0666`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 26.9 KB (26865 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.9.8`

```console
$ docker pull clickhouse@sha256:ffe2549bd940fdca6e1244b43e12607b563c105a7cfbb5b97de76b1c4b09efc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.9.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:87329f094ea41b9673cb6101e1acad62b8a0f47b2f6ee1d37d90e6c78f2cea59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262318472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81bd89b4722bc0c2ba08e53e25dda6d4f9cc138e39e9960e9646fcb1ef4b2b0`
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
# Fri, 17 Apr 2026 22:05:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:46 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:14 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa516dc0cf58e41d3131c5590b68c1c4ed1970705fad57ba2f6508efb5575fa0`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 7.6 MB (7599232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c8357a6e3993c2a8fc5ca7e729f20a087178c0f3467067555d681df1324f7`  
		Last Modified: Fri, 17 Apr 2026 22:06:43 GMT  
		Size: 224.1 MB (224112692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11849c834161c582418bf3b2ffa5caf4ee0b75cf885da14199ad86a5a3cd70d8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bd25b69add95a223f17cfbdda806c97ec07eaf0577cda7a30b5739e39fffb8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a1b522e255539ca8776fb1fe4719d8fe403769784f0247ab67047df041066f`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832d64788dbccaf2c61e4c06508220c06386e7af677bf97b1002f856cdcb1171`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2152e07e2660dbbbf06b957ee32e92e63c41894c159e6fe533121c81493b11`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.9.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:566e04909b5206b2609c1f9b70eed719b8065c1b3c79f6f6ec4c6a8009fa2567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a705115398293659917b7c9158599cdea0e7f04d0d02e5937fee255ff40c02`

```dockerfile
```

-	Layers:
	-	`sha256:8e6619019b474dc48f0d7f8c22c5b6fc182fc1484abd78eccec8c0d6142d337b`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 26.6 KB (26629 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.9.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9f74978fbe5304dd0cce6d765cab6561807e08d4802596950d7eb7e10767136c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244554228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d343c3636431f0994f216c45255604394a50d8c4fdad8b6f450f1b545d8eba`
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
# Fri, 17 Apr 2026 22:05:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:42 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:11 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:12 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1064ba074b4a7ef351d2ac68ef66dc2d125fc9824514b010408b891b663fa`  
		Last Modified: Fri, 17 Apr 2026 22:06:34 GMT  
		Size: 7.6 MB (7578923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2cc870af3c6969e747fd46c71acb1fc968be8256572d572feaeea020748966`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 208.5 MB (208498714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd309dd15521a92d8f216a8241c2e38006ae92335eba2ae7372e00fea36e8638`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f7f66088bb1e55d672d02219b720feca5249e9152abfa1abb4a37f109e9db`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57244f2db207fd19c6e7c7ab3c699b6b77b9b49d0db40257d85c3dadfc5d211`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf058ee907becc54cd510c6a44379579be857f4b6e54b927ad2342fd2ce31fd`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf65e091a2f8e62ec2e3f74b984968b89e91b151a98392d6eb7a1eb99513f1c`  
		Last Modified: Fri, 17 Apr 2026 22:06:36 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.9.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7c57c80aaccd4c7c1ae00005a7f67677a24a518a408228de2315e6bf285983fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a880907a0ec3e5dd3cd59b449dd701fe1a63bdc5546350daf398ce4797745ad`

```dockerfile
```

-	Layers:
	-	`sha256:5b5b0d76a54c6d2e21b83d0d2c1207a69021dafe250d28959184d199751e0666`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 26.9 KB (26865 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.9.8-jammy`

```console
$ docker pull clickhouse@sha256:ffe2549bd940fdca6e1244b43e12607b563c105a7cfbb5b97de76b1c4b09efc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.9.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:87329f094ea41b9673cb6101e1acad62b8a0f47b2f6ee1d37d90e6c78f2cea59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262318472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81bd89b4722bc0c2ba08e53e25dda6d4f9cc138e39e9960e9646fcb1ef4b2b0`
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
# Fri, 17 Apr 2026 22:05:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:46 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:14 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa516dc0cf58e41d3131c5590b68c1c4ed1970705fad57ba2f6508efb5575fa0`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 7.6 MB (7599232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c8357a6e3993c2a8fc5ca7e729f20a087178c0f3467067555d681df1324f7`  
		Last Modified: Fri, 17 Apr 2026 22:06:43 GMT  
		Size: 224.1 MB (224112692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11849c834161c582418bf3b2ffa5caf4ee0b75cf885da14199ad86a5a3cd70d8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bd25b69add95a223f17cfbdda806c97ec07eaf0577cda7a30b5739e39fffb8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a1b522e255539ca8776fb1fe4719d8fe403769784f0247ab67047df041066f`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832d64788dbccaf2c61e4c06508220c06386e7af677bf97b1002f856cdcb1171`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2152e07e2660dbbbf06b957ee32e92e63c41894c159e6fe533121c81493b11`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.9.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:566e04909b5206b2609c1f9b70eed719b8065c1b3c79f6f6ec4c6a8009fa2567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a705115398293659917b7c9158599cdea0e7f04d0d02e5937fee255ff40c02`

```dockerfile
```

-	Layers:
	-	`sha256:8e6619019b474dc48f0d7f8c22c5b6fc182fc1484abd78eccec8c0d6142d337b`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 26.6 KB (26629 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.9.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9f74978fbe5304dd0cce6d765cab6561807e08d4802596950d7eb7e10767136c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244554228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d343c3636431f0994f216c45255604394a50d8c4fdad8b6f450f1b545d8eba`
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
# Fri, 17 Apr 2026 22:05:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:42 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:11 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:12 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1064ba074b4a7ef351d2ac68ef66dc2d125fc9824514b010408b891b663fa`  
		Last Modified: Fri, 17 Apr 2026 22:06:34 GMT  
		Size: 7.6 MB (7578923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2cc870af3c6969e747fd46c71acb1fc968be8256572d572feaeea020748966`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 208.5 MB (208498714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd309dd15521a92d8f216a8241c2e38006ae92335eba2ae7372e00fea36e8638`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f7f66088bb1e55d672d02219b720feca5249e9152abfa1abb4a37f109e9db`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57244f2db207fd19c6e7c7ab3c699b6b77b9b49d0db40257d85c3dadfc5d211`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf058ee907becc54cd510c6a44379579be857f4b6e54b927ad2342fd2ce31fd`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf65e091a2f8e62ec2e3f74b984968b89e91b151a98392d6eb7a1eb99513f1c`  
		Last Modified: Fri, 17 Apr 2026 22:06:36 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.9.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7c57c80aaccd4c7c1ae00005a7f67677a24a518a408228de2315e6bf285983fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a880907a0ec3e5dd3cd59b449dd701fe1a63bdc5546350daf398ce4797745ad`

```dockerfile
```

-	Layers:
	-	`sha256:5b5b0d76a54c6d2e21b83d0d2c1207a69021dafe250d28959184d199751e0666`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 26.9 KB (26865 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:ffe2549bd940fdca6e1244b43e12607b563c105a7cfbb5b97de76b1c4b09efc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:87329f094ea41b9673cb6101e1acad62b8a0f47b2f6ee1d37d90e6c78f2cea59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262318472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81bd89b4722bc0c2ba08e53e25dda6d4f9cc138e39e9960e9646fcb1ef4b2b0`
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
# Fri, 17 Apr 2026 22:05:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:46 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:14 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa516dc0cf58e41d3131c5590b68c1c4ed1970705fad57ba2f6508efb5575fa0`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 7.6 MB (7599232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c8357a6e3993c2a8fc5ca7e729f20a087178c0f3467067555d681df1324f7`  
		Last Modified: Fri, 17 Apr 2026 22:06:43 GMT  
		Size: 224.1 MB (224112692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11849c834161c582418bf3b2ffa5caf4ee0b75cf885da14199ad86a5a3cd70d8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bd25b69add95a223f17cfbdda806c97ec07eaf0577cda7a30b5739e39fffb8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a1b522e255539ca8776fb1fe4719d8fe403769784f0247ab67047df041066f`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832d64788dbccaf2c61e4c06508220c06386e7af677bf97b1002f856cdcb1171`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2152e07e2660dbbbf06b957ee32e92e63c41894c159e6fe533121c81493b11`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:566e04909b5206b2609c1f9b70eed719b8065c1b3c79f6f6ec4c6a8009fa2567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a705115398293659917b7c9158599cdea0e7f04d0d02e5937fee255ff40c02`

```dockerfile
```

-	Layers:
	-	`sha256:8e6619019b474dc48f0d7f8c22c5b6fc182fc1484abd78eccec8c0d6142d337b`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 26.6 KB (26629 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9f74978fbe5304dd0cce6d765cab6561807e08d4802596950d7eb7e10767136c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244554228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d343c3636431f0994f216c45255604394a50d8c4fdad8b6f450f1b545d8eba`
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
# Fri, 17 Apr 2026 22:05:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:42 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:11 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:12 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1064ba074b4a7ef351d2ac68ef66dc2d125fc9824514b010408b891b663fa`  
		Last Modified: Fri, 17 Apr 2026 22:06:34 GMT  
		Size: 7.6 MB (7578923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2cc870af3c6969e747fd46c71acb1fc968be8256572d572feaeea020748966`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 208.5 MB (208498714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd309dd15521a92d8f216a8241c2e38006ae92335eba2ae7372e00fea36e8638`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f7f66088bb1e55d672d02219b720feca5249e9152abfa1abb4a37f109e9db`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57244f2db207fd19c6e7c7ab3c699b6b77b9b49d0db40257d85c3dadfc5d211`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf058ee907becc54cd510c6a44379579be857f4b6e54b927ad2342fd2ce31fd`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf65e091a2f8e62ec2e3f74b984968b89e91b151a98392d6eb7a1eb99513f1c`  
		Last Modified: Fri, 17 Apr 2026 22:06:36 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7c57c80aaccd4c7c1ae00005a7f67677a24a518a408228de2315e6bf285983fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a880907a0ec3e5dd3cd59b449dd701fe1a63bdc5546350daf398ce4797745ad`

```dockerfile
```

-	Layers:
	-	`sha256:5b5b0d76a54c6d2e21b83d0d2c1207a69021dafe250d28959184d199751e0666`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 26.9 KB (26865 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:ffe2549bd940fdca6e1244b43e12607b563c105a7cfbb5b97de76b1c4b09efc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:87329f094ea41b9673cb6101e1acad62b8a0f47b2f6ee1d37d90e6c78f2cea59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262318472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81bd89b4722bc0c2ba08e53e25dda6d4f9cc138e39e9960e9646fcb1ef4b2b0`
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
# Fri, 17 Apr 2026 22:05:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:46 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:14 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa516dc0cf58e41d3131c5590b68c1c4ed1970705fad57ba2f6508efb5575fa0`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 7.6 MB (7599232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c8357a6e3993c2a8fc5ca7e729f20a087178c0f3467067555d681df1324f7`  
		Last Modified: Fri, 17 Apr 2026 22:06:43 GMT  
		Size: 224.1 MB (224112692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11849c834161c582418bf3b2ffa5caf4ee0b75cf885da14199ad86a5a3cd70d8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bd25b69add95a223f17cfbdda806c97ec07eaf0577cda7a30b5739e39fffb8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a1b522e255539ca8776fb1fe4719d8fe403769784f0247ab67047df041066f`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832d64788dbccaf2c61e4c06508220c06386e7af677bf97b1002f856cdcb1171`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2152e07e2660dbbbf06b957ee32e92e63c41894c159e6fe533121c81493b11`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:566e04909b5206b2609c1f9b70eed719b8065c1b3c79f6f6ec4c6a8009fa2567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a705115398293659917b7c9158599cdea0e7f04d0d02e5937fee255ff40c02`

```dockerfile
```

-	Layers:
	-	`sha256:8e6619019b474dc48f0d7f8c22c5b6fc182fc1484abd78eccec8c0d6142d337b`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 26.6 KB (26629 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9f74978fbe5304dd0cce6d765cab6561807e08d4802596950d7eb7e10767136c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244554228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d343c3636431f0994f216c45255604394a50d8c4fdad8b6f450f1b545d8eba`
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
# Fri, 17 Apr 2026 22:05:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:42 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:11 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:12 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1064ba074b4a7ef351d2ac68ef66dc2d125fc9824514b010408b891b663fa`  
		Last Modified: Fri, 17 Apr 2026 22:06:34 GMT  
		Size: 7.6 MB (7578923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2cc870af3c6969e747fd46c71acb1fc968be8256572d572feaeea020748966`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 208.5 MB (208498714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd309dd15521a92d8f216a8241c2e38006ae92335eba2ae7372e00fea36e8638`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f7f66088bb1e55d672d02219b720feca5249e9152abfa1abb4a37f109e9db`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57244f2db207fd19c6e7c7ab3c699b6b77b9b49d0db40257d85c3dadfc5d211`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf058ee907becc54cd510c6a44379579be857f4b6e54b927ad2342fd2ce31fd`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf65e091a2f8e62ec2e3f74b984968b89e91b151a98392d6eb7a1eb99513f1c`  
		Last Modified: Fri, 17 Apr 2026 22:06:36 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7c57c80aaccd4c7c1ae00005a7f67677a24a518a408228de2315e6bf285983fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a880907a0ec3e5dd3cd59b449dd701fe1a63bdc5546350daf398ce4797745ad`

```dockerfile
```

-	Layers:
	-	`sha256:5b5b0d76a54c6d2e21b83d0d2c1207a69021dafe250d28959184d199751e0666`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 26.9 KB (26865 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:ffe2549bd940fdca6e1244b43e12607b563c105a7cfbb5b97de76b1c4b09efc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:87329f094ea41b9673cb6101e1acad62b8a0f47b2f6ee1d37d90e6c78f2cea59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262318472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81bd89b4722bc0c2ba08e53e25dda6d4f9cc138e39e9960e9646fcb1ef4b2b0`
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
# Fri, 17 Apr 2026 22:05:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:46 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:14 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa516dc0cf58e41d3131c5590b68c1c4ed1970705fad57ba2f6508efb5575fa0`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 7.6 MB (7599232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c8357a6e3993c2a8fc5ca7e729f20a087178c0f3467067555d681df1324f7`  
		Last Modified: Fri, 17 Apr 2026 22:06:43 GMT  
		Size: 224.1 MB (224112692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11849c834161c582418bf3b2ffa5caf4ee0b75cf885da14199ad86a5a3cd70d8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bd25b69add95a223f17cfbdda806c97ec07eaf0577cda7a30b5739e39fffb8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a1b522e255539ca8776fb1fe4719d8fe403769784f0247ab67047df041066f`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832d64788dbccaf2c61e4c06508220c06386e7af677bf97b1002f856cdcb1171`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2152e07e2660dbbbf06b957ee32e92e63c41894c159e6fe533121c81493b11`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:566e04909b5206b2609c1f9b70eed719b8065c1b3c79f6f6ec4c6a8009fa2567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a705115398293659917b7c9158599cdea0e7f04d0d02e5937fee255ff40c02`

```dockerfile
```

-	Layers:
	-	`sha256:8e6619019b474dc48f0d7f8c22c5b6fc182fc1484abd78eccec8c0d6142d337b`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 26.6 KB (26629 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9f74978fbe5304dd0cce6d765cab6561807e08d4802596950d7eb7e10767136c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244554228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d343c3636431f0994f216c45255604394a50d8c4fdad8b6f450f1b545d8eba`
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
# Fri, 17 Apr 2026 22:05:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:42 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:11 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:12 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1064ba074b4a7ef351d2ac68ef66dc2d125fc9824514b010408b891b663fa`  
		Last Modified: Fri, 17 Apr 2026 22:06:34 GMT  
		Size: 7.6 MB (7578923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2cc870af3c6969e747fd46c71acb1fc968be8256572d572feaeea020748966`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 208.5 MB (208498714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd309dd15521a92d8f216a8241c2e38006ae92335eba2ae7372e00fea36e8638`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f7f66088bb1e55d672d02219b720feca5249e9152abfa1abb4a37f109e9db`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57244f2db207fd19c6e7c7ab3c699b6b77b9b49d0db40257d85c3dadfc5d211`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf058ee907becc54cd510c6a44379579be857f4b6e54b927ad2342fd2ce31fd`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf65e091a2f8e62ec2e3f74b984968b89e91b151a98392d6eb7a1eb99513f1c`  
		Last Modified: Fri, 17 Apr 2026 22:06:36 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7c57c80aaccd4c7c1ae00005a7f67677a24a518a408228de2315e6bf285983fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a880907a0ec3e5dd3cd59b449dd701fe1a63bdc5546350daf398ce4797745ad`

```dockerfile
```

-	Layers:
	-	`sha256:5b5b0d76a54c6d2e21b83d0d2c1207a69021dafe250d28959184d199751e0666`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 26.9 KB (26865 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:ffe2549bd940fdca6e1244b43e12607b563c105a7cfbb5b97de76b1c4b09efc5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:87329f094ea41b9673cb6101e1acad62b8a0f47b2f6ee1d37d90e6c78f2cea59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.3 MB (262318472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81bd89b4722bc0c2ba08e53e25dda6d4f9cc138e39e9960e9646fcb1ef4b2b0`
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
# Fri, 17 Apr 2026 22:05:46 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:46 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:46 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:46 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:46 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:14 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:14 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:14 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:14 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa516dc0cf58e41d3131c5590b68c1c4ed1970705fad57ba2f6508efb5575fa0`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 7.6 MB (7599232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65c8357a6e3993c2a8fc5ca7e729f20a087178c0f3467067555d681df1324f7`  
		Last Modified: Fri, 17 Apr 2026 22:06:43 GMT  
		Size: 224.1 MB (224112692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11849c834161c582418bf3b2ffa5caf4ee0b75cf885da14199ad86a5a3cd70d8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bd25b69add95a223f17cfbdda806c97ec07eaf0577cda7a30b5739e39fffb8`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a1b522e255539ca8776fb1fe4719d8fe403769784f0247ab67047df041066f`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:832d64788dbccaf2c61e4c06508220c06386e7af677bf97b1002f856cdcb1171`  
		Last Modified: Fri, 17 Apr 2026 22:06:38 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2152e07e2660dbbbf06b957ee32e92e63c41894c159e6fe533121c81493b11`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:566e04909b5206b2609c1f9b70eed719b8065c1b3c79f6f6ec4c6a8009fa2567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9a705115398293659917b7c9158599cdea0e7f04d0d02e5937fee255ff40c02`

```dockerfile
```

-	Layers:
	-	`sha256:8e6619019b474dc48f0d7f8c22c5b6fc182fc1484abd78eccec8c0d6142d337b`  
		Last Modified: Fri, 17 Apr 2026 22:06:37 GMT  
		Size: 26.6 KB (26629 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:9f74978fbe5304dd0cce6d765cab6561807e08d4802596950d7eb7e10767136c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.6 MB (244554228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d343c3636431f0994f216c45255604394a50d8c4fdad8b6f450f1b545d8eba`
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
# Fri, 17 Apr 2026 22:05:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 17 Apr 2026 22:05:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 17 Apr 2026 22:05:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPO_CHANNEL=stable
# Fri, 17 Apr 2026 22:05:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 17 Apr 2026 22:05:42 GMT
ARG VERSION=26.3.9.8
# Fri, 17 Apr 2026 22:05:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 17 Apr 2026 22:06:11 GMT
ENV TZ=UTC
# Fri, 17 Apr 2026 22:06:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.9.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 17 Apr 2026 22:06:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 17 Apr 2026 22:06:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 17 Apr 2026 22:06:12 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 17 Apr 2026 22:06:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 17 Apr 2026 22:06:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb1064ba074b4a7ef351d2ac68ef66dc2d125fc9824514b010408b891b663fa`  
		Last Modified: Fri, 17 Apr 2026 22:06:34 GMT  
		Size: 7.6 MB (7578923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2cc870af3c6969e747fd46c71acb1fc968be8256572d572feaeea020748966`  
		Last Modified: Fri, 17 Apr 2026 22:06:39 GMT  
		Size: 208.5 MB (208498714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd309dd15521a92d8f216a8241c2e38006ae92335eba2ae7372e00fea36e8638`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a0f7f66088bb1e55d672d02219b720feca5249e9152abfa1abb4a37f109e9db`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57244f2db207fd19c6e7c7ab3c699b6b77b9b49d0db40257d85c3dadfc5d211`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf058ee907becc54cd510c6a44379579be857f4b6e54b927ad2342fd2ce31fd`  
		Last Modified: Fri, 17 Apr 2026 22:06:35 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf65e091a2f8e62ec2e3f74b984968b89e91b151a98392d6eb7a1eb99513f1c`  
		Last Modified: Fri, 17 Apr 2026 22:06:36 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7c57c80aaccd4c7c1ae00005a7f67677a24a518a408228de2315e6bf285983fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a880907a0ec3e5dd3cd59b449dd701fe1a63bdc5546350daf398ce4797745ad`

```dockerfile
```

-	Layers:
	-	`sha256:5b5b0d76a54c6d2e21b83d0d2c1207a69021dafe250d28959184d199751e0666`  
		Last Modified: Fri, 17 Apr 2026 22:06:33 GMT  
		Size: 26.9 KB (26865 bytes)  
		MIME: application/vnd.in-toto+json
