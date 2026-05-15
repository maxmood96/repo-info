<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.23`](#clickhouse25823)
-	[`clickhouse:25.8.23-jammy`](#clickhouse25823-jammy)
-	[`clickhouse:25.8.23.13`](#clickhouse2582313)
-	[`clickhouse:25.8.23.13-jammy`](#clickhouse2582313-jammy)
-	[`clickhouse:26.2`](#clickhouse262)
-	[`clickhouse:26.2-jammy`](#clickhouse262-jammy)
-	[`clickhouse:26.2.18`](#clickhouse26218)
-	[`clickhouse:26.2.18-jammy`](#clickhouse26218-jammy)
-	[`clickhouse:26.2.18.8`](#clickhouse262188)
-	[`clickhouse:26.2.18.8-jammy`](#clickhouse262188-jammy)
-	[`clickhouse:26.3`](#clickhouse263)
-	[`clickhouse:26.3-jammy`](#clickhouse263-jammy)
-	[`clickhouse:26.3.10`](#clickhouse26310)
-	[`clickhouse:26.3.10-jammy`](#clickhouse26310-jammy)
-	[`clickhouse:26.3.10.62`](#clickhouse2631062)
-	[`clickhouse:26.3.10.62-jammy`](#clickhouse2631062-jammy)
-	[`clickhouse:26.4`](#clickhouse264)
-	[`clickhouse:26.4-jammy`](#clickhouse264-jammy)
-	[`clickhouse:26.4.2`](#clickhouse2642)
-	[`clickhouse:26.4.2-jammy`](#clickhouse2642-jammy)
-	[`clickhouse:26.4.2.10`](#clickhouse264210)
-	[`clickhouse:26.4.2.10-jammy`](#clickhouse264210-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:120f7787f3c8348f9ef1604576fd8d6dddea0119294ee7ff92aae012bdaf50bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:946afdf10ba21ac49d459489d82d8574a5b82cbefd218b2cc7f3676727f819aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229736134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898aced72fee331c70d58a7a8c4e6fed61038c3fd85f6a4524cbc1bad69b78c3`
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
# Fri, 15 May 2026 20:13:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:13:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:13:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:13:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:13:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:13:00 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 20:13:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:24 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6198935e4c55ea3200b58ab56b0f6d7ac7d354295114230da9b28873004449b9`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 7.6 MB (7599209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103bac519b1aadfa46fbb1070f878b621afe21ef9d6b4b4de1cc28d54930111b`  
		Last Modified: Fri, 15 May 2026 20:13:58 GMT  
		Size: 191.5 MB (191530407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6dd08c431ea3aa95018000e2c79f3066878f602748e16f2eb5abb3421120ef`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee09314fe284db58d3694fbd1847ecb85a19fd4040a3084c22e71f0905552444`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a507db5e302556e0de8be987a3db8a9244494face2af3f8930c15c6007e7e0`  
		Last Modified: Fri, 15 May 2026 20:13:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a64d669527cc67773dbefa63c0cc4815c9982f84bb2d5bfc1ad13044e2382aa`  
		Last Modified: Fri, 15 May 2026 20:13:48 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b53c8a06e548ddd945507099dd1ca071ab8279759b9f7685e0463dda8756857`  
		Last Modified: Fri, 15 May 2026 20:13:49 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2989d8aee1db653f7150490f28d055e4fb0b3efdc7159b58d2da3cbde17cb268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fe4acbafc01d7ea075cc8e580ded2afabbbd75c2c1cc1c3cbf92d47650602d`

```dockerfile
```

-	Layers:
	-	`sha256:86147e4fa707c5fdb59ef96869da702880e173e98db750eebb3ed045a9387e5a`  
		Last Modified: Fri, 15 May 2026 20:13:46 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0bee4e1b902b0a16a258817c952332ea56e3e3306853e2f68c75c4ab73340259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214755894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555981d8ec9377bac6520f9e41d33bdefd43741c1550c505fce64fdebc5674a4`
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
# Fri, 15 May 2026 20:12:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:41 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:41 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 20:12:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:20 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:20 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:20 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:20 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:20 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:20 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4ba3fd81b78d81cde22f57080242d451e0874560fb2a85e42d60f564d69a4d`  
		Last Modified: Fri, 15 May 2026 20:13:39 GMT  
		Size: 7.6 MB (7578924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed971e1f00e1850e716e54614727445dada3deb6c85e5654ed157893a2954a9`  
		Last Modified: Fri, 15 May 2026 20:13:42 GMT  
		Size: 178.7 MB (178700407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab32bd7d6b5d491330f76d853b90acfc583421f50c2550e13f399db6f568e66`  
		Last Modified: Fri, 15 May 2026 20:13:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99dc0c4363dc7d76407d6f25fb4e87d840260437ee480e8a0da8802eebd49433`  
		Last Modified: Fri, 15 May 2026 20:13:39 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a720aa38614e97a32ea0557751f1e7fe859748800c95171a83f9732958c2ea09`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bddcaef3f88078d160bf5276028cd8f63c77aa67aa6201cee8fa7b31b7087d`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dafa50616f0afea00586f771e649703b689a6e75edc3399b5ac2355147cc56`  
		Last Modified: Fri, 15 May 2026 20:13:41 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a4b251bd89da4bda7b508dc8cb9a63e51f203d1d9d77361068d9a96ab90aa414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dff045eb8f1bcd3d0282cebae5d93eb266f23daec63dab878c06764f6e3a24`

```dockerfile
```

-	Layers:
	-	`sha256:bce1ec2d6bdf3765133e79faf0fc671eeab796f885cd4dec41b365e5dfd6f041`  
		Last Modified: Fri, 15 May 2026 20:13:38 GMT  
		Size: 26.4 KB (26422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:120f7787f3c8348f9ef1604576fd8d6dddea0119294ee7ff92aae012bdaf50bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:946afdf10ba21ac49d459489d82d8574a5b82cbefd218b2cc7f3676727f819aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229736134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898aced72fee331c70d58a7a8c4e6fed61038c3fd85f6a4524cbc1bad69b78c3`
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
# Fri, 15 May 2026 20:13:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:13:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:13:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:13:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:13:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:13:00 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 20:13:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:24 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6198935e4c55ea3200b58ab56b0f6d7ac7d354295114230da9b28873004449b9`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 7.6 MB (7599209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103bac519b1aadfa46fbb1070f878b621afe21ef9d6b4b4de1cc28d54930111b`  
		Last Modified: Fri, 15 May 2026 20:13:58 GMT  
		Size: 191.5 MB (191530407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6dd08c431ea3aa95018000e2c79f3066878f602748e16f2eb5abb3421120ef`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee09314fe284db58d3694fbd1847ecb85a19fd4040a3084c22e71f0905552444`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a507db5e302556e0de8be987a3db8a9244494face2af3f8930c15c6007e7e0`  
		Last Modified: Fri, 15 May 2026 20:13:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a64d669527cc67773dbefa63c0cc4815c9982f84bb2d5bfc1ad13044e2382aa`  
		Last Modified: Fri, 15 May 2026 20:13:48 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b53c8a06e548ddd945507099dd1ca071ab8279759b9f7685e0463dda8756857`  
		Last Modified: Fri, 15 May 2026 20:13:49 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2989d8aee1db653f7150490f28d055e4fb0b3efdc7159b58d2da3cbde17cb268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fe4acbafc01d7ea075cc8e580ded2afabbbd75c2c1cc1c3cbf92d47650602d`

```dockerfile
```

-	Layers:
	-	`sha256:86147e4fa707c5fdb59ef96869da702880e173e98db750eebb3ed045a9387e5a`  
		Last Modified: Fri, 15 May 2026 20:13:46 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0bee4e1b902b0a16a258817c952332ea56e3e3306853e2f68c75c4ab73340259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214755894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555981d8ec9377bac6520f9e41d33bdefd43741c1550c505fce64fdebc5674a4`
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
# Fri, 15 May 2026 20:12:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:41 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:41 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 20:12:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:20 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:20 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:20 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:20 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:20 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:20 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4ba3fd81b78d81cde22f57080242d451e0874560fb2a85e42d60f564d69a4d`  
		Last Modified: Fri, 15 May 2026 20:13:39 GMT  
		Size: 7.6 MB (7578924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed971e1f00e1850e716e54614727445dada3deb6c85e5654ed157893a2954a9`  
		Last Modified: Fri, 15 May 2026 20:13:42 GMT  
		Size: 178.7 MB (178700407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab32bd7d6b5d491330f76d853b90acfc583421f50c2550e13f399db6f568e66`  
		Last Modified: Fri, 15 May 2026 20:13:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99dc0c4363dc7d76407d6f25fb4e87d840260437ee480e8a0da8802eebd49433`  
		Last Modified: Fri, 15 May 2026 20:13:39 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a720aa38614e97a32ea0557751f1e7fe859748800c95171a83f9732958c2ea09`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bddcaef3f88078d160bf5276028cd8f63c77aa67aa6201cee8fa7b31b7087d`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dafa50616f0afea00586f771e649703b689a6e75edc3399b5ac2355147cc56`  
		Last Modified: Fri, 15 May 2026 20:13:41 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a4b251bd89da4bda7b508dc8cb9a63e51f203d1d9d77361068d9a96ab90aa414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dff045eb8f1bcd3d0282cebae5d93eb266f23daec63dab878c06764f6e3a24`

```dockerfile
```

-	Layers:
	-	`sha256:bce1ec2d6bdf3765133e79faf0fc671eeab796f885cd4dec41b365e5dfd6f041`  
		Last Modified: Fri, 15 May 2026 20:13:38 GMT  
		Size: 26.4 KB (26422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.23`

```console
$ docker pull clickhouse@sha256:120f7787f3c8348f9ef1604576fd8d6dddea0119294ee7ff92aae012bdaf50bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.23` - linux; amd64

```console
$ docker pull clickhouse@sha256:946afdf10ba21ac49d459489d82d8574a5b82cbefd218b2cc7f3676727f819aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229736134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898aced72fee331c70d58a7a8c4e6fed61038c3fd85f6a4524cbc1bad69b78c3`
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
# Fri, 15 May 2026 20:13:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:13:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:13:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:13:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:13:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:13:00 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 20:13:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:24 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6198935e4c55ea3200b58ab56b0f6d7ac7d354295114230da9b28873004449b9`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 7.6 MB (7599209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103bac519b1aadfa46fbb1070f878b621afe21ef9d6b4b4de1cc28d54930111b`  
		Last Modified: Fri, 15 May 2026 20:13:58 GMT  
		Size: 191.5 MB (191530407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6dd08c431ea3aa95018000e2c79f3066878f602748e16f2eb5abb3421120ef`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee09314fe284db58d3694fbd1847ecb85a19fd4040a3084c22e71f0905552444`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a507db5e302556e0de8be987a3db8a9244494face2af3f8930c15c6007e7e0`  
		Last Modified: Fri, 15 May 2026 20:13:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a64d669527cc67773dbefa63c0cc4815c9982f84bb2d5bfc1ad13044e2382aa`  
		Last Modified: Fri, 15 May 2026 20:13:48 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b53c8a06e548ddd945507099dd1ca071ab8279759b9f7685e0463dda8756857`  
		Last Modified: Fri, 15 May 2026 20:13:49 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.23` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2989d8aee1db653f7150490f28d055e4fb0b3efdc7159b58d2da3cbde17cb268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fe4acbafc01d7ea075cc8e580ded2afabbbd75c2c1cc1c3cbf92d47650602d`

```dockerfile
```

-	Layers:
	-	`sha256:86147e4fa707c5fdb59ef96869da702880e173e98db750eebb3ed045a9387e5a`  
		Last Modified: Fri, 15 May 2026 20:13:46 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.23` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0bee4e1b902b0a16a258817c952332ea56e3e3306853e2f68c75c4ab73340259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214755894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555981d8ec9377bac6520f9e41d33bdefd43741c1550c505fce64fdebc5674a4`
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
# Fri, 15 May 2026 20:12:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:41 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:41 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 20:12:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:20 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:20 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:20 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:20 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:20 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:20 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4ba3fd81b78d81cde22f57080242d451e0874560fb2a85e42d60f564d69a4d`  
		Last Modified: Fri, 15 May 2026 20:13:39 GMT  
		Size: 7.6 MB (7578924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed971e1f00e1850e716e54614727445dada3deb6c85e5654ed157893a2954a9`  
		Last Modified: Fri, 15 May 2026 20:13:42 GMT  
		Size: 178.7 MB (178700407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab32bd7d6b5d491330f76d853b90acfc583421f50c2550e13f399db6f568e66`  
		Last Modified: Fri, 15 May 2026 20:13:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99dc0c4363dc7d76407d6f25fb4e87d840260437ee480e8a0da8802eebd49433`  
		Last Modified: Fri, 15 May 2026 20:13:39 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a720aa38614e97a32ea0557751f1e7fe859748800c95171a83f9732958c2ea09`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bddcaef3f88078d160bf5276028cd8f63c77aa67aa6201cee8fa7b31b7087d`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dafa50616f0afea00586f771e649703b689a6e75edc3399b5ac2355147cc56`  
		Last Modified: Fri, 15 May 2026 20:13:41 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.23` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a4b251bd89da4bda7b508dc8cb9a63e51f203d1d9d77361068d9a96ab90aa414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dff045eb8f1bcd3d0282cebae5d93eb266f23daec63dab878c06764f6e3a24`

```dockerfile
```

-	Layers:
	-	`sha256:bce1ec2d6bdf3765133e79faf0fc671eeab796f885cd4dec41b365e5dfd6f041`  
		Last Modified: Fri, 15 May 2026 20:13:38 GMT  
		Size: 26.4 KB (26422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.23-jammy`

```console
$ docker pull clickhouse@sha256:120f7787f3c8348f9ef1604576fd8d6dddea0119294ee7ff92aae012bdaf50bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.23-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:946afdf10ba21ac49d459489d82d8574a5b82cbefd218b2cc7f3676727f819aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229736134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898aced72fee331c70d58a7a8c4e6fed61038c3fd85f6a4524cbc1bad69b78c3`
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
# Fri, 15 May 2026 20:13:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:13:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:13:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:13:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:13:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:13:00 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 20:13:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:24 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6198935e4c55ea3200b58ab56b0f6d7ac7d354295114230da9b28873004449b9`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 7.6 MB (7599209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103bac519b1aadfa46fbb1070f878b621afe21ef9d6b4b4de1cc28d54930111b`  
		Last Modified: Fri, 15 May 2026 20:13:58 GMT  
		Size: 191.5 MB (191530407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6dd08c431ea3aa95018000e2c79f3066878f602748e16f2eb5abb3421120ef`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee09314fe284db58d3694fbd1847ecb85a19fd4040a3084c22e71f0905552444`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a507db5e302556e0de8be987a3db8a9244494face2af3f8930c15c6007e7e0`  
		Last Modified: Fri, 15 May 2026 20:13:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a64d669527cc67773dbefa63c0cc4815c9982f84bb2d5bfc1ad13044e2382aa`  
		Last Modified: Fri, 15 May 2026 20:13:48 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b53c8a06e548ddd945507099dd1ca071ab8279759b9f7685e0463dda8756857`  
		Last Modified: Fri, 15 May 2026 20:13:49 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.23-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2989d8aee1db653f7150490f28d055e4fb0b3efdc7159b58d2da3cbde17cb268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fe4acbafc01d7ea075cc8e580ded2afabbbd75c2c1cc1c3cbf92d47650602d`

```dockerfile
```

-	Layers:
	-	`sha256:86147e4fa707c5fdb59ef96869da702880e173e98db750eebb3ed045a9387e5a`  
		Last Modified: Fri, 15 May 2026 20:13:46 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.23-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0bee4e1b902b0a16a258817c952332ea56e3e3306853e2f68c75c4ab73340259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214755894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555981d8ec9377bac6520f9e41d33bdefd43741c1550c505fce64fdebc5674a4`
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
# Fri, 15 May 2026 20:12:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:41 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:41 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 20:12:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:20 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:20 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:20 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:20 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:20 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:20 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4ba3fd81b78d81cde22f57080242d451e0874560fb2a85e42d60f564d69a4d`  
		Last Modified: Fri, 15 May 2026 20:13:39 GMT  
		Size: 7.6 MB (7578924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed971e1f00e1850e716e54614727445dada3deb6c85e5654ed157893a2954a9`  
		Last Modified: Fri, 15 May 2026 20:13:42 GMT  
		Size: 178.7 MB (178700407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab32bd7d6b5d491330f76d853b90acfc583421f50c2550e13f399db6f568e66`  
		Last Modified: Fri, 15 May 2026 20:13:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99dc0c4363dc7d76407d6f25fb4e87d840260437ee480e8a0da8802eebd49433`  
		Last Modified: Fri, 15 May 2026 20:13:39 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a720aa38614e97a32ea0557751f1e7fe859748800c95171a83f9732958c2ea09`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bddcaef3f88078d160bf5276028cd8f63c77aa67aa6201cee8fa7b31b7087d`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dafa50616f0afea00586f771e649703b689a6e75edc3399b5ac2355147cc56`  
		Last Modified: Fri, 15 May 2026 20:13:41 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.23-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a4b251bd89da4bda7b508dc8cb9a63e51f203d1d9d77361068d9a96ab90aa414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dff045eb8f1bcd3d0282cebae5d93eb266f23daec63dab878c06764f6e3a24`

```dockerfile
```

-	Layers:
	-	`sha256:bce1ec2d6bdf3765133e79faf0fc671eeab796f885cd4dec41b365e5dfd6f041`  
		Last Modified: Fri, 15 May 2026 20:13:38 GMT  
		Size: 26.4 KB (26422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.23.13`

```console
$ docker pull clickhouse@sha256:120f7787f3c8348f9ef1604576fd8d6dddea0119294ee7ff92aae012bdaf50bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.23.13` - linux; amd64

```console
$ docker pull clickhouse@sha256:946afdf10ba21ac49d459489d82d8574a5b82cbefd218b2cc7f3676727f819aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229736134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898aced72fee331c70d58a7a8c4e6fed61038c3fd85f6a4524cbc1bad69b78c3`
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
# Fri, 15 May 2026 20:13:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:13:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:13:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:13:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:13:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:13:00 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 20:13:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:24 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6198935e4c55ea3200b58ab56b0f6d7ac7d354295114230da9b28873004449b9`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 7.6 MB (7599209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103bac519b1aadfa46fbb1070f878b621afe21ef9d6b4b4de1cc28d54930111b`  
		Last Modified: Fri, 15 May 2026 20:13:58 GMT  
		Size: 191.5 MB (191530407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6dd08c431ea3aa95018000e2c79f3066878f602748e16f2eb5abb3421120ef`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee09314fe284db58d3694fbd1847ecb85a19fd4040a3084c22e71f0905552444`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a507db5e302556e0de8be987a3db8a9244494face2af3f8930c15c6007e7e0`  
		Last Modified: Fri, 15 May 2026 20:13:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a64d669527cc67773dbefa63c0cc4815c9982f84bb2d5bfc1ad13044e2382aa`  
		Last Modified: Fri, 15 May 2026 20:13:48 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b53c8a06e548ddd945507099dd1ca071ab8279759b9f7685e0463dda8756857`  
		Last Modified: Fri, 15 May 2026 20:13:49 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.23.13` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2989d8aee1db653f7150490f28d055e4fb0b3efdc7159b58d2da3cbde17cb268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fe4acbafc01d7ea075cc8e580ded2afabbbd75c2c1cc1c3cbf92d47650602d`

```dockerfile
```

-	Layers:
	-	`sha256:86147e4fa707c5fdb59ef96869da702880e173e98db750eebb3ed045a9387e5a`  
		Last Modified: Fri, 15 May 2026 20:13:46 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.23.13` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0bee4e1b902b0a16a258817c952332ea56e3e3306853e2f68c75c4ab73340259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214755894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555981d8ec9377bac6520f9e41d33bdefd43741c1550c505fce64fdebc5674a4`
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
# Fri, 15 May 2026 20:12:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:41 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:41 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 20:12:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:20 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:20 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:20 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:20 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:20 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:20 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4ba3fd81b78d81cde22f57080242d451e0874560fb2a85e42d60f564d69a4d`  
		Last Modified: Fri, 15 May 2026 20:13:39 GMT  
		Size: 7.6 MB (7578924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed971e1f00e1850e716e54614727445dada3deb6c85e5654ed157893a2954a9`  
		Last Modified: Fri, 15 May 2026 20:13:42 GMT  
		Size: 178.7 MB (178700407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab32bd7d6b5d491330f76d853b90acfc583421f50c2550e13f399db6f568e66`  
		Last Modified: Fri, 15 May 2026 20:13:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99dc0c4363dc7d76407d6f25fb4e87d840260437ee480e8a0da8802eebd49433`  
		Last Modified: Fri, 15 May 2026 20:13:39 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a720aa38614e97a32ea0557751f1e7fe859748800c95171a83f9732958c2ea09`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bddcaef3f88078d160bf5276028cd8f63c77aa67aa6201cee8fa7b31b7087d`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dafa50616f0afea00586f771e649703b689a6e75edc3399b5ac2355147cc56`  
		Last Modified: Fri, 15 May 2026 20:13:41 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.23.13` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a4b251bd89da4bda7b508dc8cb9a63e51f203d1d9d77361068d9a96ab90aa414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dff045eb8f1bcd3d0282cebae5d93eb266f23daec63dab878c06764f6e3a24`

```dockerfile
```

-	Layers:
	-	`sha256:bce1ec2d6bdf3765133e79faf0fc671eeab796f885cd4dec41b365e5dfd6f041`  
		Last Modified: Fri, 15 May 2026 20:13:38 GMT  
		Size: 26.4 KB (26422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.23.13-jammy`

```console
$ docker pull clickhouse@sha256:120f7787f3c8348f9ef1604576fd8d6dddea0119294ee7ff92aae012bdaf50bd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.23.13-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:946afdf10ba21ac49d459489d82d8574a5b82cbefd218b2cc7f3676727f819aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229736134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898aced72fee331c70d58a7a8c4e6fed61038c3fd85f6a4524cbc1bad69b78c3`
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
# Fri, 15 May 2026 20:13:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:13:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:13:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:13:00 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:13:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:13:00 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 20:13:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:23 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:24 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:24 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:24 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:24 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:24 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:24 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:24 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6198935e4c55ea3200b58ab56b0f6d7ac7d354295114230da9b28873004449b9`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 7.6 MB (7599209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:103bac519b1aadfa46fbb1070f878b621afe21ef9d6b4b4de1cc28d54930111b`  
		Last Modified: Fri, 15 May 2026 20:13:58 GMT  
		Size: 191.5 MB (191530407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6dd08c431ea3aa95018000e2c79f3066878f602748e16f2eb5abb3421120ef`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee09314fe284db58d3694fbd1847ecb85a19fd4040a3084c22e71f0905552444`  
		Last Modified: Fri, 15 May 2026 20:13:47 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a507db5e302556e0de8be987a3db8a9244494face2af3f8930c15c6007e7e0`  
		Last Modified: Fri, 15 May 2026 20:13:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a64d669527cc67773dbefa63c0cc4815c9982f84bb2d5bfc1ad13044e2382aa`  
		Last Modified: Fri, 15 May 2026 20:13:48 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b53c8a06e548ddd945507099dd1ca071ab8279759b9f7685e0463dda8756857`  
		Last Modified: Fri, 15 May 2026 20:13:49 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.23.13-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2989d8aee1db653f7150490f28d055e4fb0b3efdc7159b58d2da3cbde17cb268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64fe4acbafc01d7ea075cc8e580ded2afabbbd75c2c1cc1c3cbf92d47650602d`

```dockerfile
```

-	Layers:
	-	`sha256:86147e4fa707c5fdb59ef96869da702880e173e98db750eebb3ed045a9387e5a`  
		Last Modified: Fri, 15 May 2026 20:13:46 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.23.13-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0bee4e1b902b0a16a258817c952332ea56e3e3306853e2f68c75c4ab73340259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214755894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:555981d8ec9377bac6520f9e41d33bdefd43741c1550c505fce64fdebc5674a4`
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
# Fri, 15 May 2026 20:12:41 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:41 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:41 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:41 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:41 GMT
ARG VERSION=25.8.23.13
# Fri, 15 May 2026 20:12:41 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:20 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:20 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.23.13 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:20 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:20 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:20 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:20 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:20 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4ba3fd81b78d81cde22f57080242d451e0874560fb2a85e42d60f564d69a4d`  
		Last Modified: Fri, 15 May 2026 20:13:39 GMT  
		Size: 7.6 MB (7578924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed971e1f00e1850e716e54614727445dada3deb6c85e5654ed157893a2954a9`  
		Last Modified: Fri, 15 May 2026 20:13:42 GMT  
		Size: 178.7 MB (178700407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab32bd7d6b5d491330f76d853b90acfc583421f50c2550e13f399db6f568e66`  
		Last Modified: Fri, 15 May 2026 20:13:38 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99dc0c4363dc7d76407d6f25fb4e87d840260437ee480e8a0da8802eebd49433`  
		Last Modified: Fri, 15 May 2026 20:13:39 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a720aa38614e97a32ea0557751f1e7fe859748800c95171a83f9732958c2ea09`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bddcaef3f88078d160bf5276028cd8f63c77aa67aa6201cee8fa7b31b7087d`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dafa50616f0afea00586f771e649703b689a6e75edc3399b5ac2355147cc56`  
		Last Modified: Fri, 15 May 2026 20:13:41 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.23.13-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a4b251bd89da4bda7b508dc8cb9a63e51f203d1d9d77361068d9a96ab90aa414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25dff045eb8f1bcd3d0282cebae5d93eb266f23daec63dab878c06764f6e3a24`

```dockerfile
```

-	Layers:
	-	`sha256:bce1ec2d6bdf3765133e79faf0fc671eeab796f885cd4dec41b365e5dfd6f041`  
		Last Modified: Fri, 15 May 2026 20:13:38 GMT  
		Size: 26.4 KB (26422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2`

```console
$ docker pull clickhouse@sha256:7c66aea153b50e5b87be20eef1198b13d12fc57cf4ed2b24059a558bb32c704d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:3a8a8f5c6513eccef267a9926264bfcdc43c60b7036b0e04db634c9bb4ec1022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253839788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece6afe942c1304dc66f97f0b2c497c245b65b8880a9f77d4979f041a7b82294`
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
# Fri, 15 May 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:26 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:51 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:51 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:51 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:51 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:51 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635cea8c69a909d8de20e5e0edb512b7fd994cc1d919c77bfe6e274df7bb6232`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 7.6 MB (7599244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e05c3664e5d19e8d1aed464b0f1d18da29c676e79473fdca6e16eeb9ef7366`  
		Last Modified: Fri, 15 May 2026 20:13:21 GMT  
		Size: 215.6 MB (215633993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b29cf36294109f87abe437963def616be6aabc239a5bc75e51a2ed582dbacf`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6f21351f6c693818e186507b515d86a329c9706f571875e9588b010d7d0bcb`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8ea03055f21f980ea6897014bee18b3a6630120c13ba154f2c8c93ffa51207`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2731e855ad4d291f07789458bfc8b9f45218e2edf2887e99ea6dc0b08a8e6a36`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb93defba8f79df041abeed3845d9df97c223f6566acdc459ac99443a2d005c`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a8f15e1ee6c9be6740a4696c8681724bdbf4e12d3693c651151a5c90f3e9fe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eaad3d9d4775a3ee14d21d0ef8de22c2cc151f36b37632c272be77417636b98`

```dockerfile
```

-	Layers:
	-	`sha256:6186cb3040452d5d2ad0c9fff9d79a0d6e1f9e2153812c59ea762f329dbbc8f6`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 25.4 KB (25420 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:64d0598da4cb077391b8dc2c1b8b090b5829dafc853e8d83a53940ec34339c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237507042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cfcdf1fa431dfbd33d5f3f2fd8c1cf57dd2f93a5215d7b62cbcff936e8c1ef`
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
# Fri, 15 May 2026 20:12:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:40 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:40 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 20:12:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:13 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32260460890e96d41e5ed382b4fe7320158a3ab51161e24db7a2808b1fedeb45`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 7.6 MB (7578926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7141781f522450deffcca6ecada524c98615ebe83afe918a2aabd7a51e3c066`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 201.5 MB (201451530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a7f1ff8ec6602e060f184163000bda447d2c4c45d3393a1bb5555381b70cb1`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40c385b9e5597597e214a1f754c350a5cb30807da57ce471845f99b938c9150`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8074ed32e4a017803e9d8d5f122d2e907df2803b6da7172f228402769ecdb2`  
		Last Modified: Fri, 15 May 2026 20:13:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284ff1627c83291f44b9e32132d6e4e59d460538dd2db08f6bcfedb8381b3bb0`  
		Last Modified: Fri, 15 May 2026 20:13:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bd1fb222e9a64bd1344422e941ea9d124ea700599c711f7d3386f8fb07b0fe`  
		Last Modified: Fri, 15 May 2026 20:13:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea6ef2ff6cf6f799bee6469803c16632d9c4f653f7249a177d97797281300fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392c7768a6ccc5552f81ed601917133a536073de0a6ae26cf80e68362d60f593`

```dockerfile
```

-	Layers:
	-	`sha256:69f3b8b96999a42b1954e0e3af964910fbac32cac7f9a307d33a5d704c506b4d`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2-jammy`

```console
$ docker pull clickhouse@sha256:7c66aea153b50e5b87be20eef1198b13d12fc57cf4ed2b24059a558bb32c704d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:3a8a8f5c6513eccef267a9926264bfcdc43c60b7036b0e04db634c9bb4ec1022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253839788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece6afe942c1304dc66f97f0b2c497c245b65b8880a9f77d4979f041a7b82294`
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
# Fri, 15 May 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:26 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:51 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:51 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:51 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:51 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:51 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635cea8c69a909d8de20e5e0edb512b7fd994cc1d919c77bfe6e274df7bb6232`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 7.6 MB (7599244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e05c3664e5d19e8d1aed464b0f1d18da29c676e79473fdca6e16eeb9ef7366`  
		Last Modified: Fri, 15 May 2026 20:13:21 GMT  
		Size: 215.6 MB (215633993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b29cf36294109f87abe437963def616be6aabc239a5bc75e51a2ed582dbacf`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6f21351f6c693818e186507b515d86a329c9706f571875e9588b010d7d0bcb`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8ea03055f21f980ea6897014bee18b3a6630120c13ba154f2c8c93ffa51207`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2731e855ad4d291f07789458bfc8b9f45218e2edf2887e99ea6dc0b08a8e6a36`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb93defba8f79df041abeed3845d9df97c223f6566acdc459ac99443a2d005c`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a8f15e1ee6c9be6740a4696c8681724bdbf4e12d3693c651151a5c90f3e9fe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eaad3d9d4775a3ee14d21d0ef8de22c2cc151f36b37632c272be77417636b98`

```dockerfile
```

-	Layers:
	-	`sha256:6186cb3040452d5d2ad0c9fff9d79a0d6e1f9e2153812c59ea762f329dbbc8f6`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 25.4 KB (25420 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:64d0598da4cb077391b8dc2c1b8b090b5829dafc853e8d83a53940ec34339c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237507042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cfcdf1fa431dfbd33d5f3f2fd8c1cf57dd2f93a5215d7b62cbcff936e8c1ef`
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
# Fri, 15 May 2026 20:12:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:40 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:40 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 20:12:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:13 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32260460890e96d41e5ed382b4fe7320158a3ab51161e24db7a2808b1fedeb45`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 7.6 MB (7578926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7141781f522450deffcca6ecada524c98615ebe83afe918a2aabd7a51e3c066`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 201.5 MB (201451530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a7f1ff8ec6602e060f184163000bda447d2c4c45d3393a1bb5555381b70cb1`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40c385b9e5597597e214a1f754c350a5cb30807da57ce471845f99b938c9150`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8074ed32e4a017803e9d8d5f122d2e907df2803b6da7172f228402769ecdb2`  
		Last Modified: Fri, 15 May 2026 20:13:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284ff1627c83291f44b9e32132d6e4e59d460538dd2db08f6bcfedb8381b3bb0`  
		Last Modified: Fri, 15 May 2026 20:13:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bd1fb222e9a64bd1344422e941ea9d124ea700599c711f7d3386f8fb07b0fe`  
		Last Modified: Fri, 15 May 2026 20:13:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea6ef2ff6cf6f799bee6469803c16632d9c4f653f7249a177d97797281300fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392c7768a6ccc5552f81ed601917133a536073de0a6ae26cf80e68362d60f593`

```dockerfile
```

-	Layers:
	-	`sha256:69f3b8b96999a42b1954e0e3af964910fbac32cac7f9a307d33a5d704c506b4d`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.18`

```console
$ docker pull clickhouse@sha256:7c66aea153b50e5b87be20eef1198b13d12fc57cf4ed2b24059a558bb32c704d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.18` - linux; amd64

```console
$ docker pull clickhouse@sha256:3a8a8f5c6513eccef267a9926264bfcdc43c60b7036b0e04db634c9bb4ec1022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253839788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece6afe942c1304dc66f97f0b2c497c245b65b8880a9f77d4979f041a7b82294`
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
# Fri, 15 May 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:26 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:51 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:51 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:51 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:51 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:51 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635cea8c69a909d8de20e5e0edb512b7fd994cc1d919c77bfe6e274df7bb6232`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 7.6 MB (7599244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e05c3664e5d19e8d1aed464b0f1d18da29c676e79473fdca6e16eeb9ef7366`  
		Last Modified: Fri, 15 May 2026 20:13:21 GMT  
		Size: 215.6 MB (215633993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b29cf36294109f87abe437963def616be6aabc239a5bc75e51a2ed582dbacf`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6f21351f6c693818e186507b515d86a329c9706f571875e9588b010d7d0bcb`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8ea03055f21f980ea6897014bee18b3a6630120c13ba154f2c8c93ffa51207`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2731e855ad4d291f07789458bfc8b9f45218e2edf2887e99ea6dc0b08a8e6a36`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb93defba8f79df041abeed3845d9df97c223f6566acdc459ac99443a2d005c`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.18` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a8f15e1ee6c9be6740a4696c8681724bdbf4e12d3693c651151a5c90f3e9fe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eaad3d9d4775a3ee14d21d0ef8de22c2cc151f36b37632c272be77417636b98`

```dockerfile
```

-	Layers:
	-	`sha256:6186cb3040452d5d2ad0c9fff9d79a0d6e1f9e2153812c59ea762f329dbbc8f6`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 25.4 KB (25420 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.18` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:64d0598da4cb077391b8dc2c1b8b090b5829dafc853e8d83a53940ec34339c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237507042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cfcdf1fa431dfbd33d5f3f2fd8c1cf57dd2f93a5215d7b62cbcff936e8c1ef`
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
# Fri, 15 May 2026 20:12:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:40 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:40 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 20:12:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:13 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32260460890e96d41e5ed382b4fe7320158a3ab51161e24db7a2808b1fedeb45`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 7.6 MB (7578926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7141781f522450deffcca6ecada524c98615ebe83afe918a2aabd7a51e3c066`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 201.5 MB (201451530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a7f1ff8ec6602e060f184163000bda447d2c4c45d3393a1bb5555381b70cb1`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40c385b9e5597597e214a1f754c350a5cb30807da57ce471845f99b938c9150`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8074ed32e4a017803e9d8d5f122d2e907df2803b6da7172f228402769ecdb2`  
		Last Modified: Fri, 15 May 2026 20:13:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284ff1627c83291f44b9e32132d6e4e59d460538dd2db08f6bcfedb8381b3bb0`  
		Last Modified: Fri, 15 May 2026 20:13:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bd1fb222e9a64bd1344422e941ea9d124ea700599c711f7d3386f8fb07b0fe`  
		Last Modified: Fri, 15 May 2026 20:13:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.18` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea6ef2ff6cf6f799bee6469803c16632d9c4f653f7249a177d97797281300fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392c7768a6ccc5552f81ed601917133a536073de0a6ae26cf80e68362d60f593`

```dockerfile
```

-	Layers:
	-	`sha256:69f3b8b96999a42b1954e0e3af964910fbac32cac7f9a307d33a5d704c506b4d`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.18-jammy`

```console
$ docker pull clickhouse@sha256:7c66aea153b50e5b87be20eef1198b13d12fc57cf4ed2b24059a558bb32c704d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.18-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:3a8a8f5c6513eccef267a9926264bfcdc43c60b7036b0e04db634c9bb4ec1022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253839788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece6afe942c1304dc66f97f0b2c497c245b65b8880a9f77d4979f041a7b82294`
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
# Fri, 15 May 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:26 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:51 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:51 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:51 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:51 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:51 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635cea8c69a909d8de20e5e0edb512b7fd994cc1d919c77bfe6e274df7bb6232`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 7.6 MB (7599244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e05c3664e5d19e8d1aed464b0f1d18da29c676e79473fdca6e16eeb9ef7366`  
		Last Modified: Fri, 15 May 2026 20:13:21 GMT  
		Size: 215.6 MB (215633993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b29cf36294109f87abe437963def616be6aabc239a5bc75e51a2ed582dbacf`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6f21351f6c693818e186507b515d86a329c9706f571875e9588b010d7d0bcb`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8ea03055f21f980ea6897014bee18b3a6630120c13ba154f2c8c93ffa51207`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2731e855ad4d291f07789458bfc8b9f45218e2edf2887e99ea6dc0b08a8e6a36`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb93defba8f79df041abeed3845d9df97c223f6566acdc459ac99443a2d005c`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.18-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a8f15e1ee6c9be6740a4696c8681724bdbf4e12d3693c651151a5c90f3e9fe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eaad3d9d4775a3ee14d21d0ef8de22c2cc151f36b37632c272be77417636b98`

```dockerfile
```

-	Layers:
	-	`sha256:6186cb3040452d5d2ad0c9fff9d79a0d6e1f9e2153812c59ea762f329dbbc8f6`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 25.4 KB (25420 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.18-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:64d0598da4cb077391b8dc2c1b8b090b5829dafc853e8d83a53940ec34339c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237507042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cfcdf1fa431dfbd33d5f3f2fd8c1cf57dd2f93a5215d7b62cbcff936e8c1ef`
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
# Fri, 15 May 2026 20:12:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:40 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:40 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 20:12:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:13 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32260460890e96d41e5ed382b4fe7320158a3ab51161e24db7a2808b1fedeb45`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 7.6 MB (7578926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7141781f522450deffcca6ecada524c98615ebe83afe918a2aabd7a51e3c066`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 201.5 MB (201451530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a7f1ff8ec6602e060f184163000bda447d2c4c45d3393a1bb5555381b70cb1`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40c385b9e5597597e214a1f754c350a5cb30807da57ce471845f99b938c9150`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8074ed32e4a017803e9d8d5f122d2e907df2803b6da7172f228402769ecdb2`  
		Last Modified: Fri, 15 May 2026 20:13:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284ff1627c83291f44b9e32132d6e4e59d460538dd2db08f6bcfedb8381b3bb0`  
		Last Modified: Fri, 15 May 2026 20:13:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bd1fb222e9a64bd1344422e941ea9d124ea700599c711f7d3386f8fb07b0fe`  
		Last Modified: Fri, 15 May 2026 20:13:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.18-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea6ef2ff6cf6f799bee6469803c16632d9c4f653f7249a177d97797281300fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392c7768a6ccc5552f81ed601917133a536073de0a6ae26cf80e68362d60f593`

```dockerfile
```

-	Layers:
	-	`sha256:69f3b8b96999a42b1954e0e3af964910fbac32cac7f9a307d33a5d704c506b4d`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.18.8`

```console
$ docker pull clickhouse@sha256:7c66aea153b50e5b87be20eef1198b13d12fc57cf4ed2b24059a558bb32c704d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.18.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:3a8a8f5c6513eccef267a9926264bfcdc43c60b7036b0e04db634c9bb4ec1022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253839788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece6afe942c1304dc66f97f0b2c497c245b65b8880a9f77d4979f041a7b82294`
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
# Fri, 15 May 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:26 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:51 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:51 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:51 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:51 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:51 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635cea8c69a909d8de20e5e0edb512b7fd994cc1d919c77bfe6e274df7bb6232`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 7.6 MB (7599244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e05c3664e5d19e8d1aed464b0f1d18da29c676e79473fdca6e16eeb9ef7366`  
		Last Modified: Fri, 15 May 2026 20:13:21 GMT  
		Size: 215.6 MB (215633993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b29cf36294109f87abe437963def616be6aabc239a5bc75e51a2ed582dbacf`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6f21351f6c693818e186507b515d86a329c9706f571875e9588b010d7d0bcb`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8ea03055f21f980ea6897014bee18b3a6630120c13ba154f2c8c93ffa51207`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2731e855ad4d291f07789458bfc8b9f45218e2edf2887e99ea6dc0b08a8e6a36`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb93defba8f79df041abeed3845d9df97c223f6566acdc459ac99443a2d005c`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.18.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a8f15e1ee6c9be6740a4696c8681724bdbf4e12d3693c651151a5c90f3e9fe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eaad3d9d4775a3ee14d21d0ef8de22c2cc151f36b37632c272be77417636b98`

```dockerfile
```

-	Layers:
	-	`sha256:6186cb3040452d5d2ad0c9fff9d79a0d6e1f9e2153812c59ea762f329dbbc8f6`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 25.4 KB (25420 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.18.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:64d0598da4cb077391b8dc2c1b8b090b5829dafc853e8d83a53940ec34339c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237507042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cfcdf1fa431dfbd33d5f3f2fd8c1cf57dd2f93a5215d7b62cbcff936e8c1ef`
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
# Fri, 15 May 2026 20:12:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:40 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:40 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 20:12:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:13 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32260460890e96d41e5ed382b4fe7320158a3ab51161e24db7a2808b1fedeb45`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 7.6 MB (7578926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7141781f522450deffcca6ecada524c98615ebe83afe918a2aabd7a51e3c066`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 201.5 MB (201451530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a7f1ff8ec6602e060f184163000bda447d2c4c45d3393a1bb5555381b70cb1`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40c385b9e5597597e214a1f754c350a5cb30807da57ce471845f99b938c9150`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8074ed32e4a017803e9d8d5f122d2e907df2803b6da7172f228402769ecdb2`  
		Last Modified: Fri, 15 May 2026 20:13:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284ff1627c83291f44b9e32132d6e4e59d460538dd2db08f6bcfedb8381b3bb0`  
		Last Modified: Fri, 15 May 2026 20:13:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bd1fb222e9a64bd1344422e941ea9d124ea700599c711f7d3386f8fb07b0fe`  
		Last Modified: Fri, 15 May 2026 20:13:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.18.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea6ef2ff6cf6f799bee6469803c16632d9c4f653f7249a177d97797281300fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392c7768a6ccc5552f81ed601917133a536073de0a6ae26cf80e68362d60f593`

```dockerfile
```

-	Layers:
	-	`sha256:69f3b8b96999a42b1954e0e3af964910fbac32cac7f9a307d33a5d704c506b4d`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.2.18.8-jammy`

```console
$ docker pull clickhouse@sha256:7c66aea153b50e5b87be20eef1198b13d12fc57cf4ed2b24059a558bb32c704d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.2.18.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:3a8a8f5c6513eccef267a9926264bfcdc43c60b7036b0e04db634c9bb4ec1022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 MB (253839788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ece6afe942c1304dc66f97f0b2c497c245b65b8880a9f77d4979f041a7b82294`
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
# Fri, 15 May 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:26 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:51 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:51 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:51 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:51 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:51 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:51 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635cea8c69a909d8de20e5e0edb512b7fd994cc1d919c77bfe6e274df7bb6232`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 7.6 MB (7599244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e05c3664e5d19e8d1aed464b0f1d18da29c676e79473fdca6e16eeb9ef7366`  
		Last Modified: Fri, 15 May 2026 20:13:21 GMT  
		Size: 215.6 MB (215633993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b29cf36294109f87abe437963def616be6aabc239a5bc75e51a2ed582dbacf`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d6f21351f6c693818e186507b515d86a329c9706f571875e9588b010d7d0bcb`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f8ea03055f21f980ea6897014bee18b3a6630120c13ba154f2c8c93ffa51207`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2731e855ad4d291f07789458bfc8b9f45218e2edf2887e99ea6dc0b08a8e6a36`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb93defba8f79df041abeed3845d9df97c223f6566acdc459ac99443a2d005c`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.18.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a8f15e1ee6c9be6740a4696c8681724bdbf4e12d3693c651151a5c90f3e9fe56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eaad3d9d4775a3ee14d21d0ef8de22c2cc151f36b37632c272be77417636b98`

```dockerfile
```

-	Layers:
	-	`sha256:6186cb3040452d5d2ad0c9fff9d79a0d6e1f9e2153812c59ea762f329dbbc8f6`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 25.4 KB (25420 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.2.18.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:64d0598da4cb077391b8dc2c1b8b090b5829dafc853e8d83a53940ec34339c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.5 MB (237507042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2cfcdf1fa431dfbd33d5f3f2fd8c1cf57dd2f93a5215d7b62cbcff936e8c1ef`
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
# Fri, 15 May 2026 20:12:40 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:40 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:40 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:40 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:40 GMT
ARG VERSION=26.2.18.8
# Fri, 15 May 2026 20:12:40 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:13:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:13:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:13:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:13:13 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:13:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.2.18.8 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:13:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:13:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:13:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:13:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:13:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:13:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32260460890e96d41e5ed382b4fe7320158a3ab51161e24db7a2808b1fedeb45`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 7.6 MB (7578926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7141781f522450deffcca6ecada524c98615ebe83afe918a2aabd7a51e3c066`  
		Last Modified: Fri, 15 May 2026 20:13:40 GMT  
		Size: 201.5 MB (201451530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a7f1ff8ec6602e060f184163000bda447d2c4c45d3393a1bb5555381b70cb1`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40c385b9e5597597e214a1f754c350a5cb30807da57ce471845f99b938c9150`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd8074ed32e4a017803e9d8d5f122d2e907df2803b6da7172f228402769ecdb2`  
		Last Modified: Fri, 15 May 2026 20:13:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284ff1627c83291f44b9e32132d6e4e59d460538dd2db08f6bcfedb8381b3bb0`  
		Last Modified: Fri, 15 May 2026 20:13:37 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bd1fb222e9a64bd1344422e941ea9d124ea700599c711f7d3386f8fb07b0fe`  
		Last Modified: Fri, 15 May 2026 20:13:37 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.2.18.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea6ef2ff6cf6f799bee6469803c16632d9c4f653f7249a177d97797281300fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:392c7768a6ccc5552f81ed601917133a536073de0a6ae26cf80e68362d60f593`

```dockerfile
```

-	Layers:
	-	`sha256:69f3b8b96999a42b1954e0e3af964910fbac32cac7f9a307d33a5d704c506b4d`  
		Last Modified: Fri, 15 May 2026 20:13:35 GMT  
		Size: 25.6 KB (25610 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3`

```console
$ docker pull clickhouse@sha256:6e6c9744ea880affeaeb297eaecdbee62baeaaf5eb93bae4cf0148fc9d707c09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:2930dac41388856da9d9b966af39711497f97ba2fdcec45978177872b53c21f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264805741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03811a854d0a975b5c58dac0a5e4d27c668f3852952dc3e52ea99e9fe4e4bbd1`
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
# Fri, 15 May 2026 20:12:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 20:12:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:50 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:50 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec80bef1e5a351e99527ab0b420e914caab74e3e531bceef4934327c4f6a31e0`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 7.6 MB (7599224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908f29adc9c7f107d4f757e333f49945314c082e5791a8b14a87d708410671aa`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 226.6 MB (226599972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b29cf36294109f87abe437963def616be6aabc239a5bc75e51a2ed582dbacf`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851f83769fc8458a25d883c50e1066b1b53d42c1d4a762c62c2eac5ebe711d46`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec8d122e9799e2989598b33de3df276f05e69167d67142ea81b4144619a0d07`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708419c0879fea53b52186c7bd3acece66e020a9ff5bde8bce01a444408ccb39`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1d37d3c4341b39395f5fffa19e30e3ab30cf525cf8bc82b87acd39cbf63938`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1467897289b8de65cc6ed205db092604b6d36885ebadd2ae6756f20b514e9c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b818e686cf2d9d43587b1771e162941c4d0dc43e0e3ff9499dd15eccfe664bc4`

```dockerfile
```

-	Layers:
	-	`sha256:24290da259fe55d62538b2a30d56810cf0b55135ad34b8c4b0d81cd2bebc8a6a`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a816656225b782366b2967b8dd016c1e9c295b68c0ddde1e03c43ced212fb7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f691bb66d68d39169b385477421c3257d94f756b3e48dd01ac5323bc1af4680`
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
# Fri, 15 May 2026 20:12:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 20:12:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22b6f69def2c37af88fc1fdaab0e3ae42f6475bb059426956176ada924fccf7`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 7.6 MB (7578915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc438280275d64a01ed12b00c30f0ae52a24a55ca77c5f8b7ec62bac184905e`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 210.2 MB (210218560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d7d3a01b0dee6dcf1511a6e2cc0ac78c4ee6b48902eb2a4ecf9e1ab7f38d8c`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984c732d979e9edcb529eebdf77a55130075a835b64461d9986a222330bfed31`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b5320ebe49fe6eaae20a8c76724123d5efa6c5302b504ff8d4b053b7ec0157`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4c8f9ed565b086aafd08dcbbad21677f168d50526223bc8e19f02403aa334c`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b472a2c941fbbb6d9bc1f14942cac6e17fc6713f8aa25c39ac117b15b2de7440`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e11af04de005418a512f2a7e0715800e2e7956445fa4576c5f0a620bc8aeab7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d967a3e529594de19f6bd9f1b0bfe1fb85646da773f33e30db8a4b1a4fa9b08`

```dockerfile
```

-	Layers:
	-	`sha256:2b2361287b8649808793fc5d1dafd594ff7ed3a7cd5346173cfd72c29da55088`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3-jammy`

```console
$ docker pull clickhouse@sha256:6e6c9744ea880affeaeb297eaecdbee62baeaaf5eb93bae4cf0148fc9d707c09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:2930dac41388856da9d9b966af39711497f97ba2fdcec45978177872b53c21f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264805741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03811a854d0a975b5c58dac0a5e4d27c668f3852952dc3e52ea99e9fe4e4bbd1`
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
# Fri, 15 May 2026 20:12:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 20:12:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:50 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:50 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec80bef1e5a351e99527ab0b420e914caab74e3e531bceef4934327c4f6a31e0`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 7.6 MB (7599224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908f29adc9c7f107d4f757e333f49945314c082e5791a8b14a87d708410671aa`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 226.6 MB (226599972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b29cf36294109f87abe437963def616be6aabc239a5bc75e51a2ed582dbacf`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851f83769fc8458a25d883c50e1066b1b53d42c1d4a762c62c2eac5ebe711d46`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec8d122e9799e2989598b33de3df276f05e69167d67142ea81b4144619a0d07`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708419c0879fea53b52186c7bd3acece66e020a9ff5bde8bce01a444408ccb39`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1d37d3c4341b39395f5fffa19e30e3ab30cf525cf8bc82b87acd39cbf63938`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1467897289b8de65cc6ed205db092604b6d36885ebadd2ae6756f20b514e9c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b818e686cf2d9d43587b1771e162941c4d0dc43e0e3ff9499dd15eccfe664bc4`

```dockerfile
```

-	Layers:
	-	`sha256:24290da259fe55d62538b2a30d56810cf0b55135ad34b8c4b0d81cd2bebc8a6a`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a816656225b782366b2967b8dd016c1e9c295b68c0ddde1e03c43ced212fb7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f691bb66d68d39169b385477421c3257d94f756b3e48dd01ac5323bc1af4680`
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
# Fri, 15 May 2026 20:12:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 20:12:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22b6f69def2c37af88fc1fdaab0e3ae42f6475bb059426956176ada924fccf7`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 7.6 MB (7578915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc438280275d64a01ed12b00c30f0ae52a24a55ca77c5f8b7ec62bac184905e`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 210.2 MB (210218560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d7d3a01b0dee6dcf1511a6e2cc0ac78c4ee6b48902eb2a4ecf9e1ab7f38d8c`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984c732d979e9edcb529eebdf77a55130075a835b64461d9986a222330bfed31`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b5320ebe49fe6eaae20a8c76724123d5efa6c5302b504ff8d4b053b7ec0157`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4c8f9ed565b086aafd08dcbbad21677f168d50526223bc8e19f02403aa334c`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b472a2c941fbbb6d9bc1f14942cac6e17fc6713f8aa25c39ac117b15b2de7440`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e11af04de005418a512f2a7e0715800e2e7956445fa4576c5f0a620bc8aeab7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d967a3e529594de19f6bd9f1b0bfe1fb85646da773f33e30db8a4b1a4fa9b08`

```dockerfile
```

-	Layers:
	-	`sha256:2b2361287b8649808793fc5d1dafd594ff7ed3a7cd5346173cfd72c29da55088`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.10`

```console
$ docker pull clickhouse@sha256:6e6c9744ea880affeaeb297eaecdbee62baeaaf5eb93bae4cf0148fc9d707c09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:2930dac41388856da9d9b966af39711497f97ba2fdcec45978177872b53c21f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264805741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03811a854d0a975b5c58dac0a5e4d27c668f3852952dc3e52ea99e9fe4e4bbd1`
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
# Fri, 15 May 2026 20:12:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 20:12:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:50 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:50 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec80bef1e5a351e99527ab0b420e914caab74e3e531bceef4934327c4f6a31e0`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 7.6 MB (7599224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908f29adc9c7f107d4f757e333f49945314c082e5791a8b14a87d708410671aa`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 226.6 MB (226599972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b29cf36294109f87abe437963def616be6aabc239a5bc75e51a2ed582dbacf`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851f83769fc8458a25d883c50e1066b1b53d42c1d4a762c62c2eac5ebe711d46`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec8d122e9799e2989598b33de3df276f05e69167d67142ea81b4144619a0d07`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708419c0879fea53b52186c7bd3acece66e020a9ff5bde8bce01a444408ccb39`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1d37d3c4341b39395f5fffa19e30e3ab30cf525cf8bc82b87acd39cbf63938`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1467897289b8de65cc6ed205db092604b6d36885ebadd2ae6756f20b514e9c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b818e686cf2d9d43587b1771e162941c4d0dc43e0e3ff9499dd15eccfe664bc4`

```dockerfile
```

-	Layers:
	-	`sha256:24290da259fe55d62538b2a30d56810cf0b55135ad34b8c4b0d81cd2bebc8a6a`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a816656225b782366b2967b8dd016c1e9c295b68c0ddde1e03c43ced212fb7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f691bb66d68d39169b385477421c3257d94f756b3e48dd01ac5323bc1af4680`
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
# Fri, 15 May 2026 20:12:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 20:12:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22b6f69def2c37af88fc1fdaab0e3ae42f6475bb059426956176ada924fccf7`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 7.6 MB (7578915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc438280275d64a01ed12b00c30f0ae52a24a55ca77c5f8b7ec62bac184905e`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 210.2 MB (210218560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d7d3a01b0dee6dcf1511a6e2cc0ac78c4ee6b48902eb2a4ecf9e1ab7f38d8c`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984c732d979e9edcb529eebdf77a55130075a835b64461d9986a222330bfed31`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b5320ebe49fe6eaae20a8c76724123d5efa6c5302b504ff8d4b053b7ec0157`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4c8f9ed565b086aafd08dcbbad21677f168d50526223bc8e19f02403aa334c`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b472a2c941fbbb6d9bc1f14942cac6e17fc6713f8aa25c39ac117b15b2de7440`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e11af04de005418a512f2a7e0715800e2e7956445fa4576c5f0a620bc8aeab7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d967a3e529594de19f6bd9f1b0bfe1fb85646da773f33e30db8a4b1a4fa9b08`

```dockerfile
```

-	Layers:
	-	`sha256:2b2361287b8649808793fc5d1dafd594ff7ed3a7cd5346173cfd72c29da55088`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.10-jammy`

```console
$ docker pull clickhouse@sha256:6e6c9744ea880affeaeb297eaecdbee62baeaaf5eb93bae4cf0148fc9d707c09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.10-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:2930dac41388856da9d9b966af39711497f97ba2fdcec45978177872b53c21f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264805741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03811a854d0a975b5c58dac0a5e4d27c668f3852952dc3e52ea99e9fe4e4bbd1`
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
# Fri, 15 May 2026 20:12:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 20:12:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:50 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:50 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec80bef1e5a351e99527ab0b420e914caab74e3e531bceef4934327c4f6a31e0`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 7.6 MB (7599224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908f29adc9c7f107d4f757e333f49945314c082e5791a8b14a87d708410671aa`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 226.6 MB (226599972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b29cf36294109f87abe437963def616be6aabc239a5bc75e51a2ed582dbacf`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851f83769fc8458a25d883c50e1066b1b53d42c1d4a762c62c2eac5ebe711d46`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec8d122e9799e2989598b33de3df276f05e69167d67142ea81b4144619a0d07`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708419c0879fea53b52186c7bd3acece66e020a9ff5bde8bce01a444408ccb39`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1d37d3c4341b39395f5fffa19e30e3ab30cf525cf8bc82b87acd39cbf63938`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1467897289b8de65cc6ed205db092604b6d36885ebadd2ae6756f20b514e9c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b818e686cf2d9d43587b1771e162941c4d0dc43e0e3ff9499dd15eccfe664bc4`

```dockerfile
```

-	Layers:
	-	`sha256:24290da259fe55d62538b2a30d56810cf0b55135ad34b8c4b0d81cd2bebc8a6a`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.10-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a816656225b782366b2967b8dd016c1e9c295b68c0ddde1e03c43ced212fb7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f691bb66d68d39169b385477421c3257d94f756b3e48dd01ac5323bc1af4680`
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
# Fri, 15 May 2026 20:12:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 20:12:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22b6f69def2c37af88fc1fdaab0e3ae42f6475bb059426956176ada924fccf7`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 7.6 MB (7578915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc438280275d64a01ed12b00c30f0ae52a24a55ca77c5f8b7ec62bac184905e`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 210.2 MB (210218560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d7d3a01b0dee6dcf1511a6e2cc0ac78c4ee6b48902eb2a4ecf9e1ab7f38d8c`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984c732d979e9edcb529eebdf77a55130075a835b64461d9986a222330bfed31`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b5320ebe49fe6eaae20a8c76724123d5efa6c5302b504ff8d4b053b7ec0157`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4c8f9ed565b086aafd08dcbbad21677f168d50526223bc8e19f02403aa334c`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b472a2c941fbbb6d9bc1f14942cac6e17fc6713f8aa25c39ac117b15b2de7440`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e11af04de005418a512f2a7e0715800e2e7956445fa4576c5f0a620bc8aeab7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d967a3e529594de19f6bd9f1b0bfe1fb85646da773f33e30db8a4b1a4fa9b08`

```dockerfile
```

-	Layers:
	-	`sha256:2b2361287b8649808793fc5d1dafd594ff7ed3a7cd5346173cfd72c29da55088`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.10.62`

```console
$ docker pull clickhouse@sha256:6e6c9744ea880affeaeb297eaecdbee62baeaaf5eb93bae4cf0148fc9d707c09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.10.62` - linux; amd64

```console
$ docker pull clickhouse@sha256:2930dac41388856da9d9b966af39711497f97ba2fdcec45978177872b53c21f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264805741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03811a854d0a975b5c58dac0a5e4d27c668f3852952dc3e52ea99e9fe4e4bbd1`
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
# Fri, 15 May 2026 20:12:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 20:12:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:50 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:50 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec80bef1e5a351e99527ab0b420e914caab74e3e531bceef4934327c4f6a31e0`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 7.6 MB (7599224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908f29adc9c7f107d4f757e333f49945314c082e5791a8b14a87d708410671aa`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 226.6 MB (226599972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b29cf36294109f87abe437963def616be6aabc239a5bc75e51a2ed582dbacf`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851f83769fc8458a25d883c50e1066b1b53d42c1d4a762c62c2eac5ebe711d46`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec8d122e9799e2989598b33de3df276f05e69167d67142ea81b4144619a0d07`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708419c0879fea53b52186c7bd3acece66e020a9ff5bde8bce01a444408ccb39`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1d37d3c4341b39395f5fffa19e30e3ab30cf525cf8bc82b87acd39cbf63938`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.10.62` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1467897289b8de65cc6ed205db092604b6d36885ebadd2ae6756f20b514e9c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b818e686cf2d9d43587b1771e162941c4d0dc43e0e3ff9499dd15eccfe664bc4`

```dockerfile
```

-	Layers:
	-	`sha256:24290da259fe55d62538b2a30d56810cf0b55135ad34b8c4b0d81cd2bebc8a6a`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.10.62` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a816656225b782366b2967b8dd016c1e9c295b68c0ddde1e03c43ced212fb7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f691bb66d68d39169b385477421c3257d94f756b3e48dd01ac5323bc1af4680`
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
# Fri, 15 May 2026 20:12:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 20:12:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22b6f69def2c37af88fc1fdaab0e3ae42f6475bb059426956176ada924fccf7`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 7.6 MB (7578915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc438280275d64a01ed12b00c30f0ae52a24a55ca77c5f8b7ec62bac184905e`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 210.2 MB (210218560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d7d3a01b0dee6dcf1511a6e2cc0ac78c4ee6b48902eb2a4ecf9e1ab7f38d8c`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984c732d979e9edcb529eebdf77a55130075a835b64461d9986a222330bfed31`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b5320ebe49fe6eaae20a8c76724123d5efa6c5302b504ff8d4b053b7ec0157`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4c8f9ed565b086aafd08dcbbad21677f168d50526223bc8e19f02403aa334c`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b472a2c941fbbb6d9bc1f14942cac6e17fc6713f8aa25c39ac117b15b2de7440`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.10.62` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e11af04de005418a512f2a7e0715800e2e7956445fa4576c5f0a620bc8aeab7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d967a3e529594de19f6bd9f1b0bfe1fb85646da773f33e30db8a4b1a4fa9b08`

```dockerfile
```

-	Layers:
	-	`sha256:2b2361287b8649808793fc5d1dafd594ff7ed3a7cd5346173cfd72c29da55088`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.10.62-jammy`

```console
$ docker pull clickhouse@sha256:6e6c9744ea880affeaeb297eaecdbee62baeaaf5eb93bae4cf0148fc9d707c09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.10.62-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:2930dac41388856da9d9b966af39711497f97ba2fdcec45978177872b53c21f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264805741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03811a854d0a975b5c58dac0a5e4d27c668f3852952dc3e52ea99e9fe4e4bbd1`
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
# Fri, 15 May 2026 20:12:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 20:12:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:50 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:50 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec80bef1e5a351e99527ab0b420e914caab74e3e531bceef4934327c4f6a31e0`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 7.6 MB (7599224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908f29adc9c7f107d4f757e333f49945314c082e5791a8b14a87d708410671aa`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 226.6 MB (226599972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b29cf36294109f87abe437963def616be6aabc239a5bc75e51a2ed582dbacf`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851f83769fc8458a25d883c50e1066b1b53d42c1d4a762c62c2eac5ebe711d46`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec8d122e9799e2989598b33de3df276f05e69167d67142ea81b4144619a0d07`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708419c0879fea53b52186c7bd3acece66e020a9ff5bde8bce01a444408ccb39`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1d37d3c4341b39395f5fffa19e30e3ab30cf525cf8bc82b87acd39cbf63938`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.10.62-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1467897289b8de65cc6ed205db092604b6d36885ebadd2ae6756f20b514e9c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b818e686cf2d9d43587b1771e162941c4d0dc43e0e3ff9499dd15eccfe664bc4`

```dockerfile
```

-	Layers:
	-	`sha256:24290da259fe55d62538b2a30d56810cf0b55135ad34b8c4b0d81cd2bebc8a6a`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.10.62-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a816656225b782366b2967b8dd016c1e9c295b68c0ddde1e03c43ced212fb7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f691bb66d68d39169b385477421c3257d94f756b3e48dd01ac5323bc1af4680`
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
# Fri, 15 May 2026 20:12:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 20:12:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22b6f69def2c37af88fc1fdaab0e3ae42f6475bb059426956176ada924fccf7`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 7.6 MB (7578915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc438280275d64a01ed12b00c30f0ae52a24a55ca77c5f8b7ec62bac184905e`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 210.2 MB (210218560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d7d3a01b0dee6dcf1511a6e2cc0ac78c4ee6b48902eb2a4ecf9e1ab7f38d8c`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984c732d979e9edcb529eebdf77a55130075a835b64461d9986a222330bfed31`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b5320ebe49fe6eaae20a8c76724123d5efa6c5302b504ff8d4b053b7ec0157`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4c8f9ed565b086aafd08dcbbad21677f168d50526223bc8e19f02403aa334c`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b472a2c941fbbb6d9bc1f14942cac6e17fc6713f8aa25c39ac117b15b2de7440`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.10.62-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e11af04de005418a512f2a7e0715800e2e7956445fa4576c5f0a620bc8aeab7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d967a3e529594de19f6bd9f1b0bfe1fb85646da773f33e30db8a4b1a4fa9b08`

```dockerfile
```

-	Layers:
	-	`sha256:2b2361287b8649808793fc5d1dafd594ff7ed3a7cd5346173cfd72c29da55088`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4`

```console
$ docker pull clickhouse@sha256:1af0a59ee14edcfe26343e5cea750505dcbe5061040e75f74563cf48c5a0223a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:eac3c18fa7fa69102d117807104bfd5d1a861b20de1cbbc97d38c0e0978aa9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257125149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ceac7d4db2314728d863114214cc142d28dec4486f574a8a822d8b4a13569d`
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
# Fri, 15 May 2026 20:12:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:04 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 20:12:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:29 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:29 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:29 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043da6b091b2130a64745708f3a86762248defdeb9e191368684b156a54db92a`  
		Last Modified: Fri, 15 May 2026 20:12:56 GMT  
		Size: 7.6 MB (7599186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f958db428686e7102bab50d7f199039d9dcd3174bdc7f3789f0e8d87b2d224`  
		Last Modified: Fri, 15 May 2026 20:13:00 GMT  
		Size: 218.9 MB (218919423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2c0f72094d39dfc7e1df290032419a048617b3c7d9008e101d3270e1bde4aa`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8bd4b70d37a12e0f9dcb0bcd6e607999215ae53796551b5b992db4a8a313a9`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e87b8b9173df45744529ff926d597f271fc4c82840de7e592db634c2bba612`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421779253a20a914c8bee0741aaee2cb8034eca79af4ced56e4a76f24c164bee`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e4599c0aad31551fdedb5cf061222bc3ca5725173e18292bc922f85af11c7`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e3a42000b3c0300af626f7ef34ef6c32fbeb9e22ad12b1ca4f8c626bd992dd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb45be40468acd598cab3f9dec62c1d20b363b8acde345e5f90cc1395f41a096`

```dockerfile
```

-	Layers:
	-	`sha256:890676a1266c1e4292517dab5d1e07fc5dca3db970553b5f182fca34932ce481`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 26.8 KB (26829 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d678ab47544c418bc60e2d8ee4f26efb87139ed9cb15b7b926be621a0fabaae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240933861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2a78dcce188b947435513ded71d2505548a3baa8bc5758f2b96e960118a8d5`
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
# Fri, 15 May 2026 20:12:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:17 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 20:12:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:46 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:46 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:46 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:46 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:46 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:46 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce635e7d01d2f3aa4cdc0e29d5ce1e1fc8db99b945439b91cbac2e10db90516`  
		Last Modified: Fri, 15 May 2026 20:13:07 GMT  
		Size: 7.6 MB (7578887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86418539472f4360479981496210d0060c38b189980bb1b74f793fce27950ca`  
		Last Modified: Fri, 15 May 2026 20:13:11 GMT  
		Size: 204.9 MB (204878380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837d157f50a0bdb54f3b0c64e656e4baeb48fd540a8b97b8a0a162fb2064d260`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0866f7d3821c6d116aa678b8de1b26f43a2fa8b261ccd7f14cefa2bced6938`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efb278e5009015a7dc5ec9e3deb460b4e0a333f6faf2282e777ef3c48eb4958`  
		Last Modified: Fri, 15 May 2026 20:13:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579fa624037cb75e2fc16f005552ce2f0e0ba5b9e145884aa21b0d4ec92cbe49`  
		Last Modified: Fri, 15 May 2026 20:13:08 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8b4d0234cba88deaf42387b52c151fc7c3594caad69a1fe88685397c9b9997`  
		Last Modified: Fri, 15 May 2026 20:13:08 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f895599d0d0dce9ca4ccb64d9b54cbc2b2d2f283b7d59c97f63c0b20a0ebff95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b34e766d4a4fa200c55507d11bef01d6567525ce2015d2833b204fe71752c0d`

```dockerfile
```

-	Layers:
	-	`sha256:192a3ef7cc75ba46257f63cb62d15be7934d2590b59ce807632bbc7b2d1c3e4e`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 27.0 KB (27042 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4-jammy`

```console
$ docker pull clickhouse@sha256:1af0a59ee14edcfe26343e5cea750505dcbe5061040e75f74563cf48c5a0223a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:eac3c18fa7fa69102d117807104bfd5d1a861b20de1cbbc97d38c0e0978aa9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257125149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ceac7d4db2314728d863114214cc142d28dec4486f574a8a822d8b4a13569d`
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
# Fri, 15 May 2026 20:12:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:04 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 20:12:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:29 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:29 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:29 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043da6b091b2130a64745708f3a86762248defdeb9e191368684b156a54db92a`  
		Last Modified: Fri, 15 May 2026 20:12:56 GMT  
		Size: 7.6 MB (7599186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f958db428686e7102bab50d7f199039d9dcd3174bdc7f3789f0e8d87b2d224`  
		Last Modified: Fri, 15 May 2026 20:13:00 GMT  
		Size: 218.9 MB (218919423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2c0f72094d39dfc7e1df290032419a048617b3c7d9008e101d3270e1bde4aa`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8bd4b70d37a12e0f9dcb0bcd6e607999215ae53796551b5b992db4a8a313a9`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e87b8b9173df45744529ff926d597f271fc4c82840de7e592db634c2bba612`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421779253a20a914c8bee0741aaee2cb8034eca79af4ced56e4a76f24c164bee`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e4599c0aad31551fdedb5cf061222bc3ca5725173e18292bc922f85af11c7`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e3a42000b3c0300af626f7ef34ef6c32fbeb9e22ad12b1ca4f8c626bd992dd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb45be40468acd598cab3f9dec62c1d20b363b8acde345e5f90cc1395f41a096`

```dockerfile
```

-	Layers:
	-	`sha256:890676a1266c1e4292517dab5d1e07fc5dca3db970553b5f182fca34932ce481`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 26.8 KB (26829 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d678ab47544c418bc60e2d8ee4f26efb87139ed9cb15b7b926be621a0fabaae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240933861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2a78dcce188b947435513ded71d2505548a3baa8bc5758f2b96e960118a8d5`
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
# Fri, 15 May 2026 20:12:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:17 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 20:12:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:46 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:46 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:46 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:46 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:46 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:46 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce635e7d01d2f3aa4cdc0e29d5ce1e1fc8db99b945439b91cbac2e10db90516`  
		Last Modified: Fri, 15 May 2026 20:13:07 GMT  
		Size: 7.6 MB (7578887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86418539472f4360479981496210d0060c38b189980bb1b74f793fce27950ca`  
		Last Modified: Fri, 15 May 2026 20:13:11 GMT  
		Size: 204.9 MB (204878380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837d157f50a0bdb54f3b0c64e656e4baeb48fd540a8b97b8a0a162fb2064d260`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0866f7d3821c6d116aa678b8de1b26f43a2fa8b261ccd7f14cefa2bced6938`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efb278e5009015a7dc5ec9e3deb460b4e0a333f6faf2282e777ef3c48eb4958`  
		Last Modified: Fri, 15 May 2026 20:13:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579fa624037cb75e2fc16f005552ce2f0e0ba5b9e145884aa21b0d4ec92cbe49`  
		Last Modified: Fri, 15 May 2026 20:13:08 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8b4d0234cba88deaf42387b52c151fc7c3594caad69a1fe88685397c9b9997`  
		Last Modified: Fri, 15 May 2026 20:13:08 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f895599d0d0dce9ca4ccb64d9b54cbc2b2d2f283b7d59c97f63c0b20a0ebff95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b34e766d4a4fa200c55507d11bef01d6567525ce2015d2833b204fe71752c0d`

```dockerfile
```

-	Layers:
	-	`sha256:192a3ef7cc75ba46257f63cb62d15be7934d2590b59ce807632bbc7b2d1c3e4e`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 27.0 KB (27042 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4.2`

```console
$ docker pull clickhouse@sha256:1af0a59ee14edcfe26343e5cea750505dcbe5061040e75f74563cf48c5a0223a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:eac3c18fa7fa69102d117807104bfd5d1a861b20de1cbbc97d38c0e0978aa9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257125149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ceac7d4db2314728d863114214cc142d28dec4486f574a8a822d8b4a13569d`
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
# Fri, 15 May 2026 20:12:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:04 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 20:12:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:29 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:29 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:29 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043da6b091b2130a64745708f3a86762248defdeb9e191368684b156a54db92a`  
		Last Modified: Fri, 15 May 2026 20:12:56 GMT  
		Size: 7.6 MB (7599186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f958db428686e7102bab50d7f199039d9dcd3174bdc7f3789f0e8d87b2d224`  
		Last Modified: Fri, 15 May 2026 20:13:00 GMT  
		Size: 218.9 MB (218919423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2c0f72094d39dfc7e1df290032419a048617b3c7d9008e101d3270e1bde4aa`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8bd4b70d37a12e0f9dcb0bcd6e607999215ae53796551b5b992db4a8a313a9`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e87b8b9173df45744529ff926d597f271fc4c82840de7e592db634c2bba612`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421779253a20a914c8bee0741aaee2cb8034eca79af4ced56e4a76f24c164bee`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e4599c0aad31551fdedb5cf061222bc3ca5725173e18292bc922f85af11c7`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e3a42000b3c0300af626f7ef34ef6c32fbeb9e22ad12b1ca4f8c626bd992dd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb45be40468acd598cab3f9dec62c1d20b363b8acde345e5f90cc1395f41a096`

```dockerfile
```

-	Layers:
	-	`sha256:890676a1266c1e4292517dab5d1e07fc5dca3db970553b5f182fca34932ce481`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 26.8 KB (26829 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d678ab47544c418bc60e2d8ee4f26efb87139ed9cb15b7b926be621a0fabaae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240933861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2a78dcce188b947435513ded71d2505548a3baa8bc5758f2b96e960118a8d5`
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
# Fri, 15 May 2026 20:12:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:17 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 20:12:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:46 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:46 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:46 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:46 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:46 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:46 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce635e7d01d2f3aa4cdc0e29d5ce1e1fc8db99b945439b91cbac2e10db90516`  
		Last Modified: Fri, 15 May 2026 20:13:07 GMT  
		Size: 7.6 MB (7578887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86418539472f4360479981496210d0060c38b189980bb1b74f793fce27950ca`  
		Last Modified: Fri, 15 May 2026 20:13:11 GMT  
		Size: 204.9 MB (204878380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837d157f50a0bdb54f3b0c64e656e4baeb48fd540a8b97b8a0a162fb2064d260`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0866f7d3821c6d116aa678b8de1b26f43a2fa8b261ccd7f14cefa2bced6938`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efb278e5009015a7dc5ec9e3deb460b4e0a333f6faf2282e777ef3c48eb4958`  
		Last Modified: Fri, 15 May 2026 20:13:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579fa624037cb75e2fc16f005552ce2f0e0ba5b9e145884aa21b0d4ec92cbe49`  
		Last Modified: Fri, 15 May 2026 20:13:08 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8b4d0234cba88deaf42387b52c151fc7c3594caad69a1fe88685397c9b9997`  
		Last Modified: Fri, 15 May 2026 20:13:08 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f895599d0d0dce9ca4ccb64d9b54cbc2b2d2f283b7d59c97f63c0b20a0ebff95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b34e766d4a4fa200c55507d11bef01d6567525ce2015d2833b204fe71752c0d`

```dockerfile
```

-	Layers:
	-	`sha256:192a3ef7cc75ba46257f63cb62d15be7934d2590b59ce807632bbc7b2d1c3e4e`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 27.0 KB (27042 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4.2-jammy`

```console
$ docker pull clickhouse@sha256:1af0a59ee14edcfe26343e5cea750505dcbe5061040e75f74563cf48c5a0223a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:eac3c18fa7fa69102d117807104bfd5d1a861b20de1cbbc97d38c0e0978aa9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257125149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ceac7d4db2314728d863114214cc142d28dec4486f574a8a822d8b4a13569d`
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
# Fri, 15 May 2026 20:12:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:04 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 20:12:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:29 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:29 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:29 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043da6b091b2130a64745708f3a86762248defdeb9e191368684b156a54db92a`  
		Last Modified: Fri, 15 May 2026 20:12:56 GMT  
		Size: 7.6 MB (7599186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f958db428686e7102bab50d7f199039d9dcd3174bdc7f3789f0e8d87b2d224`  
		Last Modified: Fri, 15 May 2026 20:13:00 GMT  
		Size: 218.9 MB (218919423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2c0f72094d39dfc7e1df290032419a048617b3c7d9008e101d3270e1bde4aa`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8bd4b70d37a12e0f9dcb0bcd6e607999215ae53796551b5b992db4a8a313a9`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e87b8b9173df45744529ff926d597f271fc4c82840de7e592db634c2bba612`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421779253a20a914c8bee0741aaee2cb8034eca79af4ced56e4a76f24c164bee`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e4599c0aad31551fdedb5cf061222bc3ca5725173e18292bc922f85af11c7`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e3a42000b3c0300af626f7ef34ef6c32fbeb9e22ad12b1ca4f8c626bd992dd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb45be40468acd598cab3f9dec62c1d20b363b8acde345e5f90cc1395f41a096`

```dockerfile
```

-	Layers:
	-	`sha256:890676a1266c1e4292517dab5d1e07fc5dca3db970553b5f182fca34932ce481`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 26.8 KB (26829 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d678ab47544c418bc60e2d8ee4f26efb87139ed9cb15b7b926be621a0fabaae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240933861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2a78dcce188b947435513ded71d2505548a3baa8bc5758f2b96e960118a8d5`
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
# Fri, 15 May 2026 20:12:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:17 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 20:12:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:46 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:46 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:46 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:46 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:46 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:46 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce635e7d01d2f3aa4cdc0e29d5ce1e1fc8db99b945439b91cbac2e10db90516`  
		Last Modified: Fri, 15 May 2026 20:13:07 GMT  
		Size: 7.6 MB (7578887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86418539472f4360479981496210d0060c38b189980bb1b74f793fce27950ca`  
		Last Modified: Fri, 15 May 2026 20:13:11 GMT  
		Size: 204.9 MB (204878380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837d157f50a0bdb54f3b0c64e656e4baeb48fd540a8b97b8a0a162fb2064d260`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0866f7d3821c6d116aa678b8de1b26f43a2fa8b261ccd7f14cefa2bced6938`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efb278e5009015a7dc5ec9e3deb460b4e0a333f6faf2282e777ef3c48eb4958`  
		Last Modified: Fri, 15 May 2026 20:13:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579fa624037cb75e2fc16f005552ce2f0e0ba5b9e145884aa21b0d4ec92cbe49`  
		Last Modified: Fri, 15 May 2026 20:13:08 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8b4d0234cba88deaf42387b52c151fc7c3594caad69a1fe88685397c9b9997`  
		Last Modified: Fri, 15 May 2026 20:13:08 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f895599d0d0dce9ca4ccb64d9b54cbc2b2d2f283b7d59c97f63c0b20a0ebff95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b34e766d4a4fa200c55507d11bef01d6567525ce2015d2833b204fe71752c0d`

```dockerfile
```

-	Layers:
	-	`sha256:192a3ef7cc75ba46257f63cb62d15be7934d2590b59ce807632bbc7b2d1c3e4e`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 27.0 KB (27042 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4.2.10`

```console
$ docker pull clickhouse@sha256:1af0a59ee14edcfe26343e5cea750505dcbe5061040e75f74563cf48c5a0223a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4.2.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:eac3c18fa7fa69102d117807104bfd5d1a861b20de1cbbc97d38c0e0978aa9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257125149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ceac7d4db2314728d863114214cc142d28dec4486f574a8a822d8b4a13569d`
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
# Fri, 15 May 2026 20:12:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:04 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 20:12:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:29 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:29 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:29 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043da6b091b2130a64745708f3a86762248defdeb9e191368684b156a54db92a`  
		Last Modified: Fri, 15 May 2026 20:12:56 GMT  
		Size: 7.6 MB (7599186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f958db428686e7102bab50d7f199039d9dcd3174bdc7f3789f0e8d87b2d224`  
		Last Modified: Fri, 15 May 2026 20:13:00 GMT  
		Size: 218.9 MB (218919423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2c0f72094d39dfc7e1df290032419a048617b3c7d9008e101d3270e1bde4aa`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8bd4b70d37a12e0f9dcb0bcd6e607999215ae53796551b5b992db4a8a313a9`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e87b8b9173df45744529ff926d597f271fc4c82840de7e592db634c2bba612`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421779253a20a914c8bee0741aaee2cb8034eca79af4ced56e4a76f24c164bee`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e4599c0aad31551fdedb5cf061222bc3ca5725173e18292bc922f85af11c7`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.2.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e3a42000b3c0300af626f7ef34ef6c32fbeb9e22ad12b1ca4f8c626bd992dd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb45be40468acd598cab3f9dec62c1d20b363b8acde345e5f90cc1395f41a096`

```dockerfile
```

-	Layers:
	-	`sha256:890676a1266c1e4292517dab5d1e07fc5dca3db970553b5f182fca34932ce481`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 26.8 KB (26829 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4.2.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d678ab47544c418bc60e2d8ee4f26efb87139ed9cb15b7b926be621a0fabaae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240933861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2a78dcce188b947435513ded71d2505548a3baa8bc5758f2b96e960118a8d5`
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
# Fri, 15 May 2026 20:12:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:17 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 20:12:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:46 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:46 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:46 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:46 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:46 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:46 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce635e7d01d2f3aa4cdc0e29d5ce1e1fc8db99b945439b91cbac2e10db90516`  
		Last Modified: Fri, 15 May 2026 20:13:07 GMT  
		Size: 7.6 MB (7578887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86418539472f4360479981496210d0060c38b189980bb1b74f793fce27950ca`  
		Last Modified: Fri, 15 May 2026 20:13:11 GMT  
		Size: 204.9 MB (204878380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837d157f50a0bdb54f3b0c64e656e4baeb48fd540a8b97b8a0a162fb2064d260`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0866f7d3821c6d116aa678b8de1b26f43a2fa8b261ccd7f14cefa2bced6938`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efb278e5009015a7dc5ec9e3deb460b4e0a333f6faf2282e777ef3c48eb4958`  
		Last Modified: Fri, 15 May 2026 20:13:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579fa624037cb75e2fc16f005552ce2f0e0ba5b9e145884aa21b0d4ec92cbe49`  
		Last Modified: Fri, 15 May 2026 20:13:08 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8b4d0234cba88deaf42387b52c151fc7c3594caad69a1fe88685397c9b9997`  
		Last Modified: Fri, 15 May 2026 20:13:08 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.2.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f895599d0d0dce9ca4ccb64d9b54cbc2b2d2f283b7d59c97f63c0b20a0ebff95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b34e766d4a4fa200c55507d11bef01d6567525ce2015d2833b204fe71752c0d`

```dockerfile
```

-	Layers:
	-	`sha256:192a3ef7cc75ba46257f63cb62d15be7934d2590b59ce807632bbc7b2d1c3e4e`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 27.0 KB (27042 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4.2.10-jammy`

```console
$ docker pull clickhouse@sha256:1af0a59ee14edcfe26343e5cea750505dcbe5061040e75f74563cf48c5a0223a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4.2.10-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:eac3c18fa7fa69102d117807104bfd5d1a861b20de1cbbc97d38c0e0978aa9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257125149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ceac7d4db2314728d863114214cc142d28dec4486f574a8a822d8b4a13569d`
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
# Fri, 15 May 2026 20:12:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:04 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 20:12:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:29 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:29 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:29 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043da6b091b2130a64745708f3a86762248defdeb9e191368684b156a54db92a`  
		Last Modified: Fri, 15 May 2026 20:12:56 GMT  
		Size: 7.6 MB (7599186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f958db428686e7102bab50d7f199039d9dcd3174bdc7f3789f0e8d87b2d224`  
		Last Modified: Fri, 15 May 2026 20:13:00 GMT  
		Size: 218.9 MB (218919423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2c0f72094d39dfc7e1df290032419a048617b3c7d9008e101d3270e1bde4aa`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8bd4b70d37a12e0f9dcb0bcd6e607999215ae53796551b5b992db4a8a313a9`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e87b8b9173df45744529ff926d597f271fc4c82840de7e592db634c2bba612`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421779253a20a914c8bee0741aaee2cb8034eca79af4ced56e4a76f24c164bee`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e4599c0aad31551fdedb5cf061222bc3ca5725173e18292bc922f85af11c7`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.2.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e3a42000b3c0300af626f7ef34ef6c32fbeb9e22ad12b1ca4f8c626bd992dd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb45be40468acd598cab3f9dec62c1d20b363b8acde345e5f90cc1395f41a096`

```dockerfile
```

-	Layers:
	-	`sha256:890676a1266c1e4292517dab5d1e07fc5dca3db970553b5f182fca34932ce481`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 26.8 KB (26829 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4.2.10-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d678ab47544c418bc60e2d8ee4f26efb87139ed9cb15b7b926be621a0fabaae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240933861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2a78dcce188b947435513ded71d2505548a3baa8bc5758f2b96e960118a8d5`
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
# Fri, 15 May 2026 20:12:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:17 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 20:12:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:46 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:46 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:46 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:46 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:46 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:46 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce635e7d01d2f3aa4cdc0e29d5ce1e1fc8db99b945439b91cbac2e10db90516`  
		Last Modified: Fri, 15 May 2026 20:13:07 GMT  
		Size: 7.6 MB (7578887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86418539472f4360479981496210d0060c38b189980bb1b74f793fce27950ca`  
		Last Modified: Fri, 15 May 2026 20:13:11 GMT  
		Size: 204.9 MB (204878380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837d157f50a0bdb54f3b0c64e656e4baeb48fd540a8b97b8a0a162fb2064d260`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0866f7d3821c6d116aa678b8de1b26f43a2fa8b261ccd7f14cefa2bced6938`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efb278e5009015a7dc5ec9e3deb460b4e0a333f6faf2282e777ef3c48eb4958`  
		Last Modified: Fri, 15 May 2026 20:13:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579fa624037cb75e2fc16f005552ce2f0e0ba5b9e145884aa21b0d4ec92cbe49`  
		Last Modified: Fri, 15 May 2026 20:13:08 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8b4d0234cba88deaf42387b52c151fc7c3594caad69a1fe88685397c9b9997`  
		Last Modified: Fri, 15 May 2026 20:13:08 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.2.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f895599d0d0dce9ca4ccb64d9b54cbc2b2d2f283b7d59c97f63c0b20a0ebff95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b34e766d4a4fa200c55507d11bef01d6567525ce2015d2833b204fe71752c0d`

```dockerfile
```

-	Layers:
	-	`sha256:192a3ef7cc75ba46257f63cb62d15be7934d2590b59ce807632bbc7b2d1c3e4e`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 27.0 KB (27042 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:1af0a59ee14edcfe26343e5cea750505dcbe5061040e75f74563cf48c5a0223a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:eac3c18fa7fa69102d117807104bfd5d1a861b20de1cbbc97d38c0e0978aa9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257125149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ceac7d4db2314728d863114214cc142d28dec4486f574a8a822d8b4a13569d`
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
# Fri, 15 May 2026 20:12:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:04 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 20:12:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:29 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:29 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:29 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043da6b091b2130a64745708f3a86762248defdeb9e191368684b156a54db92a`  
		Last Modified: Fri, 15 May 2026 20:12:56 GMT  
		Size: 7.6 MB (7599186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f958db428686e7102bab50d7f199039d9dcd3174bdc7f3789f0e8d87b2d224`  
		Last Modified: Fri, 15 May 2026 20:13:00 GMT  
		Size: 218.9 MB (218919423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2c0f72094d39dfc7e1df290032419a048617b3c7d9008e101d3270e1bde4aa`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8bd4b70d37a12e0f9dcb0bcd6e607999215ae53796551b5b992db4a8a313a9`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e87b8b9173df45744529ff926d597f271fc4c82840de7e592db634c2bba612`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421779253a20a914c8bee0741aaee2cb8034eca79af4ced56e4a76f24c164bee`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e4599c0aad31551fdedb5cf061222bc3ca5725173e18292bc922f85af11c7`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e3a42000b3c0300af626f7ef34ef6c32fbeb9e22ad12b1ca4f8c626bd992dd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb45be40468acd598cab3f9dec62c1d20b363b8acde345e5f90cc1395f41a096`

```dockerfile
```

-	Layers:
	-	`sha256:890676a1266c1e4292517dab5d1e07fc5dca3db970553b5f182fca34932ce481`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 26.8 KB (26829 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d678ab47544c418bc60e2d8ee4f26efb87139ed9cb15b7b926be621a0fabaae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240933861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2a78dcce188b947435513ded71d2505548a3baa8bc5758f2b96e960118a8d5`
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
# Fri, 15 May 2026 20:12:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:17 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 20:12:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:46 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:46 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:46 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:46 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:46 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:46 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce635e7d01d2f3aa4cdc0e29d5ce1e1fc8db99b945439b91cbac2e10db90516`  
		Last Modified: Fri, 15 May 2026 20:13:07 GMT  
		Size: 7.6 MB (7578887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86418539472f4360479981496210d0060c38b189980bb1b74f793fce27950ca`  
		Last Modified: Fri, 15 May 2026 20:13:11 GMT  
		Size: 204.9 MB (204878380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837d157f50a0bdb54f3b0c64e656e4baeb48fd540a8b97b8a0a162fb2064d260`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0866f7d3821c6d116aa678b8de1b26f43a2fa8b261ccd7f14cefa2bced6938`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efb278e5009015a7dc5ec9e3deb460b4e0a333f6faf2282e777ef3c48eb4958`  
		Last Modified: Fri, 15 May 2026 20:13:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579fa624037cb75e2fc16f005552ce2f0e0ba5b9e145884aa21b0d4ec92cbe49`  
		Last Modified: Fri, 15 May 2026 20:13:08 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8b4d0234cba88deaf42387b52c151fc7c3594caad69a1fe88685397c9b9997`  
		Last Modified: Fri, 15 May 2026 20:13:08 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f895599d0d0dce9ca4ccb64d9b54cbc2b2d2f283b7d59c97f63c0b20a0ebff95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b34e766d4a4fa200c55507d11bef01d6567525ce2015d2833b204fe71752c0d`

```dockerfile
```

-	Layers:
	-	`sha256:192a3ef7cc75ba46257f63cb62d15be7934d2590b59ce807632bbc7b2d1c3e4e`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 27.0 KB (27042 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:1af0a59ee14edcfe26343e5cea750505dcbe5061040e75f74563cf48c5a0223a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:eac3c18fa7fa69102d117807104bfd5d1a861b20de1cbbc97d38c0e0978aa9ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257125149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ceac7d4db2314728d863114214cc142d28dec4486f574a8a822d8b4a13569d`
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
# Fri, 15 May 2026 20:12:04 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:04 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:04 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:04 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:04 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 20:12:04 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:29 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:29 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:29 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043da6b091b2130a64745708f3a86762248defdeb9e191368684b156a54db92a`  
		Last Modified: Fri, 15 May 2026 20:12:56 GMT  
		Size: 7.6 MB (7599186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f958db428686e7102bab50d7f199039d9dcd3174bdc7f3789f0e8d87b2d224`  
		Last Modified: Fri, 15 May 2026 20:13:00 GMT  
		Size: 218.9 MB (218919423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e2c0f72094d39dfc7e1df290032419a048617b3c7d9008e101d3270e1bde4aa`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8bd4b70d37a12e0f9dcb0bcd6e607999215ae53796551b5b992db4a8a313a9`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e87b8b9173df45744529ff926d597f271fc4c82840de7e592db634c2bba612`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421779253a20a914c8bee0741aaee2cb8034eca79af4ced56e4a76f24c164bee`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5e4599c0aad31551fdedb5cf061222bc3ca5725173e18292bc922f85af11c7`  
		Last Modified: Fri, 15 May 2026 20:12:57 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e3a42000b3c0300af626f7ef34ef6c32fbeb9e22ad12b1ca4f8c626bd992dd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb45be40468acd598cab3f9dec62c1d20b363b8acde345e5f90cc1395f41a096`

```dockerfile
```

-	Layers:
	-	`sha256:890676a1266c1e4292517dab5d1e07fc5dca3db970553b5f182fca34932ce481`  
		Last Modified: Fri, 15 May 2026 20:12:55 GMT  
		Size: 26.8 KB (26829 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d678ab47544c418bc60e2d8ee4f26efb87139ed9cb15b7b926be621a0fabaae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240933861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2a78dcce188b947435513ded71d2505548a3baa8bc5758f2b96e960118a8d5`
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
# Fri, 15 May 2026 20:12:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:17 GMT
ARG VERSION=26.4.2.10
# Fri, 15 May 2026 20:12:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:46 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:46 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.2.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:46 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:46 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:46 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:46 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:46 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce635e7d01d2f3aa4cdc0e29d5ce1e1fc8db99b945439b91cbac2e10db90516`  
		Last Modified: Fri, 15 May 2026 20:13:07 GMT  
		Size: 7.6 MB (7578887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86418539472f4360479981496210d0060c38b189980bb1b74f793fce27950ca`  
		Last Modified: Fri, 15 May 2026 20:13:11 GMT  
		Size: 204.9 MB (204878380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:837d157f50a0bdb54f3b0c64e656e4baeb48fd540a8b97b8a0a162fb2064d260`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0866f7d3821c6d116aa678b8de1b26f43a2fa8b261ccd7f14cefa2bced6938`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5efb278e5009015a7dc5ec9e3deb460b4e0a333f6faf2282e777ef3c48eb4958`  
		Last Modified: Fri, 15 May 2026 20:13:07 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579fa624037cb75e2fc16f005552ce2f0e0ba5b9e145884aa21b0d4ec92cbe49`  
		Last Modified: Fri, 15 May 2026 20:13:08 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8b4d0234cba88deaf42387b52c151fc7c3594caad69a1fe88685397c9b9997`  
		Last Modified: Fri, 15 May 2026 20:13:08 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f895599d0d0dce9ca4ccb64d9b54cbc2b2d2f283b7d59c97f63c0b20a0ebff95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b34e766d4a4fa200c55507d11bef01d6567525ce2015d2833b204fe71752c0d`

```dockerfile
```

-	Layers:
	-	`sha256:192a3ef7cc75ba46257f63cb62d15be7934d2590b59ce807632bbc7b2d1c3e4e`  
		Last Modified: Fri, 15 May 2026 20:13:06 GMT  
		Size: 27.0 KB (27042 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:6e6c9744ea880affeaeb297eaecdbee62baeaaf5eb93bae4cf0148fc9d707c09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:2930dac41388856da9d9b966af39711497f97ba2fdcec45978177872b53c21f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264805741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03811a854d0a975b5c58dac0a5e4d27c668f3852952dc3e52ea99e9fe4e4bbd1`
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
# Fri, 15 May 2026 20:12:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 20:12:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:50 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:50 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec80bef1e5a351e99527ab0b420e914caab74e3e531bceef4934327c4f6a31e0`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 7.6 MB (7599224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908f29adc9c7f107d4f757e333f49945314c082e5791a8b14a87d708410671aa`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 226.6 MB (226599972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b29cf36294109f87abe437963def616be6aabc239a5bc75e51a2ed582dbacf`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851f83769fc8458a25d883c50e1066b1b53d42c1d4a762c62c2eac5ebe711d46`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec8d122e9799e2989598b33de3df276f05e69167d67142ea81b4144619a0d07`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708419c0879fea53b52186c7bd3acece66e020a9ff5bde8bce01a444408ccb39`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1d37d3c4341b39395f5fffa19e30e3ab30cf525cf8bc82b87acd39cbf63938`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1467897289b8de65cc6ed205db092604b6d36885ebadd2ae6756f20b514e9c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b818e686cf2d9d43587b1771e162941c4d0dc43e0e3ff9499dd15eccfe664bc4`

```dockerfile
```

-	Layers:
	-	`sha256:24290da259fe55d62538b2a30d56810cf0b55135ad34b8c4b0d81cd2bebc8a6a`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a816656225b782366b2967b8dd016c1e9c295b68c0ddde1e03c43ced212fb7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f691bb66d68d39169b385477421c3257d94f756b3e48dd01ac5323bc1af4680`
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
# Fri, 15 May 2026 20:12:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 20:12:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22b6f69def2c37af88fc1fdaab0e3ae42f6475bb059426956176ada924fccf7`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 7.6 MB (7578915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc438280275d64a01ed12b00c30f0ae52a24a55ca77c5f8b7ec62bac184905e`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 210.2 MB (210218560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d7d3a01b0dee6dcf1511a6e2cc0ac78c4ee6b48902eb2a4ecf9e1ab7f38d8c`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984c732d979e9edcb529eebdf77a55130075a835b64461d9986a222330bfed31`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b5320ebe49fe6eaae20a8c76724123d5efa6c5302b504ff8d4b053b7ec0157`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4c8f9ed565b086aafd08dcbbad21677f168d50526223bc8e19f02403aa334c`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b472a2c941fbbb6d9bc1f14942cac6e17fc6713f8aa25c39ac117b15b2de7440`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e11af04de005418a512f2a7e0715800e2e7956445fa4576c5f0a620bc8aeab7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d967a3e529594de19f6bd9f1b0bfe1fb85646da773f33e30db8a4b1a4fa9b08`

```dockerfile
```

-	Layers:
	-	`sha256:2b2361287b8649808793fc5d1dafd594ff7ed3a7cd5346173cfd72c29da55088`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:6e6c9744ea880affeaeb297eaecdbee62baeaaf5eb93bae4cf0148fc9d707c09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:2930dac41388856da9d9b966af39711497f97ba2fdcec45978177872b53c21f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264805741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03811a854d0a975b5c58dac0a5e4d27c668f3852952dc3e52ea99e9fe4e4bbd1`
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
# Fri, 15 May 2026 20:12:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 20:12:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:50 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:50 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:50 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:50 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:50 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:50 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:50 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f63eb04151bcac21ad049f8d781b97b219aba392c5457907f8f3e88e43eb48ec`  
		Last Modified: Fri, 10 Apr 2026 11:00:47 GMT  
		Size: 29.7 MB (29736498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec80bef1e5a351e99527ab0b420e914caab74e3e531bceef4934327c4f6a31e0`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 7.6 MB (7599224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908f29adc9c7f107d4f757e333f49945314c082e5791a8b14a87d708410671aa`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 226.6 MB (226599972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b29cf36294109f87abe437963def616be6aabc239a5bc75e51a2ed582dbacf`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851f83769fc8458a25d883c50e1066b1b53d42c1d4a762c62c2eac5ebe711d46`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec8d122e9799e2989598b33de3df276f05e69167d67142ea81b4144619a0d07`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708419c0879fea53b52186c7bd3acece66e020a9ff5bde8bce01a444408ccb39`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1d37d3c4341b39395f5fffa19e30e3ab30cf525cf8bc82b87acd39cbf63938`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1467897289b8de65cc6ed205db092604b6d36885ebadd2ae6756f20b514e9c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b818e686cf2d9d43587b1771e162941c4d0dc43e0e3ff9499dd15eccfe664bc4`

```dockerfile
```

-	Layers:
	-	`sha256:24290da259fe55d62538b2a30d56810cf0b55135ad34b8c4b0d81cd2bebc8a6a`  
		Last Modified: Fri, 15 May 2026 20:13:16 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a816656225b782366b2967b8dd016c1e9c295b68c0ddde1e03c43ced212fb7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f691bb66d68d39169b385477421c3257d94f756b3e48dd01ac5323bc1af4680`
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
# Fri, 15 May 2026 20:12:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 20:12:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 20:12:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 20:12:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 20:12:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 20:12:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 20:12:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 20:12:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 20:12:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 20:12:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 20:12:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 20:12:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 20:12:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 20:12:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 20:12:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 20:12:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 20:12:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 20:12:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6edbc812af48552062d74659cf0a08b413dbfdbacdd5aac73329d889d9b3b44a`  
		Last Modified: Fri, 10 Apr 2026 11:00:55 GMT  
		Size: 27.6 MB (27606543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22b6f69def2c37af88fc1fdaab0e3ae42f6475bb059426956176ada924fccf7`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 7.6 MB (7578915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc438280275d64a01ed12b00c30f0ae52a24a55ca77c5f8b7ec62bac184905e`  
		Last Modified: Fri, 15 May 2026 20:13:22 GMT  
		Size: 210.2 MB (210218560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d7d3a01b0dee6dcf1511a6e2cc0ac78c4ee6b48902eb2a4ecf9e1ab7f38d8c`  
		Last Modified: Fri, 15 May 2026 20:13:17 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:984c732d979e9edcb529eebdf77a55130075a835b64461d9986a222330bfed31`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b5320ebe49fe6eaae20a8c76724123d5efa6c5302b504ff8d4b053b7ec0157`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4c8f9ed565b086aafd08dcbbad21677f168d50526223bc8e19f02403aa334c`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b472a2c941fbbb6d9bc1f14942cac6e17fc6713f8aa25c39ac117b15b2de7440`  
		Last Modified: Fri, 15 May 2026 20:13:19 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e11af04de005418a512f2a7e0715800e2e7956445fa4576c5f0a620bc8aeab7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d967a3e529594de19f6bd9f1b0bfe1fb85646da773f33e30db8a4b1a4fa9b08`

```dockerfile
```

-	Layers:
	-	`sha256:2b2361287b8649808793fc5d1dafd594ff7ed3a7cd5346173cfd72c29da55088`  
		Last Modified: Fri, 15 May 2026 20:13:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json
