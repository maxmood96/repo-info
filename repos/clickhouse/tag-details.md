<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:24.8`](#clickhouse248)
-	[`clickhouse:24.8-focal`](#clickhouse248-focal)
-	[`clickhouse:24.8.14`](#clickhouse24814)
-	[`clickhouse:24.8.14-focal`](#clickhouse24814-focal)
-	[`clickhouse:24.8.14.39`](#clickhouse2481439)
-	[`clickhouse:24.8.14.39-focal`](#clickhouse2481439-focal)
-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.3`](#clickhouse2533)
-	[`clickhouse:25.3.3-jammy`](#clickhouse2533-jammy)
-	[`clickhouse:25.3.3.42`](#clickhouse253342)
-	[`clickhouse:25.3.3.42-jammy`](#clickhouse253342-jammy)
-	[`clickhouse:25.4`](#clickhouse254)
-	[`clickhouse:25.4-jammy`](#clickhouse254-jammy)
-	[`clickhouse:25.4.5`](#clickhouse2545)
-	[`clickhouse:25.4.5-jammy`](#clickhouse2545-jammy)
-	[`clickhouse:25.4.5.24`](#clickhouse254524)
-	[`clickhouse:25.4.5.24-jammy`](#clickhouse254524-jammy)
-	[`clickhouse:25.5`](#clickhouse255)
-	[`clickhouse:25.5-jammy`](#clickhouse255-jammy)
-	[`clickhouse:25.5.1`](#clickhouse2551)
-	[`clickhouse:25.5.1-jammy`](#clickhouse2551-jammy)
-	[`clickhouse:25.5.1.2782`](#clickhouse25512782)
-	[`clickhouse:25.5.1.2782-jammy`](#clickhouse25512782-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:24.8`

```console
$ docker pull clickhouse@sha256:9eb59796efe815711207122267e407dd3b42efd90d01537e1c80118bfc642a11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:1b41b544da2428cc0df6632a38af8f0fef28658cce772fbd1f051ac2d8c74245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178875199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184157298fb8634def0cd9587b2a40374578f308a346d9d96c07ef0c4826d8d9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 28 Mar 2025 10:04:18 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=24.8.14.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e1243e412a6a0201cd184f8fa51a0e71d129b8f4de79db7d193183afec4c6d`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 8.8 MB (8799908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac9af3af17b3193492bcdfd91f391c8c334911aaf3922fa6311319cbe6a33f4`  
		Last Modified: Wed, 09 Apr 2025 01:12:10 GMT  
		Size: 141.7 MB (141696924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c4bb93ab79bf3904707d3c99cd46e7835928d2a2f90c2ba21b912ce560de83`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36637523a27e51acb137f07a48d0ad9849a41a41c0c60b84c41ab4498429ab56`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382d8e10b9f36a4c5dea337b013c269860abca3be162c5463a80174e6d98eb1f`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcae91c2cf4a08b42245af59422ab5c439de48c7cd6f00c4ada6ee64c324b39`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acffb612a4bc15abbb5b81b9384d4534df6a5e5854abc7d5add9464619084de8`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d343e95711098f63c25aaca6822dfe5c52903b87ae2bc5fdfea508f5f8a2920e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99477c584de9210dbfd2f83bf82529a95c5493326ad37a34aa14d700b58d5fc`

```dockerfile
```

-	Layers:
	-	`sha256:b2d7d1ee8f1c4eba7c73e03dcb2dea9e16004b7c6d36e276f19c0b8466252f6a`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:554e80790c9457710c634dfcb227a95883c5946fcaf645d20aad32ffe5b80235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172255073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81902d5c0fadae3ecb9e8dda6e0ba20448059361dc8270b1f4032f7fe7805fb4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Fri, 28 Mar 2025 10:04:18 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=24.8.14.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef4febeaa9a96a464e61f373f7883b7bf2e04bca608d6f01b00d574f182900`  
		Last Modified: Wed, 09 Apr 2025 06:15:59 GMT  
		Size: 8.7 MB (8658757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a0789ea10e651f70441e6da73550d2821aabb69bc62b7f062631cb21cb3be`  
		Last Modified: Wed, 09 Apr 2025 06:16:02 GMT  
		Size: 136.8 MB (136750682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798c2b06438cfb8c040af039a5404f2eb18b7e887f0e03c4221bdf23bf423e7`  
		Last Modified: Wed, 09 Apr 2025 06:15:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f94512f579ab88482ec7b65bbdf5c4be1554b0fc7be38134d2655b6a3a2ba1`  
		Last Modified: Wed, 09 Apr 2025 06:15:59 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c9df5310d0e344009510a490a161d18ef94d62c24fa9a240d03af5ab2cefb3`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cec40ddbc5ae51f53198099e6bdff6123006e041994449d5d13aedf54f4377`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7506d9e38ab7aa6336f39aeb3ec50c386a354f0cfd2d921f65bf9384d597d8e5`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f79f8d62eb7b922dbeb9e72520f3f7c5dbd3aea919520afc9588df3b3258ab66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc9e29fd088b81bc80e9685b3996fceb91345b5845198fdbe9d8693e2c7779b`

```dockerfile
```

-	Layers:
	-	`sha256:c2e883ea8b3fbae4797a842837bb11755d84d5df1ff79013d0cbf0801ba7c31a`  
		Last Modified: Wed, 09 Apr 2025 06:15:58 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8-focal`

```console
$ docker pull clickhouse@sha256:9eb59796efe815711207122267e407dd3b42efd90d01537e1c80118bfc642a11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:1b41b544da2428cc0df6632a38af8f0fef28658cce772fbd1f051ac2d8c74245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178875199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184157298fb8634def0cd9587b2a40374578f308a346d9d96c07ef0c4826d8d9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 28 Mar 2025 10:04:18 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=24.8.14.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e1243e412a6a0201cd184f8fa51a0e71d129b8f4de79db7d193183afec4c6d`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 8.8 MB (8799908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac9af3af17b3193492bcdfd91f391c8c334911aaf3922fa6311319cbe6a33f4`  
		Last Modified: Wed, 09 Apr 2025 01:12:10 GMT  
		Size: 141.7 MB (141696924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c4bb93ab79bf3904707d3c99cd46e7835928d2a2f90c2ba21b912ce560de83`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36637523a27e51acb137f07a48d0ad9849a41a41c0c60b84c41ab4498429ab56`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382d8e10b9f36a4c5dea337b013c269860abca3be162c5463a80174e6d98eb1f`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcae91c2cf4a08b42245af59422ab5c439de48c7cd6f00c4ada6ee64c324b39`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acffb612a4bc15abbb5b81b9384d4534df6a5e5854abc7d5add9464619084de8`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d343e95711098f63c25aaca6822dfe5c52903b87ae2bc5fdfea508f5f8a2920e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99477c584de9210dbfd2f83bf82529a95c5493326ad37a34aa14d700b58d5fc`

```dockerfile
```

-	Layers:
	-	`sha256:b2d7d1ee8f1c4eba7c73e03dcb2dea9e16004b7c6d36e276f19c0b8466252f6a`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:554e80790c9457710c634dfcb227a95883c5946fcaf645d20aad32ffe5b80235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172255073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81902d5c0fadae3ecb9e8dda6e0ba20448059361dc8270b1f4032f7fe7805fb4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Fri, 28 Mar 2025 10:04:18 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=24.8.14.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef4febeaa9a96a464e61f373f7883b7bf2e04bca608d6f01b00d574f182900`  
		Last Modified: Wed, 09 Apr 2025 06:15:59 GMT  
		Size: 8.7 MB (8658757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a0789ea10e651f70441e6da73550d2821aabb69bc62b7f062631cb21cb3be`  
		Last Modified: Wed, 09 Apr 2025 06:16:02 GMT  
		Size: 136.8 MB (136750682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798c2b06438cfb8c040af039a5404f2eb18b7e887f0e03c4221bdf23bf423e7`  
		Last Modified: Wed, 09 Apr 2025 06:15:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f94512f579ab88482ec7b65bbdf5c4be1554b0fc7be38134d2655b6a3a2ba1`  
		Last Modified: Wed, 09 Apr 2025 06:15:59 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c9df5310d0e344009510a490a161d18ef94d62c24fa9a240d03af5ab2cefb3`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cec40ddbc5ae51f53198099e6bdff6123006e041994449d5d13aedf54f4377`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7506d9e38ab7aa6336f39aeb3ec50c386a354f0cfd2d921f65bf9384d597d8e5`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f79f8d62eb7b922dbeb9e72520f3f7c5dbd3aea919520afc9588df3b3258ab66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc9e29fd088b81bc80e9685b3996fceb91345b5845198fdbe9d8693e2c7779b`

```dockerfile
```

-	Layers:
	-	`sha256:c2e883ea8b3fbae4797a842837bb11755d84d5df1ff79013d0cbf0801ba7c31a`  
		Last Modified: Wed, 09 Apr 2025 06:15:58 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.14`

```console
$ docker pull clickhouse@sha256:9eb59796efe815711207122267e407dd3b42efd90d01537e1c80118bfc642a11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.14` - linux; amd64

```console
$ docker pull clickhouse@sha256:1b41b544da2428cc0df6632a38af8f0fef28658cce772fbd1f051ac2d8c74245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178875199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184157298fb8634def0cd9587b2a40374578f308a346d9d96c07ef0c4826d8d9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 28 Mar 2025 10:04:18 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=24.8.14.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e1243e412a6a0201cd184f8fa51a0e71d129b8f4de79db7d193183afec4c6d`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 8.8 MB (8799908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac9af3af17b3193492bcdfd91f391c8c334911aaf3922fa6311319cbe6a33f4`  
		Last Modified: Wed, 09 Apr 2025 01:12:10 GMT  
		Size: 141.7 MB (141696924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c4bb93ab79bf3904707d3c99cd46e7835928d2a2f90c2ba21b912ce560de83`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36637523a27e51acb137f07a48d0ad9849a41a41c0c60b84c41ab4498429ab56`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382d8e10b9f36a4c5dea337b013c269860abca3be162c5463a80174e6d98eb1f`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcae91c2cf4a08b42245af59422ab5c439de48c7cd6f00c4ada6ee64c324b39`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acffb612a4bc15abbb5b81b9384d4534df6a5e5854abc7d5add9464619084de8`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d343e95711098f63c25aaca6822dfe5c52903b87ae2bc5fdfea508f5f8a2920e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99477c584de9210dbfd2f83bf82529a95c5493326ad37a34aa14d700b58d5fc`

```dockerfile
```

-	Layers:
	-	`sha256:b2d7d1ee8f1c4eba7c73e03dcb2dea9e16004b7c6d36e276f19c0b8466252f6a`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.14` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:554e80790c9457710c634dfcb227a95883c5946fcaf645d20aad32ffe5b80235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172255073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81902d5c0fadae3ecb9e8dda6e0ba20448059361dc8270b1f4032f7fe7805fb4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Fri, 28 Mar 2025 10:04:18 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=24.8.14.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef4febeaa9a96a464e61f373f7883b7bf2e04bca608d6f01b00d574f182900`  
		Last Modified: Wed, 09 Apr 2025 06:15:59 GMT  
		Size: 8.7 MB (8658757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a0789ea10e651f70441e6da73550d2821aabb69bc62b7f062631cb21cb3be`  
		Last Modified: Wed, 09 Apr 2025 06:16:02 GMT  
		Size: 136.8 MB (136750682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798c2b06438cfb8c040af039a5404f2eb18b7e887f0e03c4221bdf23bf423e7`  
		Last Modified: Wed, 09 Apr 2025 06:15:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f94512f579ab88482ec7b65bbdf5c4be1554b0fc7be38134d2655b6a3a2ba1`  
		Last Modified: Wed, 09 Apr 2025 06:15:59 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c9df5310d0e344009510a490a161d18ef94d62c24fa9a240d03af5ab2cefb3`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cec40ddbc5ae51f53198099e6bdff6123006e041994449d5d13aedf54f4377`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7506d9e38ab7aa6336f39aeb3ec50c386a354f0cfd2d921f65bf9384d597d8e5`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f79f8d62eb7b922dbeb9e72520f3f7c5dbd3aea919520afc9588df3b3258ab66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc9e29fd088b81bc80e9685b3996fceb91345b5845198fdbe9d8693e2c7779b`

```dockerfile
```

-	Layers:
	-	`sha256:c2e883ea8b3fbae4797a842837bb11755d84d5df1ff79013d0cbf0801ba7c31a`  
		Last Modified: Wed, 09 Apr 2025 06:15:58 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.14-focal`

```console
$ docker pull clickhouse@sha256:9eb59796efe815711207122267e407dd3b42efd90d01537e1c80118bfc642a11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.14-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:1b41b544da2428cc0df6632a38af8f0fef28658cce772fbd1f051ac2d8c74245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178875199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184157298fb8634def0cd9587b2a40374578f308a346d9d96c07ef0c4826d8d9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 28 Mar 2025 10:04:18 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=24.8.14.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e1243e412a6a0201cd184f8fa51a0e71d129b8f4de79db7d193183afec4c6d`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 8.8 MB (8799908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac9af3af17b3193492bcdfd91f391c8c334911aaf3922fa6311319cbe6a33f4`  
		Last Modified: Wed, 09 Apr 2025 01:12:10 GMT  
		Size: 141.7 MB (141696924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c4bb93ab79bf3904707d3c99cd46e7835928d2a2f90c2ba21b912ce560de83`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36637523a27e51acb137f07a48d0ad9849a41a41c0c60b84c41ab4498429ab56`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382d8e10b9f36a4c5dea337b013c269860abca3be162c5463a80174e6d98eb1f`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcae91c2cf4a08b42245af59422ab5c439de48c7cd6f00c4ada6ee64c324b39`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acffb612a4bc15abbb5b81b9384d4534df6a5e5854abc7d5add9464619084de8`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d343e95711098f63c25aaca6822dfe5c52903b87ae2bc5fdfea508f5f8a2920e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99477c584de9210dbfd2f83bf82529a95c5493326ad37a34aa14d700b58d5fc`

```dockerfile
```

-	Layers:
	-	`sha256:b2d7d1ee8f1c4eba7c73e03dcb2dea9e16004b7c6d36e276f19c0b8466252f6a`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.14-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:554e80790c9457710c634dfcb227a95883c5946fcaf645d20aad32ffe5b80235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172255073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81902d5c0fadae3ecb9e8dda6e0ba20448059361dc8270b1f4032f7fe7805fb4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Fri, 28 Mar 2025 10:04:18 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=24.8.14.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef4febeaa9a96a464e61f373f7883b7bf2e04bca608d6f01b00d574f182900`  
		Last Modified: Wed, 09 Apr 2025 06:15:59 GMT  
		Size: 8.7 MB (8658757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a0789ea10e651f70441e6da73550d2821aabb69bc62b7f062631cb21cb3be`  
		Last Modified: Wed, 09 Apr 2025 06:16:02 GMT  
		Size: 136.8 MB (136750682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798c2b06438cfb8c040af039a5404f2eb18b7e887f0e03c4221bdf23bf423e7`  
		Last Modified: Wed, 09 Apr 2025 06:15:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f94512f579ab88482ec7b65bbdf5c4be1554b0fc7be38134d2655b6a3a2ba1`  
		Last Modified: Wed, 09 Apr 2025 06:15:59 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c9df5310d0e344009510a490a161d18ef94d62c24fa9a240d03af5ab2cefb3`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cec40ddbc5ae51f53198099e6bdff6123006e041994449d5d13aedf54f4377`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7506d9e38ab7aa6336f39aeb3ec50c386a354f0cfd2d921f65bf9384d597d8e5`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f79f8d62eb7b922dbeb9e72520f3f7c5dbd3aea919520afc9588df3b3258ab66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc9e29fd088b81bc80e9685b3996fceb91345b5845198fdbe9d8693e2c7779b`

```dockerfile
```

-	Layers:
	-	`sha256:c2e883ea8b3fbae4797a842837bb11755d84d5df1ff79013d0cbf0801ba7c31a`  
		Last Modified: Wed, 09 Apr 2025 06:15:58 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.14.39`

```console
$ docker pull clickhouse@sha256:9eb59796efe815711207122267e407dd3b42efd90d01537e1c80118bfc642a11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.14.39` - linux; amd64

```console
$ docker pull clickhouse@sha256:1b41b544da2428cc0df6632a38af8f0fef28658cce772fbd1f051ac2d8c74245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178875199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184157298fb8634def0cd9587b2a40374578f308a346d9d96c07ef0c4826d8d9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 28 Mar 2025 10:04:18 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=24.8.14.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e1243e412a6a0201cd184f8fa51a0e71d129b8f4de79db7d193183afec4c6d`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 8.8 MB (8799908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac9af3af17b3193492bcdfd91f391c8c334911aaf3922fa6311319cbe6a33f4`  
		Last Modified: Wed, 09 Apr 2025 01:12:10 GMT  
		Size: 141.7 MB (141696924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c4bb93ab79bf3904707d3c99cd46e7835928d2a2f90c2ba21b912ce560de83`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36637523a27e51acb137f07a48d0ad9849a41a41c0c60b84c41ab4498429ab56`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382d8e10b9f36a4c5dea337b013c269860abca3be162c5463a80174e6d98eb1f`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcae91c2cf4a08b42245af59422ab5c439de48c7cd6f00c4ada6ee64c324b39`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acffb612a4bc15abbb5b81b9384d4534df6a5e5854abc7d5add9464619084de8`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14.39` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d343e95711098f63c25aaca6822dfe5c52903b87ae2bc5fdfea508f5f8a2920e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99477c584de9210dbfd2f83bf82529a95c5493326ad37a34aa14d700b58d5fc`

```dockerfile
```

-	Layers:
	-	`sha256:b2d7d1ee8f1c4eba7c73e03dcb2dea9e16004b7c6d36e276f19c0b8466252f6a`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.14.39` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:554e80790c9457710c634dfcb227a95883c5946fcaf645d20aad32ffe5b80235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172255073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81902d5c0fadae3ecb9e8dda6e0ba20448059361dc8270b1f4032f7fe7805fb4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Fri, 28 Mar 2025 10:04:18 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=24.8.14.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef4febeaa9a96a464e61f373f7883b7bf2e04bca608d6f01b00d574f182900`  
		Last Modified: Wed, 09 Apr 2025 06:15:59 GMT  
		Size: 8.7 MB (8658757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a0789ea10e651f70441e6da73550d2821aabb69bc62b7f062631cb21cb3be`  
		Last Modified: Wed, 09 Apr 2025 06:16:02 GMT  
		Size: 136.8 MB (136750682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798c2b06438cfb8c040af039a5404f2eb18b7e887f0e03c4221bdf23bf423e7`  
		Last Modified: Wed, 09 Apr 2025 06:15:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f94512f579ab88482ec7b65bbdf5c4be1554b0fc7be38134d2655b6a3a2ba1`  
		Last Modified: Wed, 09 Apr 2025 06:15:59 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c9df5310d0e344009510a490a161d18ef94d62c24fa9a240d03af5ab2cefb3`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cec40ddbc5ae51f53198099e6bdff6123006e041994449d5d13aedf54f4377`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7506d9e38ab7aa6336f39aeb3ec50c386a354f0cfd2d921f65bf9384d597d8e5`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14.39` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f79f8d62eb7b922dbeb9e72520f3f7c5dbd3aea919520afc9588df3b3258ab66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc9e29fd088b81bc80e9685b3996fceb91345b5845198fdbe9d8693e2c7779b`

```dockerfile
```

-	Layers:
	-	`sha256:c2e883ea8b3fbae4797a842837bb11755d84d5df1ff79013d0cbf0801ba7c31a`  
		Last Modified: Wed, 09 Apr 2025 06:15:58 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.14.39-focal`

```console
$ docker pull clickhouse@sha256:9eb59796efe815711207122267e407dd3b42efd90d01537e1c80118bfc642a11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.14.39-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:1b41b544da2428cc0df6632a38af8f0fef28658cce772fbd1f051ac2d8c74245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178875199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:184157298fb8634def0cd9587b2a40374578f308a346d9d96c07ef0c4826d8d9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:f9ee450324e6ff2c946bc9aae5cf7e35e240dbd387d8b9f5ee1ed5b8434b9894 in / 
# Fri, 28 Mar 2025 10:04:18 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=24.8.14.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:13b7e930469f6d3575a320709035c6acf6f5485a76abcf03d1b92a64c09c2476`  
		Last Modified: Tue, 08 Apr 2025 11:48:23 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e1243e412a6a0201cd184f8fa51a0e71d129b8f4de79db7d193183afec4c6d`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 8.8 MB (8799908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac9af3af17b3193492bcdfd91f391c8c334911aaf3922fa6311319cbe6a33f4`  
		Last Modified: Wed, 09 Apr 2025 01:12:10 GMT  
		Size: 141.7 MB (141696924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c4bb93ab79bf3904707d3c99cd46e7835928d2a2f90c2ba21b912ce560de83`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36637523a27e51acb137f07a48d0ad9849a41a41c0c60b84c41ab4498429ab56`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382d8e10b9f36a4c5dea337b013c269860abca3be162c5463a80174e6d98eb1f`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcae91c2cf4a08b42245af59422ab5c439de48c7cd6f00c4ada6ee64c324b39`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acffb612a4bc15abbb5b81b9384d4534df6a5e5854abc7d5add9464619084de8`  
		Last Modified: Wed, 09 Apr 2025 01:12:09 GMT  
		Size: 3.8 KB (3839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14.39-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d343e95711098f63c25aaca6822dfe5c52903b87ae2bc5fdfea508f5f8a2920e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e99477c584de9210dbfd2f83bf82529a95c5493326ad37a34aa14d700b58d5fc`

```dockerfile
```

-	Layers:
	-	`sha256:b2d7d1ee8f1c4eba7c73e03dcb2dea9e16004b7c6d36e276f19c0b8466252f6a`  
		Last Modified: Wed, 09 Apr 2025 01:12:08 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.8.14.39-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:554e80790c9457710c634dfcb227a95883c5946fcaf645d20aad32ffe5b80235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.3 MB (172255073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81902d5c0fadae3ecb9e8dda6e0ba20448059361dc8270b1f4032f7fe7805fb4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:2c90d89e4dd4e1d2473deca816f585a78ced2a0c5c799399810f86fdbb17ac7e in / 
# Fri, 28 Mar 2025 10:04:18 GMT
CMD ["/bin/bash"]
# Fri, 28 Mar 2025 10:04:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 28 Mar 2025 10:04:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPO_CHANNEL=stable
# Fri, 28 Mar 2025 10:04:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 28 Mar 2025 10:04:18 GMT
ARG VERSION=24.8.14.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 28 Mar 2025 10:04:18 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 28 Mar 2025 10:04:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 28 Mar 2025 10:04:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:ecd83b6c354452b6a9979c7666bba16927f1e60e2afbfe6401dd6f87d5db8576`  
		Last Modified: Tue, 08 Apr 2025 11:48:29 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef4febeaa9a96a464e61f373f7883b7bf2e04bca608d6f01b00d574f182900`  
		Last Modified: Wed, 09 Apr 2025 06:15:59 GMT  
		Size: 8.7 MB (8658757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a0789ea10e651f70441e6da73550d2821aabb69bc62b7f062631cb21cb3be`  
		Last Modified: Wed, 09 Apr 2025 06:16:02 GMT  
		Size: 136.8 MB (136750682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798c2b06438cfb8c040af039a5404f2eb18b7e887f0e03c4221bdf23bf423e7`  
		Last Modified: Wed, 09 Apr 2025 06:15:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f94512f579ab88482ec7b65bbdf5c4be1554b0fc7be38134d2655b6a3a2ba1`  
		Last Modified: Wed, 09 Apr 2025 06:15:59 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c9df5310d0e344009510a490a161d18ef94d62c24fa9a240d03af5ab2cefb3`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cec40ddbc5ae51f53198099e6bdff6123006e041994449d5d13aedf54f4377`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7506d9e38ab7aa6336f39aeb3ec50c386a354f0cfd2d921f65bf9384d597d8e5`  
		Last Modified: Wed, 09 Apr 2025 06:16:00 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14.39-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f79f8d62eb7b922dbeb9e72520f3f7c5dbd3aea919520afc9588df3b3258ab66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc9e29fd088b81bc80e9685b3996fceb91345b5845198fdbe9d8693e2c7779b`

```dockerfile
```

-	Layers:
	-	`sha256:c2e883ea8b3fbae4797a842837bb11755d84d5df1ff79013d0cbf0801ba7c31a`  
		Last Modified: Wed, 09 Apr 2025 06:15:58 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:6f432bce9f74156e04db2a40fc5f5e59f05aa585194e5548368c6cbf456d63ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:b320679c5ca0b848e8c0e7ed06dbe975d5d4aa084f7e7b89ed7de34fc4b656f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc321325d517a2fc1a63924ffe8d507cb7388279b62cff337348d501785f740`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 10:04:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 02 May 2025 10:04:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ARG REPO_CHANNEL=stable
# Fri, 02 May 2025 10:04:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 02 May 2025 10:04:11 GMT
ARG VERSION=25.3.3.42
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 10:04:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 02 May 2025 10:04:11 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 02 May 2025 10:04:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 02 May 2025 10:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293c18414ddc6b5045bd255b1d3fff2b475d11f7bd01cf6f63c08323588bfeb`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 7.2 MB (7152053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a83e724674ef99b3a02f95d6f99edb74d6da86f3e952d96df426d2e24ffad54`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 167.0 MB (166978959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5788f6ecbfd19db9de8f1ebca0a309877c17b3a68e2b6927db7178a38dd3e2ea`  
		Last Modified: Mon, 05 May 2025 16:34:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c12c8cb54ca9170c10677abfac3c0cd2a66c86322bdbab8b6e6fe92cc0137`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477777a3fe047b2d393a11522c673d966c5106c04a594f53822905dfb3099ed`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357524fb1f1cb1c745bd69563a49c927ad2294938d4f470a351f5f65404ffdc`  
		Last Modified: Mon, 05 May 2025 16:34:59 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89b4acb36be4c123b76a5f2e389268a91bc95467c65d1b794c398fd8fb1631`  
		Last Modified: Mon, 05 May 2025 16:34:59 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0faf7dfca35f7610a11768af5806f14de92c5d3c6878fe530ace15f313771a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56563ead7314ab3dda2382afd2bc4d4d832666426dbd96304c321466b2e7722e`

```dockerfile
```

-	Layers:
	-	`sha256:001a2ba99704453b4192ecf76574a83ce56a72dc98bb29362403dd51dea2e99c`  
		Last Modified: Mon, 05 May 2025 16:34:57 GMT  
		Size: 25.9 KB (25874 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:641cd40cc4e90fff20a5e6a3388a2d862362b1ca4fbfb99227bfa4190b23ea77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192035226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972daccc52695628d0a97703050d19c600e6618b622b76f30d0fc538fab8a0c8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 10:04:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 02 May 2025 10:04:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ARG REPO_CHANNEL=stable
# Fri, 02 May 2025 10:04:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 02 May 2025 10:04:11 GMT
ARG VERSION=25.3.3.42
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 10:04:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 02 May 2025 10:04:11 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 02 May 2025 10:04:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 02 May 2025 10:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be04f390c597833173d77846d1293ad9897baf5e3a03f35936564cf8357f23d0`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 7.1 MB (7127782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63304746e0be595e8c18791c88e140ffcce7ef167770cb0eed5751a00ae24c97`  
		Last Modified: Mon, 05 May 2025 16:38:34 GMT  
		Size: 156.7 MB (156682982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3a65e1ba7a953198688fcc235a4aa5964d0f2579898b986d2df707007fade3`  
		Last Modified: Mon, 05 May 2025 16:38:29 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b201d0974da903e0cdb374d1c08192a2b464ec8048c2a9663a887ed549deb8e`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d384269f2cbb93d090459b306fac19a3f928e07fb6661a56d4a9a5a622d1676b`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b89a2a8dbd8bb92760956b84348fe7e88a495d07ab09fc6ac96aeee9be29109`  
		Last Modified: Mon, 05 May 2025 16:38:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423d17743661f544353b767293e75d841505deef68df1b0f01a77d1ae0189a8a`  
		Last Modified: Mon, 05 May 2025 16:38:31 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ce50101a43b7bc7af719b6306abf2eed03069509ccaeedb29ad994a9f08c395b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66dec5164ea12453fde66e209a44499f7785d422ad48fa1a4cdfec7132f70843`

```dockerfile
```

-	Layers:
	-	`sha256:1710dd56b0182fa3009a6a1f008d8ee7f69b543253b84d6e7738a98b83af284f`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:6f432bce9f74156e04db2a40fc5f5e59f05aa585194e5548368c6cbf456d63ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:b320679c5ca0b848e8c0e7ed06dbe975d5d4aa084f7e7b89ed7de34fc4b656f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc321325d517a2fc1a63924ffe8d507cb7388279b62cff337348d501785f740`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 10:04:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 02 May 2025 10:04:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ARG REPO_CHANNEL=stable
# Fri, 02 May 2025 10:04:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 02 May 2025 10:04:11 GMT
ARG VERSION=25.3.3.42
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 10:04:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 02 May 2025 10:04:11 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 02 May 2025 10:04:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 02 May 2025 10:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293c18414ddc6b5045bd255b1d3fff2b475d11f7bd01cf6f63c08323588bfeb`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 7.2 MB (7152053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a83e724674ef99b3a02f95d6f99edb74d6da86f3e952d96df426d2e24ffad54`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 167.0 MB (166978959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5788f6ecbfd19db9de8f1ebca0a309877c17b3a68e2b6927db7178a38dd3e2ea`  
		Last Modified: Mon, 05 May 2025 16:34:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c12c8cb54ca9170c10677abfac3c0cd2a66c86322bdbab8b6e6fe92cc0137`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477777a3fe047b2d393a11522c673d966c5106c04a594f53822905dfb3099ed`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357524fb1f1cb1c745bd69563a49c927ad2294938d4f470a351f5f65404ffdc`  
		Last Modified: Mon, 05 May 2025 16:34:59 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89b4acb36be4c123b76a5f2e389268a91bc95467c65d1b794c398fd8fb1631`  
		Last Modified: Mon, 05 May 2025 16:34:59 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0faf7dfca35f7610a11768af5806f14de92c5d3c6878fe530ace15f313771a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56563ead7314ab3dda2382afd2bc4d4d832666426dbd96304c321466b2e7722e`

```dockerfile
```

-	Layers:
	-	`sha256:001a2ba99704453b4192ecf76574a83ce56a72dc98bb29362403dd51dea2e99c`  
		Last Modified: Mon, 05 May 2025 16:34:57 GMT  
		Size: 25.9 KB (25874 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:641cd40cc4e90fff20a5e6a3388a2d862362b1ca4fbfb99227bfa4190b23ea77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192035226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972daccc52695628d0a97703050d19c600e6618b622b76f30d0fc538fab8a0c8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 10:04:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 02 May 2025 10:04:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ARG REPO_CHANNEL=stable
# Fri, 02 May 2025 10:04:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 02 May 2025 10:04:11 GMT
ARG VERSION=25.3.3.42
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 10:04:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 02 May 2025 10:04:11 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 02 May 2025 10:04:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 02 May 2025 10:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be04f390c597833173d77846d1293ad9897baf5e3a03f35936564cf8357f23d0`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 7.1 MB (7127782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63304746e0be595e8c18791c88e140ffcce7ef167770cb0eed5751a00ae24c97`  
		Last Modified: Mon, 05 May 2025 16:38:34 GMT  
		Size: 156.7 MB (156682982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3a65e1ba7a953198688fcc235a4aa5964d0f2579898b986d2df707007fade3`  
		Last Modified: Mon, 05 May 2025 16:38:29 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b201d0974da903e0cdb374d1c08192a2b464ec8048c2a9663a887ed549deb8e`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d384269f2cbb93d090459b306fac19a3f928e07fb6661a56d4a9a5a622d1676b`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b89a2a8dbd8bb92760956b84348fe7e88a495d07ab09fc6ac96aeee9be29109`  
		Last Modified: Mon, 05 May 2025 16:38:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423d17743661f544353b767293e75d841505deef68df1b0f01a77d1ae0189a8a`  
		Last Modified: Mon, 05 May 2025 16:38:31 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ce50101a43b7bc7af719b6306abf2eed03069509ccaeedb29ad994a9f08c395b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66dec5164ea12453fde66e209a44499f7785d422ad48fa1a4cdfec7132f70843`

```dockerfile
```

-	Layers:
	-	`sha256:1710dd56b0182fa3009a6a1f008d8ee7f69b543253b84d6e7738a98b83af284f`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.3`

```console
$ docker pull clickhouse@sha256:6f432bce9f74156e04db2a40fc5f5e59f05aa585194e5548368c6cbf456d63ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:b320679c5ca0b848e8c0e7ed06dbe975d5d4aa084f7e7b89ed7de34fc4b656f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc321325d517a2fc1a63924ffe8d507cb7388279b62cff337348d501785f740`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 10:04:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 02 May 2025 10:04:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ARG REPO_CHANNEL=stable
# Fri, 02 May 2025 10:04:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 02 May 2025 10:04:11 GMT
ARG VERSION=25.3.3.42
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 10:04:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 02 May 2025 10:04:11 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 02 May 2025 10:04:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 02 May 2025 10:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293c18414ddc6b5045bd255b1d3fff2b475d11f7bd01cf6f63c08323588bfeb`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 7.2 MB (7152053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a83e724674ef99b3a02f95d6f99edb74d6da86f3e952d96df426d2e24ffad54`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 167.0 MB (166978959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5788f6ecbfd19db9de8f1ebca0a309877c17b3a68e2b6927db7178a38dd3e2ea`  
		Last Modified: Mon, 05 May 2025 16:34:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c12c8cb54ca9170c10677abfac3c0cd2a66c86322bdbab8b6e6fe92cc0137`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477777a3fe047b2d393a11522c673d966c5106c04a594f53822905dfb3099ed`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357524fb1f1cb1c745bd69563a49c927ad2294938d4f470a351f5f65404ffdc`  
		Last Modified: Mon, 05 May 2025 16:34:59 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89b4acb36be4c123b76a5f2e389268a91bc95467c65d1b794c398fd8fb1631`  
		Last Modified: Mon, 05 May 2025 16:34:59 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0faf7dfca35f7610a11768af5806f14de92c5d3c6878fe530ace15f313771a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56563ead7314ab3dda2382afd2bc4d4d832666426dbd96304c321466b2e7722e`

```dockerfile
```

-	Layers:
	-	`sha256:001a2ba99704453b4192ecf76574a83ce56a72dc98bb29362403dd51dea2e99c`  
		Last Modified: Mon, 05 May 2025 16:34:57 GMT  
		Size: 25.9 KB (25874 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:641cd40cc4e90fff20a5e6a3388a2d862362b1ca4fbfb99227bfa4190b23ea77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192035226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972daccc52695628d0a97703050d19c600e6618b622b76f30d0fc538fab8a0c8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 10:04:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 02 May 2025 10:04:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ARG REPO_CHANNEL=stable
# Fri, 02 May 2025 10:04:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 02 May 2025 10:04:11 GMT
ARG VERSION=25.3.3.42
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 10:04:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 02 May 2025 10:04:11 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 02 May 2025 10:04:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 02 May 2025 10:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be04f390c597833173d77846d1293ad9897baf5e3a03f35936564cf8357f23d0`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 7.1 MB (7127782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63304746e0be595e8c18791c88e140ffcce7ef167770cb0eed5751a00ae24c97`  
		Last Modified: Mon, 05 May 2025 16:38:34 GMT  
		Size: 156.7 MB (156682982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3a65e1ba7a953198688fcc235a4aa5964d0f2579898b986d2df707007fade3`  
		Last Modified: Mon, 05 May 2025 16:38:29 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b201d0974da903e0cdb374d1c08192a2b464ec8048c2a9663a887ed549deb8e`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d384269f2cbb93d090459b306fac19a3f928e07fb6661a56d4a9a5a622d1676b`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b89a2a8dbd8bb92760956b84348fe7e88a495d07ab09fc6ac96aeee9be29109`  
		Last Modified: Mon, 05 May 2025 16:38:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423d17743661f544353b767293e75d841505deef68df1b0f01a77d1ae0189a8a`  
		Last Modified: Mon, 05 May 2025 16:38:31 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ce50101a43b7bc7af719b6306abf2eed03069509ccaeedb29ad994a9f08c395b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66dec5164ea12453fde66e209a44499f7785d422ad48fa1a4cdfec7132f70843`

```dockerfile
```

-	Layers:
	-	`sha256:1710dd56b0182fa3009a6a1f008d8ee7f69b543253b84d6e7738a98b83af284f`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.3-jammy`

```console
$ docker pull clickhouse@sha256:6f432bce9f74156e04db2a40fc5f5e59f05aa585194e5548368c6cbf456d63ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:b320679c5ca0b848e8c0e7ed06dbe975d5d4aa084f7e7b89ed7de34fc4b656f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc321325d517a2fc1a63924ffe8d507cb7388279b62cff337348d501785f740`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 10:04:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 02 May 2025 10:04:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ARG REPO_CHANNEL=stable
# Fri, 02 May 2025 10:04:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 02 May 2025 10:04:11 GMT
ARG VERSION=25.3.3.42
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 10:04:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 02 May 2025 10:04:11 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 02 May 2025 10:04:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 02 May 2025 10:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293c18414ddc6b5045bd255b1d3fff2b475d11f7bd01cf6f63c08323588bfeb`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 7.2 MB (7152053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a83e724674ef99b3a02f95d6f99edb74d6da86f3e952d96df426d2e24ffad54`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 167.0 MB (166978959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5788f6ecbfd19db9de8f1ebca0a309877c17b3a68e2b6927db7178a38dd3e2ea`  
		Last Modified: Mon, 05 May 2025 16:34:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c12c8cb54ca9170c10677abfac3c0cd2a66c86322bdbab8b6e6fe92cc0137`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477777a3fe047b2d393a11522c673d966c5106c04a594f53822905dfb3099ed`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357524fb1f1cb1c745bd69563a49c927ad2294938d4f470a351f5f65404ffdc`  
		Last Modified: Mon, 05 May 2025 16:34:59 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89b4acb36be4c123b76a5f2e389268a91bc95467c65d1b794c398fd8fb1631`  
		Last Modified: Mon, 05 May 2025 16:34:59 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0faf7dfca35f7610a11768af5806f14de92c5d3c6878fe530ace15f313771a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56563ead7314ab3dda2382afd2bc4d4d832666426dbd96304c321466b2e7722e`

```dockerfile
```

-	Layers:
	-	`sha256:001a2ba99704453b4192ecf76574a83ce56a72dc98bb29362403dd51dea2e99c`  
		Last Modified: Mon, 05 May 2025 16:34:57 GMT  
		Size: 25.9 KB (25874 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:641cd40cc4e90fff20a5e6a3388a2d862362b1ca4fbfb99227bfa4190b23ea77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192035226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972daccc52695628d0a97703050d19c600e6618b622b76f30d0fc538fab8a0c8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 10:04:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 02 May 2025 10:04:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ARG REPO_CHANNEL=stable
# Fri, 02 May 2025 10:04:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 02 May 2025 10:04:11 GMT
ARG VERSION=25.3.3.42
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 10:04:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 02 May 2025 10:04:11 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 02 May 2025 10:04:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 02 May 2025 10:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be04f390c597833173d77846d1293ad9897baf5e3a03f35936564cf8357f23d0`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 7.1 MB (7127782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63304746e0be595e8c18791c88e140ffcce7ef167770cb0eed5751a00ae24c97`  
		Last Modified: Mon, 05 May 2025 16:38:34 GMT  
		Size: 156.7 MB (156682982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3a65e1ba7a953198688fcc235a4aa5964d0f2579898b986d2df707007fade3`  
		Last Modified: Mon, 05 May 2025 16:38:29 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b201d0974da903e0cdb374d1c08192a2b464ec8048c2a9663a887ed549deb8e`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d384269f2cbb93d090459b306fac19a3f928e07fb6661a56d4a9a5a622d1676b`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b89a2a8dbd8bb92760956b84348fe7e88a495d07ab09fc6ac96aeee9be29109`  
		Last Modified: Mon, 05 May 2025 16:38:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423d17743661f544353b767293e75d841505deef68df1b0f01a77d1ae0189a8a`  
		Last Modified: Mon, 05 May 2025 16:38:31 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ce50101a43b7bc7af719b6306abf2eed03069509ccaeedb29ad994a9f08c395b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66dec5164ea12453fde66e209a44499f7785d422ad48fa1a4cdfec7132f70843`

```dockerfile
```

-	Layers:
	-	`sha256:1710dd56b0182fa3009a6a1f008d8ee7f69b543253b84d6e7738a98b83af284f`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.3.42`

```console
$ docker pull clickhouse@sha256:6f432bce9f74156e04db2a40fc5f5e59f05aa585194e5548368c6cbf456d63ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.3.42` - linux; amd64

```console
$ docker pull clickhouse@sha256:b320679c5ca0b848e8c0e7ed06dbe975d5d4aa084f7e7b89ed7de34fc4b656f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc321325d517a2fc1a63924ffe8d507cb7388279b62cff337348d501785f740`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 10:04:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 02 May 2025 10:04:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ARG REPO_CHANNEL=stable
# Fri, 02 May 2025 10:04:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 02 May 2025 10:04:11 GMT
ARG VERSION=25.3.3.42
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 10:04:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 02 May 2025 10:04:11 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 02 May 2025 10:04:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 02 May 2025 10:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293c18414ddc6b5045bd255b1d3fff2b475d11f7bd01cf6f63c08323588bfeb`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 7.2 MB (7152053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a83e724674ef99b3a02f95d6f99edb74d6da86f3e952d96df426d2e24ffad54`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 167.0 MB (166978959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5788f6ecbfd19db9de8f1ebca0a309877c17b3a68e2b6927db7178a38dd3e2ea`  
		Last Modified: Mon, 05 May 2025 16:34:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c12c8cb54ca9170c10677abfac3c0cd2a66c86322bdbab8b6e6fe92cc0137`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477777a3fe047b2d393a11522c673d966c5106c04a594f53822905dfb3099ed`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357524fb1f1cb1c745bd69563a49c927ad2294938d4f470a351f5f65404ffdc`  
		Last Modified: Mon, 05 May 2025 16:34:59 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89b4acb36be4c123b76a5f2e389268a91bc95467c65d1b794c398fd8fb1631`  
		Last Modified: Mon, 05 May 2025 16:34:59 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.3.42` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0faf7dfca35f7610a11768af5806f14de92c5d3c6878fe530ace15f313771a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56563ead7314ab3dda2382afd2bc4d4d832666426dbd96304c321466b2e7722e`

```dockerfile
```

-	Layers:
	-	`sha256:001a2ba99704453b4192ecf76574a83ce56a72dc98bb29362403dd51dea2e99c`  
		Last Modified: Mon, 05 May 2025 16:34:57 GMT  
		Size: 25.9 KB (25874 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.3.42` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:641cd40cc4e90fff20a5e6a3388a2d862362b1ca4fbfb99227bfa4190b23ea77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192035226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972daccc52695628d0a97703050d19c600e6618b622b76f30d0fc538fab8a0c8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 10:04:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 02 May 2025 10:04:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ARG REPO_CHANNEL=stable
# Fri, 02 May 2025 10:04:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 02 May 2025 10:04:11 GMT
ARG VERSION=25.3.3.42
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 10:04:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 02 May 2025 10:04:11 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 02 May 2025 10:04:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 02 May 2025 10:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be04f390c597833173d77846d1293ad9897baf5e3a03f35936564cf8357f23d0`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 7.1 MB (7127782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63304746e0be595e8c18791c88e140ffcce7ef167770cb0eed5751a00ae24c97`  
		Last Modified: Mon, 05 May 2025 16:38:34 GMT  
		Size: 156.7 MB (156682982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3a65e1ba7a953198688fcc235a4aa5964d0f2579898b986d2df707007fade3`  
		Last Modified: Mon, 05 May 2025 16:38:29 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b201d0974da903e0cdb374d1c08192a2b464ec8048c2a9663a887ed549deb8e`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d384269f2cbb93d090459b306fac19a3f928e07fb6661a56d4a9a5a622d1676b`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b89a2a8dbd8bb92760956b84348fe7e88a495d07ab09fc6ac96aeee9be29109`  
		Last Modified: Mon, 05 May 2025 16:38:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423d17743661f544353b767293e75d841505deef68df1b0f01a77d1ae0189a8a`  
		Last Modified: Mon, 05 May 2025 16:38:31 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.3.42` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ce50101a43b7bc7af719b6306abf2eed03069509ccaeedb29ad994a9f08c395b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66dec5164ea12453fde66e209a44499f7785d422ad48fa1a4cdfec7132f70843`

```dockerfile
```

-	Layers:
	-	`sha256:1710dd56b0182fa3009a6a1f008d8ee7f69b543253b84d6e7738a98b83af284f`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.3.42-jammy`

```console
$ docker pull clickhouse@sha256:6f432bce9f74156e04db2a40fc5f5e59f05aa585194e5548368c6cbf456d63ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.3.42-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:b320679c5ca0b848e8c0e7ed06dbe975d5d4aa084f7e7b89ed7de34fc4b656f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc321325d517a2fc1a63924ffe8d507cb7388279b62cff337348d501785f740`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 10:04:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 02 May 2025 10:04:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ARG REPO_CHANNEL=stable
# Fri, 02 May 2025 10:04:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 02 May 2025 10:04:11 GMT
ARG VERSION=25.3.3.42
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 10:04:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 02 May 2025 10:04:11 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 02 May 2025 10:04:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 02 May 2025 10:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293c18414ddc6b5045bd255b1d3fff2b475d11f7bd01cf6f63c08323588bfeb`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 7.2 MB (7152053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a83e724674ef99b3a02f95d6f99edb74d6da86f3e952d96df426d2e24ffad54`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 167.0 MB (166978959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5788f6ecbfd19db9de8f1ebca0a309877c17b3a68e2b6927db7178a38dd3e2ea`  
		Last Modified: Mon, 05 May 2025 16:34:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c12c8cb54ca9170c10677abfac3c0cd2a66c86322bdbab8b6e6fe92cc0137`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477777a3fe047b2d393a11522c673d966c5106c04a594f53822905dfb3099ed`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357524fb1f1cb1c745bd69563a49c927ad2294938d4f470a351f5f65404ffdc`  
		Last Modified: Mon, 05 May 2025 16:34:59 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89b4acb36be4c123b76a5f2e389268a91bc95467c65d1b794c398fd8fb1631`  
		Last Modified: Mon, 05 May 2025 16:34:59 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.3.42-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0faf7dfca35f7610a11768af5806f14de92c5d3c6878fe530ace15f313771a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56563ead7314ab3dda2382afd2bc4d4d832666426dbd96304c321466b2e7722e`

```dockerfile
```

-	Layers:
	-	`sha256:001a2ba99704453b4192ecf76574a83ce56a72dc98bb29362403dd51dea2e99c`  
		Last Modified: Mon, 05 May 2025 16:34:57 GMT  
		Size: 25.9 KB (25874 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.3.42-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:641cd40cc4e90fff20a5e6a3388a2d862362b1ca4fbfb99227bfa4190b23ea77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192035226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972daccc52695628d0a97703050d19c600e6618b622b76f30d0fc538fab8a0c8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 10:04:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 02 May 2025 10:04:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ARG REPO_CHANNEL=stable
# Fri, 02 May 2025 10:04:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 02 May 2025 10:04:11 GMT
ARG VERSION=25.3.3.42
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 10:04:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 02 May 2025 10:04:11 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 02 May 2025 10:04:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 02 May 2025 10:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be04f390c597833173d77846d1293ad9897baf5e3a03f35936564cf8357f23d0`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 7.1 MB (7127782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63304746e0be595e8c18791c88e140ffcce7ef167770cb0eed5751a00ae24c97`  
		Last Modified: Mon, 05 May 2025 16:38:34 GMT  
		Size: 156.7 MB (156682982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3a65e1ba7a953198688fcc235a4aa5964d0f2579898b986d2df707007fade3`  
		Last Modified: Mon, 05 May 2025 16:38:29 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b201d0974da903e0cdb374d1c08192a2b464ec8048c2a9663a887ed549deb8e`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d384269f2cbb93d090459b306fac19a3f928e07fb6661a56d4a9a5a622d1676b`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b89a2a8dbd8bb92760956b84348fe7e88a495d07ab09fc6ac96aeee9be29109`  
		Last Modified: Mon, 05 May 2025 16:38:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423d17743661f544353b767293e75d841505deef68df1b0f01a77d1ae0189a8a`  
		Last Modified: Mon, 05 May 2025 16:38:31 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.3.42-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ce50101a43b7bc7af719b6306abf2eed03069509ccaeedb29ad994a9f08c395b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66dec5164ea12453fde66e209a44499f7785d422ad48fa1a4cdfec7132f70843`

```dockerfile
```

-	Layers:
	-	`sha256:1710dd56b0182fa3009a6a1f008d8ee7f69b543253b84d6e7738a98b83af284f`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4`

```console
$ docker pull clickhouse@sha256:0c9b78643e9f8353c6c70691a02b9c239bb1698f41c4079c2a497fd757b6ada1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:8f18a0a41064a847a58cdfa6bc4ced18dcd85dee3914b6b79affbcce305a4899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202712439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54d9220cf005c72809763cbe7fcedede132e3128081166f3883960dacd9cda7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.4.5.24
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f090d5d18ed15ad952071b0b9e68a26650431bcc0c7568362e280a1d8c9f671`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 7.2 MB (7152064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d3671b86b58814c1c85212ac19e3d4335494023d20d8fe2a70a38ac85ce38f`  
		Last Modified: Fri, 23 May 2025 17:04:53 GMT  
		Size: 165.2 MB (165157516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053fab35d35352fccdc3b3dc8dbb20aa57cae688d23b974adb07848d418dc06a`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c3c02cd73c3179e3f39545284dea6df6165aa173b87bd750e3cbeb7b7c0e6`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca2179e29aa3e3e31bdb8c5af84bf490dbfc2fa3a4bc2e190433b01ae6670c9`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a3d548800afdaf5a9a252bf3c35785e73c476bbb488b9f32ad251942307c19`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc2fc426e0fe087246f182c37929286c0723f48953f5b7df09d31dcfeb8fcaf`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d61d43e237d77f810d6fe50e2d8b597224a9be32593da01438e1ae3eb97ee3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28238f781c8ffd1564f0c648f77a7dc07d8e93d4f718c553ce1010e52f0ee1b8`

```dockerfile
```

-	Layers:
	-	`sha256:40bf9cc732ac01f470c1c56c2580e1ad40bb7ae98400e7eda19fd961a9d7c347`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:85672aa19880b47aaa3647768b8315761cc1e6c6ef330c88035766b29099bc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190044446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a69a2d77cede81baf8eb7a3b557c3a7757f51f6b35571801517681939b7506`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.4.5.24
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c58a873289c5dd324c5060870267f03e8fe2a30e6694e5dc4f0199253b42`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 7.1 MB (7127767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bacf7b8c12506d93d671f38819a615bb2a4985c9c6de1749ac0a2c253d649c`  
		Last Modified: Fri, 23 May 2025 17:05:46 GMT  
		Size: 154.7 MB (154692220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6287325af859b31cbc767ee257165a26f760006628622650741d6715606ac575`  
		Last Modified: Fri, 23 May 2025 17:05:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55835426d5ba35efa2b18a917faf8bcfe7dd332c507cdc27b8052ad96b8c4bb8`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a34d6f22fe224e14460fede16f7ce21935735946045250c8da410e523f9636f`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7117830de723757d1c4295958cf8fc1e2a568a86603e327cd2bd1a0e79c2725c`  
		Last Modified: Fri, 23 May 2025 17:05:44 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24100be7f8dc12ea86405c0e88ecfa5fdf0c3d23514eb01a8a3daf8cc396f295`  
		Last Modified: Fri, 23 May 2025 17:05:44 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e00bfc0ac14ea962ce6c14bd33ee0939e8c042373529993949df909eb94cc0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfffe73b1e1bd4ca6160e098e256a4c0396bcf5c5a2db557d356ba71c5f8abd`

```dockerfile
```

-	Layers:
	-	`sha256:64b9ab6ac788fa82be2ecad366e2852fa1b1889f1b1844d8d80dff8029e2c535`  
		Last Modified: Fri, 23 May 2025 17:05:42 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4-jammy`

```console
$ docker pull clickhouse@sha256:0c9b78643e9f8353c6c70691a02b9c239bb1698f41c4079c2a497fd757b6ada1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8f18a0a41064a847a58cdfa6bc4ced18dcd85dee3914b6b79affbcce305a4899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202712439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54d9220cf005c72809763cbe7fcedede132e3128081166f3883960dacd9cda7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.4.5.24
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f090d5d18ed15ad952071b0b9e68a26650431bcc0c7568362e280a1d8c9f671`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 7.2 MB (7152064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d3671b86b58814c1c85212ac19e3d4335494023d20d8fe2a70a38ac85ce38f`  
		Last Modified: Fri, 23 May 2025 17:04:53 GMT  
		Size: 165.2 MB (165157516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053fab35d35352fccdc3b3dc8dbb20aa57cae688d23b974adb07848d418dc06a`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c3c02cd73c3179e3f39545284dea6df6165aa173b87bd750e3cbeb7b7c0e6`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca2179e29aa3e3e31bdb8c5af84bf490dbfc2fa3a4bc2e190433b01ae6670c9`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a3d548800afdaf5a9a252bf3c35785e73c476bbb488b9f32ad251942307c19`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc2fc426e0fe087246f182c37929286c0723f48953f5b7df09d31dcfeb8fcaf`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d61d43e237d77f810d6fe50e2d8b597224a9be32593da01438e1ae3eb97ee3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28238f781c8ffd1564f0c648f77a7dc07d8e93d4f718c553ce1010e52f0ee1b8`

```dockerfile
```

-	Layers:
	-	`sha256:40bf9cc732ac01f470c1c56c2580e1ad40bb7ae98400e7eda19fd961a9d7c347`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:85672aa19880b47aaa3647768b8315761cc1e6c6ef330c88035766b29099bc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190044446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a69a2d77cede81baf8eb7a3b557c3a7757f51f6b35571801517681939b7506`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.4.5.24
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c58a873289c5dd324c5060870267f03e8fe2a30e6694e5dc4f0199253b42`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 7.1 MB (7127767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bacf7b8c12506d93d671f38819a615bb2a4985c9c6de1749ac0a2c253d649c`  
		Last Modified: Fri, 23 May 2025 17:05:46 GMT  
		Size: 154.7 MB (154692220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6287325af859b31cbc767ee257165a26f760006628622650741d6715606ac575`  
		Last Modified: Fri, 23 May 2025 17:05:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55835426d5ba35efa2b18a917faf8bcfe7dd332c507cdc27b8052ad96b8c4bb8`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a34d6f22fe224e14460fede16f7ce21935735946045250c8da410e523f9636f`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7117830de723757d1c4295958cf8fc1e2a568a86603e327cd2bd1a0e79c2725c`  
		Last Modified: Fri, 23 May 2025 17:05:44 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24100be7f8dc12ea86405c0e88ecfa5fdf0c3d23514eb01a8a3daf8cc396f295`  
		Last Modified: Fri, 23 May 2025 17:05:44 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e00bfc0ac14ea962ce6c14bd33ee0939e8c042373529993949df909eb94cc0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfffe73b1e1bd4ca6160e098e256a4c0396bcf5c5a2db557d356ba71c5f8abd`

```dockerfile
```

-	Layers:
	-	`sha256:64b9ab6ac788fa82be2ecad366e2852fa1b1889f1b1844d8d80dff8029e2c535`  
		Last Modified: Fri, 23 May 2025 17:05:42 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.5`

```console
$ docker pull clickhouse@sha256:0c9b78643e9f8353c6c70691a02b9c239bb1698f41c4079c2a497fd757b6ada1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:8f18a0a41064a847a58cdfa6bc4ced18dcd85dee3914b6b79affbcce305a4899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202712439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54d9220cf005c72809763cbe7fcedede132e3128081166f3883960dacd9cda7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.4.5.24
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f090d5d18ed15ad952071b0b9e68a26650431bcc0c7568362e280a1d8c9f671`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 7.2 MB (7152064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d3671b86b58814c1c85212ac19e3d4335494023d20d8fe2a70a38ac85ce38f`  
		Last Modified: Fri, 23 May 2025 17:04:53 GMT  
		Size: 165.2 MB (165157516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053fab35d35352fccdc3b3dc8dbb20aa57cae688d23b974adb07848d418dc06a`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c3c02cd73c3179e3f39545284dea6df6165aa173b87bd750e3cbeb7b7c0e6`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca2179e29aa3e3e31bdb8c5af84bf490dbfc2fa3a4bc2e190433b01ae6670c9`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a3d548800afdaf5a9a252bf3c35785e73c476bbb488b9f32ad251942307c19`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc2fc426e0fe087246f182c37929286c0723f48953f5b7df09d31dcfeb8fcaf`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d61d43e237d77f810d6fe50e2d8b597224a9be32593da01438e1ae3eb97ee3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28238f781c8ffd1564f0c648f77a7dc07d8e93d4f718c553ce1010e52f0ee1b8`

```dockerfile
```

-	Layers:
	-	`sha256:40bf9cc732ac01f470c1c56c2580e1ad40bb7ae98400e7eda19fd961a9d7c347`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:85672aa19880b47aaa3647768b8315761cc1e6c6ef330c88035766b29099bc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190044446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a69a2d77cede81baf8eb7a3b557c3a7757f51f6b35571801517681939b7506`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.4.5.24
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c58a873289c5dd324c5060870267f03e8fe2a30e6694e5dc4f0199253b42`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 7.1 MB (7127767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bacf7b8c12506d93d671f38819a615bb2a4985c9c6de1749ac0a2c253d649c`  
		Last Modified: Fri, 23 May 2025 17:05:46 GMT  
		Size: 154.7 MB (154692220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6287325af859b31cbc767ee257165a26f760006628622650741d6715606ac575`  
		Last Modified: Fri, 23 May 2025 17:05:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55835426d5ba35efa2b18a917faf8bcfe7dd332c507cdc27b8052ad96b8c4bb8`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a34d6f22fe224e14460fede16f7ce21935735946045250c8da410e523f9636f`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7117830de723757d1c4295958cf8fc1e2a568a86603e327cd2bd1a0e79c2725c`  
		Last Modified: Fri, 23 May 2025 17:05:44 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24100be7f8dc12ea86405c0e88ecfa5fdf0c3d23514eb01a8a3daf8cc396f295`  
		Last Modified: Fri, 23 May 2025 17:05:44 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e00bfc0ac14ea962ce6c14bd33ee0939e8c042373529993949df909eb94cc0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfffe73b1e1bd4ca6160e098e256a4c0396bcf5c5a2db557d356ba71c5f8abd`

```dockerfile
```

-	Layers:
	-	`sha256:64b9ab6ac788fa82be2ecad366e2852fa1b1889f1b1844d8d80dff8029e2c535`  
		Last Modified: Fri, 23 May 2025 17:05:42 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.5-jammy`

```console
$ docker pull clickhouse@sha256:0c9b78643e9f8353c6c70691a02b9c239bb1698f41c4079c2a497fd757b6ada1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8f18a0a41064a847a58cdfa6bc4ced18dcd85dee3914b6b79affbcce305a4899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202712439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54d9220cf005c72809763cbe7fcedede132e3128081166f3883960dacd9cda7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.4.5.24
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f090d5d18ed15ad952071b0b9e68a26650431bcc0c7568362e280a1d8c9f671`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 7.2 MB (7152064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d3671b86b58814c1c85212ac19e3d4335494023d20d8fe2a70a38ac85ce38f`  
		Last Modified: Fri, 23 May 2025 17:04:53 GMT  
		Size: 165.2 MB (165157516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053fab35d35352fccdc3b3dc8dbb20aa57cae688d23b974adb07848d418dc06a`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c3c02cd73c3179e3f39545284dea6df6165aa173b87bd750e3cbeb7b7c0e6`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca2179e29aa3e3e31bdb8c5af84bf490dbfc2fa3a4bc2e190433b01ae6670c9`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a3d548800afdaf5a9a252bf3c35785e73c476bbb488b9f32ad251942307c19`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc2fc426e0fe087246f182c37929286c0723f48953f5b7df09d31dcfeb8fcaf`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d61d43e237d77f810d6fe50e2d8b597224a9be32593da01438e1ae3eb97ee3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28238f781c8ffd1564f0c648f77a7dc07d8e93d4f718c553ce1010e52f0ee1b8`

```dockerfile
```

-	Layers:
	-	`sha256:40bf9cc732ac01f470c1c56c2580e1ad40bb7ae98400e7eda19fd961a9d7c347`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:85672aa19880b47aaa3647768b8315761cc1e6c6ef330c88035766b29099bc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190044446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a69a2d77cede81baf8eb7a3b557c3a7757f51f6b35571801517681939b7506`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.4.5.24
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c58a873289c5dd324c5060870267f03e8fe2a30e6694e5dc4f0199253b42`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 7.1 MB (7127767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bacf7b8c12506d93d671f38819a615bb2a4985c9c6de1749ac0a2c253d649c`  
		Last Modified: Fri, 23 May 2025 17:05:46 GMT  
		Size: 154.7 MB (154692220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6287325af859b31cbc767ee257165a26f760006628622650741d6715606ac575`  
		Last Modified: Fri, 23 May 2025 17:05:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55835426d5ba35efa2b18a917faf8bcfe7dd332c507cdc27b8052ad96b8c4bb8`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a34d6f22fe224e14460fede16f7ce21935735946045250c8da410e523f9636f`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7117830de723757d1c4295958cf8fc1e2a568a86603e327cd2bd1a0e79c2725c`  
		Last Modified: Fri, 23 May 2025 17:05:44 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24100be7f8dc12ea86405c0e88ecfa5fdf0c3d23514eb01a8a3daf8cc396f295`  
		Last Modified: Fri, 23 May 2025 17:05:44 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e00bfc0ac14ea962ce6c14bd33ee0939e8c042373529993949df909eb94cc0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfffe73b1e1bd4ca6160e098e256a4c0396bcf5c5a2db557d356ba71c5f8abd`

```dockerfile
```

-	Layers:
	-	`sha256:64b9ab6ac788fa82be2ecad366e2852fa1b1889f1b1844d8d80dff8029e2c535`  
		Last Modified: Fri, 23 May 2025 17:05:42 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.5.24`

```console
$ docker pull clickhouse@sha256:0c9b78643e9f8353c6c70691a02b9c239bb1698f41c4079c2a497fd757b6ada1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.5.24` - linux; amd64

```console
$ docker pull clickhouse@sha256:8f18a0a41064a847a58cdfa6bc4ced18dcd85dee3914b6b79affbcce305a4899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202712439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54d9220cf005c72809763cbe7fcedede132e3128081166f3883960dacd9cda7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.4.5.24
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f090d5d18ed15ad952071b0b9e68a26650431bcc0c7568362e280a1d8c9f671`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 7.2 MB (7152064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d3671b86b58814c1c85212ac19e3d4335494023d20d8fe2a70a38ac85ce38f`  
		Last Modified: Fri, 23 May 2025 17:04:53 GMT  
		Size: 165.2 MB (165157516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053fab35d35352fccdc3b3dc8dbb20aa57cae688d23b974adb07848d418dc06a`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c3c02cd73c3179e3f39545284dea6df6165aa173b87bd750e3cbeb7b7c0e6`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca2179e29aa3e3e31bdb8c5af84bf490dbfc2fa3a4bc2e190433b01ae6670c9`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a3d548800afdaf5a9a252bf3c35785e73c476bbb488b9f32ad251942307c19`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc2fc426e0fe087246f182c37929286c0723f48953f5b7df09d31dcfeb8fcaf`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.5.24` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d61d43e237d77f810d6fe50e2d8b597224a9be32593da01438e1ae3eb97ee3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28238f781c8ffd1564f0c648f77a7dc07d8e93d4f718c553ce1010e52f0ee1b8`

```dockerfile
```

-	Layers:
	-	`sha256:40bf9cc732ac01f470c1c56c2580e1ad40bb7ae98400e7eda19fd961a9d7c347`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.5.24` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:85672aa19880b47aaa3647768b8315761cc1e6c6ef330c88035766b29099bc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190044446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a69a2d77cede81baf8eb7a3b557c3a7757f51f6b35571801517681939b7506`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.4.5.24
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c58a873289c5dd324c5060870267f03e8fe2a30e6694e5dc4f0199253b42`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 7.1 MB (7127767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bacf7b8c12506d93d671f38819a615bb2a4985c9c6de1749ac0a2c253d649c`  
		Last Modified: Fri, 23 May 2025 17:05:46 GMT  
		Size: 154.7 MB (154692220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6287325af859b31cbc767ee257165a26f760006628622650741d6715606ac575`  
		Last Modified: Fri, 23 May 2025 17:05:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55835426d5ba35efa2b18a917faf8bcfe7dd332c507cdc27b8052ad96b8c4bb8`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a34d6f22fe224e14460fede16f7ce21935735946045250c8da410e523f9636f`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7117830de723757d1c4295958cf8fc1e2a568a86603e327cd2bd1a0e79c2725c`  
		Last Modified: Fri, 23 May 2025 17:05:44 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24100be7f8dc12ea86405c0e88ecfa5fdf0c3d23514eb01a8a3daf8cc396f295`  
		Last Modified: Fri, 23 May 2025 17:05:44 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.5.24` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e00bfc0ac14ea962ce6c14bd33ee0939e8c042373529993949df909eb94cc0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfffe73b1e1bd4ca6160e098e256a4c0396bcf5c5a2db557d356ba71c5f8abd`

```dockerfile
```

-	Layers:
	-	`sha256:64b9ab6ac788fa82be2ecad366e2852fa1b1889f1b1844d8d80dff8029e2c535`  
		Last Modified: Fri, 23 May 2025 17:05:42 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.5.24-jammy`

```console
$ docker pull clickhouse@sha256:0c9b78643e9f8353c6c70691a02b9c239bb1698f41c4079c2a497fd757b6ada1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.5.24-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8f18a0a41064a847a58cdfa6bc4ced18dcd85dee3914b6b79affbcce305a4899
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202712439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54d9220cf005c72809763cbe7fcedede132e3128081166f3883960dacd9cda7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.4.5.24
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f090d5d18ed15ad952071b0b9e68a26650431bcc0c7568362e280a1d8c9f671`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 7.2 MB (7152064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d3671b86b58814c1c85212ac19e3d4335494023d20d8fe2a70a38ac85ce38f`  
		Last Modified: Fri, 23 May 2025 17:04:53 GMT  
		Size: 165.2 MB (165157516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053fab35d35352fccdc3b3dc8dbb20aa57cae688d23b974adb07848d418dc06a`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890c3c02cd73c3179e3f39545284dea6df6165aa173b87bd750e3cbeb7b7c0e6`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca2179e29aa3e3e31bdb8c5af84bf490dbfc2fa3a4bc2e190433b01ae6670c9`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a3d548800afdaf5a9a252bf3c35785e73c476bbb488b9f32ad251942307c19`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc2fc426e0fe087246f182c37929286c0723f48953f5b7df09d31dcfeb8fcaf`  
		Last Modified: Fri, 23 May 2025 17:04:51 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.5.24-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d61d43e237d77f810d6fe50e2d8b597224a9be32593da01438e1ae3eb97ee3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28238f781c8ffd1564f0c648f77a7dc07d8e93d4f718c553ce1010e52f0ee1b8`

```dockerfile
```

-	Layers:
	-	`sha256:40bf9cc732ac01f470c1c56c2580e1ad40bb7ae98400e7eda19fd961a9d7c347`  
		Last Modified: Fri, 23 May 2025 17:04:50 GMT  
		Size: 25.3 KB (25262 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.5.24-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:85672aa19880b47aaa3647768b8315761cc1e6c6ef330c88035766b29099bc8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190044446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69a69a2d77cede81baf8eb7a3b557c3a7757f51f6b35571801517681939b7506`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.4.5.24
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.5.24 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f700c58a873289c5dd324c5060870267f03e8fe2a30e6694e5dc4f0199253b42`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 7.1 MB (7127767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27bacf7b8c12506d93d671f38819a615bb2a4985c9c6de1749ac0a2c253d649c`  
		Last Modified: Fri, 23 May 2025 17:05:46 GMT  
		Size: 154.7 MB (154692220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6287325af859b31cbc767ee257165a26f760006628622650741d6715606ac575`  
		Last Modified: Fri, 23 May 2025 17:05:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55835426d5ba35efa2b18a917faf8bcfe7dd332c507cdc27b8052ad96b8c4bb8`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a34d6f22fe224e14460fede16f7ce21935735946045250c8da410e523f9636f`  
		Last Modified: Fri, 23 May 2025 17:05:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7117830de723757d1c4295958cf8fc1e2a568a86603e327cd2bd1a0e79c2725c`  
		Last Modified: Fri, 23 May 2025 17:05:44 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24100be7f8dc12ea86405c0e88ecfa5fdf0c3d23514eb01a8a3daf8cc396f295`  
		Last Modified: Fri, 23 May 2025 17:05:44 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.5.24-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e00bfc0ac14ea962ce6c14bd33ee0939e8c042373529993949df909eb94cc0d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfffe73b1e1bd4ca6160e098e256a4c0396bcf5c5a2db557d356ba71c5f8abd`

```dockerfile
```

-	Layers:
	-	`sha256:64b9ab6ac788fa82be2ecad366e2852fa1b1889f1b1844d8d80dff8029e2c535`  
		Last Modified: Fri, 23 May 2025 17:05:42 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5`

```console
$ docker pull clickhouse@sha256:470114515e8ef26bf10020e6949b04c9dc75722ca0a2c98bb82c027327f13c80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:e96b2a65a4972f96046e7095ab89c2f7bf6cde9225bcaba3added5553a3665ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205992665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828b3e01aa7864ededf4583c3695daece684cd54e266ae1e4481f6993467044d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd180e99af6e8a635c124ac88a22ef63cf17cff53e537fdfcd0804fadad61fc6`  
		Last Modified: Fri, 23 May 2025 17:05:04 GMT  
		Size: 7.2 MB (7151944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f7d54a227de8f904f2cbb8bd6a1d5c8f766257835dc829e9762ef6f2ca8dc4`  
		Last Modified: Fri, 23 May 2025 17:05:08 GMT  
		Size: 168.4 MB (168437865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edbd4b6fd576d2b6a81c633486aa0ae4a45560c7e104dd9e03529749d7c6f48`  
		Last Modified: Fri, 23 May 2025 17:05:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e511784a70985fed75bb4766e0bc1dd3e8483c0a01b72c4bd3f2e4ac952c30`  
		Last Modified: Fri, 23 May 2025 17:05:04 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593969705065da1263004c4ee7ca56fe3aeed1fbebcb9b5f0a01a95e5af950db`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65aec7ae4592ef3f7195bf07e65ccb314d703c500dee178399a7674ebb22ac2`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a45b6a11d04db702333075b27c54cfe03908ed78dd458bf38f0658ad425d0bc`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cbd8008a9ef82f0188ec7d793b9795a3b91fadf8afd2028a6d58bdfb18216d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac21aa5774e2acbd638f4e2063aa2ae38353820934905da4edc7d620aa78077`

```dockerfile
```

-	Layers:
	-	`sha256:4e27de348195003815d254c7810735b47071050392ebdce1b4af948733cfee9d`  
		Last Modified: Fri, 23 May 2025 17:05:03 GMT  
		Size: 25.9 KB (25898 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4464c90becdde299168c0f06d1218a90865a4bdbe22be2a4118fa509b5feb96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192487306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc18fcff80fd20c45952f6b567c68429836bf6510ffa7a0aca376eaad4a85b6b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eb6f6d756f55bb7432895aca56cba74e904a26438e38de6fa4fb747558c7bc`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 7.1 MB (7127794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007fedfcc03b5b7abd18606ac24e2e3cca135fcdd3f0d70b7aba8348a88baff`  
		Last Modified: Fri, 23 May 2025 17:04:44 GMT  
		Size: 157.1 MB (157135055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c5000478ac61b52cd1d3ac64a845ef1f5dc803edb9b7bbb1c4aed0b9bff722`  
		Last Modified: Fri, 23 May 2025 17:04:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfea4819b2811e369c70b8633fecdc9aa0ebf72abef51249efe4d0f392d12e92`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6ad83ffb10b9c9e2bcfadda7149c1440b5066db63e6eb2d346fb693229daca`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67db376579d9069deafa02f84c6d4316295e74911b16083e17b4826ecac21d`  
		Last Modified: Fri, 23 May 2025 17:04:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc8eee9198db9da70a05bff9f57e1af7273da8867bc4cbb17cc907774c0ea23`  
		Last Modified: Fri, 23 May 2025 17:04:42 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d4ff4620d1db9265b0deeab3213905058f2365fbaacaef01676dd2aa508a4954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b35a4ad0720bdac55cac7b0db6bd7535bbf7543ce437811d782f6d4e2be28c`

```dockerfile
```

-	Layers:
	-	`sha256:375b78d42bcd4520fb8fc1071063fdd1a14c65683c3331fc9607b38b60023d8a`  
		Last Modified: Fri, 23 May 2025 17:04:40 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5-jammy`

```console
$ docker pull clickhouse@sha256:470114515e8ef26bf10020e6949b04c9dc75722ca0a2c98bb82c027327f13c80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e96b2a65a4972f96046e7095ab89c2f7bf6cde9225bcaba3added5553a3665ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205992665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828b3e01aa7864ededf4583c3695daece684cd54e266ae1e4481f6993467044d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd180e99af6e8a635c124ac88a22ef63cf17cff53e537fdfcd0804fadad61fc6`  
		Last Modified: Fri, 23 May 2025 17:05:04 GMT  
		Size: 7.2 MB (7151944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f7d54a227de8f904f2cbb8bd6a1d5c8f766257835dc829e9762ef6f2ca8dc4`  
		Last Modified: Fri, 23 May 2025 17:05:08 GMT  
		Size: 168.4 MB (168437865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edbd4b6fd576d2b6a81c633486aa0ae4a45560c7e104dd9e03529749d7c6f48`  
		Last Modified: Fri, 23 May 2025 17:05:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e511784a70985fed75bb4766e0bc1dd3e8483c0a01b72c4bd3f2e4ac952c30`  
		Last Modified: Fri, 23 May 2025 17:05:04 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593969705065da1263004c4ee7ca56fe3aeed1fbebcb9b5f0a01a95e5af950db`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65aec7ae4592ef3f7195bf07e65ccb314d703c500dee178399a7674ebb22ac2`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a45b6a11d04db702333075b27c54cfe03908ed78dd458bf38f0658ad425d0bc`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cbd8008a9ef82f0188ec7d793b9795a3b91fadf8afd2028a6d58bdfb18216d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac21aa5774e2acbd638f4e2063aa2ae38353820934905da4edc7d620aa78077`

```dockerfile
```

-	Layers:
	-	`sha256:4e27de348195003815d254c7810735b47071050392ebdce1b4af948733cfee9d`  
		Last Modified: Fri, 23 May 2025 17:05:03 GMT  
		Size: 25.9 KB (25898 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4464c90becdde299168c0f06d1218a90865a4bdbe22be2a4118fa509b5feb96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192487306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc18fcff80fd20c45952f6b567c68429836bf6510ffa7a0aca376eaad4a85b6b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eb6f6d756f55bb7432895aca56cba74e904a26438e38de6fa4fb747558c7bc`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 7.1 MB (7127794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007fedfcc03b5b7abd18606ac24e2e3cca135fcdd3f0d70b7aba8348a88baff`  
		Last Modified: Fri, 23 May 2025 17:04:44 GMT  
		Size: 157.1 MB (157135055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c5000478ac61b52cd1d3ac64a845ef1f5dc803edb9b7bbb1c4aed0b9bff722`  
		Last Modified: Fri, 23 May 2025 17:04:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfea4819b2811e369c70b8633fecdc9aa0ebf72abef51249efe4d0f392d12e92`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6ad83ffb10b9c9e2bcfadda7149c1440b5066db63e6eb2d346fb693229daca`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67db376579d9069deafa02f84c6d4316295e74911b16083e17b4826ecac21d`  
		Last Modified: Fri, 23 May 2025 17:04:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc8eee9198db9da70a05bff9f57e1af7273da8867bc4cbb17cc907774c0ea23`  
		Last Modified: Fri, 23 May 2025 17:04:42 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d4ff4620d1db9265b0deeab3213905058f2365fbaacaef01676dd2aa508a4954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b35a4ad0720bdac55cac7b0db6bd7535bbf7543ce437811d782f6d4e2be28c`

```dockerfile
```

-	Layers:
	-	`sha256:375b78d42bcd4520fb8fc1071063fdd1a14c65683c3331fc9607b38b60023d8a`  
		Last Modified: Fri, 23 May 2025 17:04:40 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.1`

```console
$ docker pull clickhouse@sha256:470114515e8ef26bf10020e6949b04c9dc75722ca0a2c98bb82c027327f13c80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:e96b2a65a4972f96046e7095ab89c2f7bf6cde9225bcaba3added5553a3665ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205992665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828b3e01aa7864ededf4583c3695daece684cd54e266ae1e4481f6993467044d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd180e99af6e8a635c124ac88a22ef63cf17cff53e537fdfcd0804fadad61fc6`  
		Last Modified: Fri, 23 May 2025 17:05:04 GMT  
		Size: 7.2 MB (7151944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f7d54a227de8f904f2cbb8bd6a1d5c8f766257835dc829e9762ef6f2ca8dc4`  
		Last Modified: Fri, 23 May 2025 17:05:08 GMT  
		Size: 168.4 MB (168437865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edbd4b6fd576d2b6a81c633486aa0ae4a45560c7e104dd9e03529749d7c6f48`  
		Last Modified: Fri, 23 May 2025 17:05:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e511784a70985fed75bb4766e0bc1dd3e8483c0a01b72c4bd3f2e4ac952c30`  
		Last Modified: Fri, 23 May 2025 17:05:04 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593969705065da1263004c4ee7ca56fe3aeed1fbebcb9b5f0a01a95e5af950db`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65aec7ae4592ef3f7195bf07e65ccb314d703c500dee178399a7674ebb22ac2`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a45b6a11d04db702333075b27c54cfe03908ed78dd458bf38f0658ad425d0bc`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cbd8008a9ef82f0188ec7d793b9795a3b91fadf8afd2028a6d58bdfb18216d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac21aa5774e2acbd638f4e2063aa2ae38353820934905da4edc7d620aa78077`

```dockerfile
```

-	Layers:
	-	`sha256:4e27de348195003815d254c7810735b47071050392ebdce1b4af948733cfee9d`  
		Last Modified: Fri, 23 May 2025 17:05:03 GMT  
		Size: 25.9 KB (25898 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4464c90becdde299168c0f06d1218a90865a4bdbe22be2a4118fa509b5feb96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192487306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc18fcff80fd20c45952f6b567c68429836bf6510ffa7a0aca376eaad4a85b6b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eb6f6d756f55bb7432895aca56cba74e904a26438e38de6fa4fb747558c7bc`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 7.1 MB (7127794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007fedfcc03b5b7abd18606ac24e2e3cca135fcdd3f0d70b7aba8348a88baff`  
		Last Modified: Fri, 23 May 2025 17:04:44 GMT  
		Size: 157.1 MB (157135055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c5000478ac61b52cd1d3ac64a845ef1f5dc803edb9b7bbb1c4aed0b9bff722`  
		Last Modified: Fri, 23 May 2025 17:04:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfea4819b2811e369c70b8633fecdc9aa0ebf72abef51249efe4d0f392d12e92`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6ad83ffb10b9c9e2bcfadda7149c1440b5066db63e6eb2d346fb693229daca`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67db376579d9069deafa02f84c6d4316295e74911b16083e17b4826ecac21d`  
		Last Modified: Fri, 23 May 2025 17:04:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc8eee9198db9da70a05bff9f57e1af7273da8867bc4cbb17cc907774c0ea23`  
		Last Modified: Fri, 23 May 2025 17:04:42 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d4ff4620d1db9265b0deeab3213905058f2365fbaacaef01676dd2aa508a4954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b35a4ad0720bdac55cac7b0db6bd7535bbf7543ce437811d782f6d4e2be28c`

```dockerfile
```

-	Layers:
	-	`sha256:375b78d42bcd4520fb8fc1071063fdd1a14c65683c3331fc9607b38b60023d8a`  
		Last Modified: Fri, 23 May 2025 17:04:40 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.1-jammy`

```console
$ docker pull clickhouse@sha256:470114515e8ef26bf10020e6949b04c9dc75722ca0a2c98bb82c027327f13c80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e96b2a65a4972f96046e7095ab89c2f7bf6cde9225bcaba3added5553a3665ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205992665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828b3e01aa7864ededf4583c3695daece684cd54e266ae1e4481f6993467044d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd180e99af6e8a635c124ac88a22ef63cf17cff53e537fdfcd0804fadad61fc6`  
		Last Modified: Fri, 23 May 2025 17:05:04 GMT  
		Size: 7.2 MB (7151944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f7d54a227de8f904f2cbb8bd6a1d5c8f766257835dc829e9762ef6f2ca8dc4`  
		Last Modified: Fri, 23 May 2025 17:05:08 GMT  
		Size: 168.4 MB (168437865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edbd4b6fd576d2b6a81c633486aa0ae4a45560c7e104dd9e03529749d7c6f48`  
		Last Modified: Fri, 23 May 2025 17:05:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e511784a70985fed75bb4766e0bc1dd3e8483c0a01b72c4bd3f2e4ac952c30`  
		Last Modified: Fri, 23 May 2025 17:05:04 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593969705065da1263004c4ee7ca56fe3aeed1fbebcb9b5f0a01a95e5af950db`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65aec7ae4592ef3f7195bf07e65ccb314d703c500dee178399a7674ebb22ac2`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a45b6a11d04db702333075b27c54cfe03908ed78dd458bf38f0658ad425d0bc`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cbd8008a9ef82f0188ec7d793b9795a3b91fadf8afd2028a6d58bdfb18216d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac21aa5774e2acbd638f4e2063aa2ae38353820934905da4edc7d620aa78077`

```dockerfile
```

-	Layers:
	-	`sha256:4e27de348195003815d254c7810735b47071050392ebdce1b4af948733cfee9d`  
		Last Modified: Fri, 23 May 2025 17:05:03 GMT  
		Size: 25.9 KB (25898 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4464c90becdde299168c0f06d1218a90865a4bdbe22be2a4118fa509b5feb96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192487306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc18fcff80fd20c45952f6b567c68429836bf6510ffa7a0aca376eaad4a85b6b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eb6f6d756f55bb7432895aca56cba74e904a26438e38de6fa4fb747558c7bc`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 7.1 MB (7127794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007fedfcc03b5b7abd18606ac24e2e3cca135fcdd3f0d70b7aba8348a88baff`  
		Last Modified: Fri, 23 May 2025 17:04:44 GMT  
		Size: 157.1 MB (157135055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c5000478ac61b52cd1d3ac64a845ef1f5dc803edb9b7bbb1c4aed0b9bff722`  
		Last Modified: Fri, 23 May 2025 17:04:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfea4819b2811e369c70b8633fecdc9aa0ebf72abef51249efe4d0f392d12e92`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6ad83ffb10b9c9e2bcfadda7149c1440b5066db63e6eb2d346fb693229daca`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67db376579d9069deafa02f84c6d4316295e74911b16083e17b4826ecac21d`  
		Last Modified: Fri, 23 May 2025 17:04:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc8eee9198db9da70a05bff9f57e1af7273da8867bc4cbb17cc907774c0ea23`  
		Last Modified: Fri, 23 May 2025 17:04:42 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d4ff4620d1db9265b0deeab3213905058f2365fbaacaef01676dd2aa508a4954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b35a4ad0720bdac55cac7b0db6bd7535bbf7543ce437811d782f6d4e2be28c`

```dockerfile
```

-	Layers:
	-	`sha256:375b78d42bcd4520fb8fc1071063fdd1a14c65683c3331fc9607b38b60023d8a`  
		Last Modified: Fri, 23 May 2025 17:04:40 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.1.2782`

```console
$ docker pull clickhouse@sha256:470114515e8ef26bf10020e6949b04c9dc75722ca0a2c98bb82c027327f13c80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.1.2782` - linux; amd64

```console
$ docker pull clickhouse@sha256:e96b2a65a4972f96046e7095ab89c2f7bf6cde9225bcaba3added5553a3665ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205992665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828b3e01aa7864ededf4583c3695daece684cd54e266ae1e4481f6993467044d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd180e99af6e8a635c124ac88a22ef63cf17cff53e537fdfcd0804fadad61fc6`  
		Last Modified: Fri, 23 May 2025 17:05:04 GMT  
		Size: 7.2 MB (7151944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f7d54a227de8f904f2cbb8bd6a1d5c8f766257835dc829e9762ef6f2ca8dc4`  
		Last Modified: Fri, 23 May 2025 17:05:08 GMT  
		Size: 168.4 MB (168437865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edbd4b6fd576d2b6a81c633486aa0ae4a45560c7e104dd9e03529749d7c6f48`  
		Last Modified: Fri, 23 May 2025 17:05:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e511784a70985fed75bb4766e0bc1dd3e8483c0a01b72c4bd3f2e4ac952c30`  
		Last Modified: Fri, 23 May 2025 17:05:04 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593969705065da1263004c4ee7ca56fe3aeed1fbebcb9b5f0a01a95e5af950db`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65aec7ae4592ef3f7195bf07e65ccb314d703c500dee178399a7674ebb22ac2`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a45b6a11d04db702333075b27c54cfe03908ed78dd458bf38f0658ad425d0bc`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.1.2782` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cbd8008a9ef82f0188ec7d793b9795a3b91fadf8afd2028a6d58bdfb18216d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac21aa5774e2acbd638f4e2063aa2ae38353820934905da4edc7d620aa78077`

```dockerfile
```

-	Layers:
	-	`sha256:4e27de348195003815d254c7810735b47071050392ebdce1b4af948733cfee9d`  
		Last Modified: Fri, 23 May 2025 17:05:03 GMT  
		Size: 25.9 KB (25898 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.1.2782` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4464c90becdde299168c0f06d1218a90865a4bdbe22be2a4118fa509b5feb96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192487306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc18fcff80fd20c45952f6b567c68429836bf6510ffa7a0aca376eaad4a85b6b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eb6f6d756f55bb7432895aca56cba74e904a26438e38de6fa4fb747558c7bc`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 7.1 MB (7127794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007fedfcc03b5b7abd18606ac24e2e3cca135fcdd3f0d70b7aba8348a88baff`  
		Last Modified: Fri, 23 May 2025 17:04:44 GMT  
		Size: 157.1 MB (157135055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c5000478ac61b52cd1d3ac64a845ef1f5dc803edb9b7bbb1c4aed0b9bff722`  
		Last Modified: Fri, 23 May 2025 17:04:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfea4819b2811e369c70b8633fecdc9aa0ebf72abef51249efe4d0f392d12e92`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6ad83ffb10b9c9e2bcfadda7149c1440b5066db63e6eb2d346fb693229daca`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67db376579d9069deafa02f84c6d4316295e74911b16083e17b4826ecac21d`  
		Last Modified: Fri, 23 May 2025 17:04:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc8eee9198db9da70a05bff9f57e1af7273da8867bc4cbb17cc907774c0ea23`  
		Last Modified: Fri, 23 May 2025 17:04:42 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.1.2782` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d4ff4620d1db9265b0deeab3213905058f2365fbaacaef01676dd2aa508a4954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b35a4ad0720bdac55cac7b0db6bd7535bbf7543ce437811d782f6d4e2be28c`

```dockerfile
```

-	Layers:
	-	`sha256:375b78d42bcd4520fb8fc1071063fdd1a14c65683c3331fc9607b38b60023d8a`  
		Last Modified: Fri, 23 May 2025 17:04:40 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.1.2782-jammy`

```console
$ docker pull clickhouse@sha256:470114515e8ef26bf10020e6949b04c9dc75722ca0a2c98bb82c027327f13c80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5.1.2782-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e96b2a65a4972f96046e7095ab89c2f7bf6cde9225bcaba3added5553a3665ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205992665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828b3e01aa7864ededf4583c3695daece684cd54e266ae1e4481f6993467044d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd180e99af6e8a635c124ac88a22ef63cf17cff53e537fdfcd0804fadad61fc6`  
		Last Modified: Fri, 23 May 2025 17:05:04 GMT  
		Size: 7.2 MB (7151944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f7d54a227de8f904f2cbb8bd6a1d5c8f766257835dc829e9762ef6f2ca8dc4`  
		Last Modified: Fri, 23 May 2025 17:05:08 GMT  
		Size: 168.4 MB (168437865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edbd4b6fd576d2b6a81c633486aa0ae4a45560c7e104dd9e03529749d7c6f48`  
		Last Modified: Fri, 23 May 2025 17:05:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e511784a70985fed75bb4766e0bc1dd3e8483c0a01b72c4bd3f2e4ac952c30`  
		Last Modified: Fri, 23 May 2025 17:05:04 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593969705065da1263004c4ee7ca56fe3aeed1fbebcb9b5f0a01a95e5af950db`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65aec7ae4592ef3f7195bf07e65ccb314d703c500dee178399a7674ebb22ac2`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a45b6a11d04db702333075b27c54cfe03908ed78dd458bf38f0658ad425d0bc`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.1.2782-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cbd8008a9ef82f0188ec7d793b9795a3b91fadf8afd2028a6d58bdfb18216d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac21aa5774e2acbd638f4e2063aa2ae38353820934905da4edc7d620aa78077`

```dockerfile
```

-	Layers:
	-	`sha256:4e27de348195003815d254c7810735b47071050392ebdce1b4af948733cfee9d`  
		Last Modified: Fri, 23 May 2025 17:05:03 GMT  
		Size: 25.9 KB (25898 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5.1.2782-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4464c90becdde299168c0f06d1218a90865a4bdbe22be2a4118fa509b5feb96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192487306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc18fcff80fd20c45952f6b567c68429836bf6510ffa7a0aca376eaad4a85b6b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eb6f6d756f55bb7432895aca56cba74e904a26438e38de6fa4fb747558c7bc`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 7.1 MB (7127794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007fedfcc03b5b7abd18606ac24e2e3cca135fcdd3f0d70b7aba8348a88baff`  
		Last Modified: Fri, 23 May 2025 17:04:44 GMT  
		Size: 157.1 MB (157135055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c5000478ac61b52cd1d3ac64a845ef1f5dc803edb9b7bbb1c4aed0b9bff722`  
		Last Modified: Fri, 23 May 2025 17:04:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfea4819b2811e369c70b8633fecdc9aa0ebf72abef51249efe4d0f392d12e92`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6ad83ffb10b9c9e2bcfadda7149c1440b5066db63e6eb2d346fb693229daca`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67db376579d9069deafa02f84c6d4316295e74911b16083e17b4826ecac21d`  
		Last Modified: Fri, 23 May 2025 17:04:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc8eee9198db9da70a05bff9f57e1af7273da8867bc4cbb17cc907774c0ea23`  
		Last Modified: Fri, 23 May 2025 17:04:42 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5.1.2782-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d4ff4620d1db9265b0deeab3213905058f2365fbaacaef01676dd2aa508a4954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b35a4ad0720bdac55cac7b0db6bd7535bbf7543ce437811d782f6d4e2be28c`

```dockerfile
```

-	Layers:
	-	`sha256:375b78d42bcd4520fb8fc1071063fdd1a14c65683c3331fc9607b38b60023d8a`  
		Last Modified: Fri, 23 May 2025 17:04:40 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:470114515e8ef26bf10020e6949b04c9dc75722ca0a2c98bb82c027327f13c80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e96b2a65a4972f96046e7095ab89c2f7bf6cde9225bcaba3added5553a3665ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205992665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828b3e01aa7864ededf4583c3695daece684cd54e266ae1e4481f6993467044d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd180e99af6e8a635c124ac88a22ef63cf17cff53e537fdfcd0804fadad61fc6`  
		Last Modified: Fri, 23 May 2025 17:05:04 GMT  
		Size: 7.2 MB (7151944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f7d54a227de8f904f2cbb8bd6a1d5c8f766257835dc829e9762ef6f2ca8dc4`  
		Last Modified: Fri, 23 May 2025 17:05:08 GMT  
		Size: 168.4 MB (168437865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edbd4b6fd576d2b6a81c633486aa0ae4a45560c7e104dd9e03529749d7c6f48`  
		Last Modified: Fri, 23 May 2025 17:05:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e511784a70985fed75bb4766e0bc1dd3e8483c0a01b72c4bd3f2e4ac952c30`  
		Last Modified: Fri, 23 May 2025 17:05:04 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593969705065da1263004c4ee7ca56fe3aeed1fbebcb9b5f0a01a95e5af950db`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65aec7ae4592ef3f7195bf07e65ccb314d703c500dee178399a7674ebb22ac2`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a45b6a11d04db702333075b27c54cfe03908ed78dd458bf38f0658ad425d0bc`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cbd8008a9ef82f0188ec7d793b9795a3b91fadf8afd2028a6d58bdfb18216d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac21aa5774e2acbd638f4e2063aa2ae38353820934905da4edc7d620aa78077`

```dockerfile
```

-	Layers:
	-	`sha256:4e27de348195003815d254c7810735b47071050392ebdce1b4af948733cfee9d`  
		Last Modified: Fri, 23 May 2025 17:05:03 GMT  
		Size: 25.9 KB (25898 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4464c90becdde299168c0f06d1218a90865a4bdbe22be2a4118fa509b5feb96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192487306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc18fcff80fd20c45952f6b567c68429836bf6510ffa7a0aca376eaad4a85b6b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eb6f6d756f55bb7432895aca56cba74e904a26438e38de6fa4fb747558c7bc`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 7.1 MB (7127794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007fedfcc03b5b7abd18606ac24e2e3cca135fcdd3f0d70b7aba8348a88baff`  
		Last Modified: Fri, 23 May 2025 17:04:44 GMT  
		Size: 157.1 MB (157135055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c5000478ac61b52cd1d3ac64a845ef1f5dc803edb9b7bbb1c4aed0b9bff722`  
		Last Modified: Fri, 23 May 2025 17:04:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfea4819b2811e369c70b8633fecdc9aa0ebf72abef51249efe4d0f392d12e92`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6ad83ffb10b9c9e2bcfadda7149c1440b5066db63e6eb2d346fb693229daca`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67db376579d9069deafa02f84c6d4316295e74911b16083e17b4826ecac21d`  
		Last Modified: Fri, 23 May 2025 17:04:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc8eee9198db9da70a05bff9f57e1af7273da8867bc4cbb17cc907774c0ea23`  
		Last Modified: Fri, 23 May 2025 17:04:42 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d4ff4620d1db9265b0deeab3213905058f2365fbaacaef01676dd2aa508a4954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b35a4ad0720bdac55cac7b0db6bd7535bbf7543ce437811d782f6d4e2be28c`

```dockerfile
```

-	Layers:
	-	`sha256:375b78d42bcd4520fb8fc1071063fdd1a14c65683c3331fc9607b38b60023d8a`  
		Last Modified: Fri, 23 May 2025 17:04:40 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:470114515e8ef26bf10020e6949b04c9dc75722ca0a2c98bb82c027327f13c80
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:e96b2a65a4972f96046e7095ab89c2f7bf6cde9225bcaba3added5553a3665ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205992665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828b3e01aa7864ededf4583c3695daece684cd54e266ae1e4481f6993467044d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd180e99af6e8a635c124ac88a22ef63cf17cff53e537fdfcd0804fadad61fc6`  
		Last Modified: Fri, 23 May 2025 17:05:04 GMT  
		Size: 7.2 MB (7151944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f7d54a227de8f904f2cbb8bd6a1d5c8f766257835dc829e9762ef6f2ca8dc4`  
		Last Modified: Fri, 23 May 2025 17:05:08 GMT  
		Size: 168.4 MB (168437865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2edbd4b6fd576d2b6a81c633486aa0ae4a45560c7e104dd9e03529749d7c6f48`  
		Last Modified: Fri, 23 May 2025 17:05:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e511784a70985fed75bb4766e0bc1dd3e8483c0a01b72c4bd3f2e4ac952c30`  
		Last Modified: Fri, 23 May 2025 17:05:04 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593969705065da1263004c4ee7ca56fe3aeed1fbebcb9b5f0a01a95e5af950db`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65aec7ae4592ef3f7195bf07e65ccb314d703c500dee178399a7674ebb22ac2`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a45b6a11d04db702333075b27c54cfe03908ed78dd458bf38f0658ad425d0bc`  
		Last Modified: Fri, 23 May 2025 17:05:05 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cbd8008a9ef82f0188ec7d793b9795a3b91fadf8afd2028a6d58bdfb18216d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac21aa5774e2acbd638f4e2063aa2ae38353820934905da4edc7d620aa78077`

```dockerfile
```

-	Layers:
	-	`sha256:4e27de348195003815d254c7810735b47071050392ebdce1b4af948733cfee9d`  
		Last Modified: Fri, 23 May 2025 17:05:03 GMT  
		Size: 25.9 KB (25898 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4464c90becdde299168c0f06d1218a90865a4bdbe22be2a4118fa509b5feb96d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192487306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc18fcff80fd20c45952f6b567c68429836bf6510ffa7a0aca376eaad4a85b6b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 23 May 2025 11:00:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 23 May 2025 11:00:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 23 May 2025 11:00:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 23 May 2025 11:00:13 GMT
ARG VERSION=25.5.1.2782
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.5.1.2782 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 23 May 2025 11:00:13 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 23 May 2025 11:00:13 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 23 May 2025 11:00:13 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 23 May 2025 11:00:13 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 23 May 2025 11:00:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3eb6f6d756f55bb7432895aca56cba74e904a26438e38de6fa4fb747558c7bc`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 7.1 MB (7127794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a007fedfcc03b5b7abd18606ac24e2e3cca135fcdd3f0d70b7aba8348a88baff`  
		Last Modified: Fri, 23 May 2025 17:04:44 GMT  
		Size: 157.1 MB (157135055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c5000478ac61b52cd1d3ac64a845ef1f5dc803edb9b7bbb1c4aed0b9bff722`  
		Last Modified: Fri, 23 May 2025 17:04:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfea4819b2811e369c70b8633fecdc9aa0ebf72abef51249efe4d0f392d12e92`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6ad83ffb10b9c9e2bcfadda7149c1440b5066db63e6eb2d346fb693229daca`  
		Last Modified: Fri, 23 May 2025 17:04:41 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa67db376579d9069deafa02f84c6d4316295e74911b16083e17b4826ecac21d`  
		Last Modified: Fri, 23 May 2025 17:04:42 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc8eee9198db9da70a05bff9f57e1af7273da8867bc4cbb17cc907774c0ea23`  
		Last Modified: Fri, 23 May 2025 17:04:42 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d4ff4620d1db9265b0deeab3213905058f2365fbaacaef01676dd2aa508a4954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4b35a4ad0720bdac55cac7b0db6bd7535bbf7543ce437811d782f6d4e2be28c`

```dockerfile
```

-	Layers:
	-	`sha256:375b78d42bcd4520fb8fc1071063fdd1a14c65683c3331fc9607b38b60023d8a`  
		Last Modified: Fri, 23 May 2025 17:04:40 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:6f432bce9f74156e04db2a40fc5f5e59f05aa585194e5548368c6cbf456d63ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:b320679c5ca0b848e8c0e7ed06dbe975d5d4aa084f7e7b89ed7de34fc4b656f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc321325d517a2fc1a63924ffe8d507cb7388279b62cff337348d501785f740`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 10:04:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 02 May 2025 10:04:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ARG REPO_CHANNEL=stable
# Fri, 02 May 2025 10:04:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 02 May 2025 10:04:11 GMT
ARG VERSION=25.3.3.42
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 10:04:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 02 May 2025 10:04:11 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 02 May 2025 10:04:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 02 May 2025 10:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293c18414ddc6b5045bd255b1d3fff2b475d11f7bd01cf6f63c08323588bfeb`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 7.2 MB (7152053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a83e724674ef99b3a02f95d6f99edb74d6da86f3e952d96df426d2e24ffad54`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 167.0 MB (166978959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5788f6ecbfd19db9de8f1ebca0a309877c17b3a68e2b6927db7178a38dd3e2ea`  
		Last Modified: Mon, 05 May 2025 16:34:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c12c8cb54ca9170c10677abfac3c0cd2a66c86322bdbab8b6e6fe92cc0137`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477777a3fe047b2d393a11522c673d966c5106c04a594f53822905dfb3099ed`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357524fb1f1cb1c745bd69563a49c927ad2294938d4f470a351f5f65404ffdc`  
		Last Modified: Mon, 05 May 2025 16:34:59 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89b4acb36be4c123b76a5f2e389268a91bc95467c65d1b794c398fd8fb1631`  
		Last Modified: Mon, 05 May 2025 16:34:59 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0faf7dfca35f7610a11768af5806f14de92c5d3c6878fe530ace15f313771a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56563ead7314ab3dda2382afd2bc4d4d832666426dbd96304c321466b2e7722e`

```dockerfile
```

-	Layers:
	-	`sha256:001a2ba99704453b4192ecf76574a83ce56a72dc98bb29362403dd51dea2e99c`  
		Last Modified: Mon, 05 May 2025 16:34:57 GMT  
		Size: 25.9 KB (25874 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:641cd40cc4e90fff20a5e6a3388a2d862362b1ca4fbfb99227bfa4190b23ea77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192035226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972daccc52695628d0a97703050d19c600e6618b622b76f30d0fc538fab8a0c8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 10:04:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 02 May 2025 10:04:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ARG REPO_CHANNEL=stable
# Fri, 02 May 2025 10:04:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 02 May 2025 10:04:11 GMT
ARG VERSION=25.3.3.42
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 10:04:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 02 May 2025 10:04:11 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 02 May 2025 10:04:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 02 May 2025 10:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be04f390c597833173d77846d1293ad9897baf5e3a03f35936564cf8357f23d0`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 7.1 MB (7127782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63304746e0be595e8c18791c88e140ffcce7ef167770cb0eed5751a00ae24c97`  
		Last Modified: Mon, 05 May 2025 16:38:34 GMT  
		Size: 156.7 MB (156682982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3a65e1ba7a953198688fcc235a4aa5964d0f2579898b986d2df707007fade3`  
		Last Modified: Mon, 05 May 2025 16:38:29 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b201d0974da903e0cdb374d1c08192a2b464ec8048c2a9663a887ed549deb8e`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d384269f2cbb93d090459b306fac19a3f928e07fb6661a56d4a9a5a622d1676b`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b89a2a8dbd8bb92760956b84348fe7e88a495d07ab09fc6ac96aeee9be29109`  
		Last Modified: Mon, 05 May 2025 16:38:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423d17743661f544353b767293e75d841505deef68df1b0f01a77d1ae0189a8a`  
		Last Modified: Mon, 05 May 2025 16:38:31 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ce50101a43b7bc7af719b6306abf2eed03069509ccaeedb29ad994a9f08c395b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66dec5164ea12453fde66e209a44499f7785d422ad48fa1a4cdfec7132f70843`

```dockerfile
```

-	Layers:
	-	`sha256:1710dd56b0182fa3009a6a1f008d8ee7f69b543253b84d6e7738a98b83af284f`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:6f432bce9f74156e04db2a40fc5f5e59f05aa585194e5548368c6cbf456d63ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:b320679c5ca0b848e8c0e7ed06dbe975d5d4aa084f7e7b89ed7de34fc4b656f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc321325d517a2fc1a63924ffe8d507cb7388279b62cff337348d501785f740`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:44:40 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:44:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:44:40 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:44:42 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Mon, 28 Apr 2025 09:44:42 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 10:04:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 02 May 2025 10:04:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ARG REPO_CHANNEL=stable
# Fri, 02 May 2025 10:04:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 02 May 2025 10:04:11 GMT
ARG VERSION=25.3.3.42
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 10:04:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 02 May 2025 10:04:11 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 02 May 2025 10:04:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 02 May 2025 10:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293c18414ddc6b5045bd255b1d3fff2b475d11f7bd01cf6f63c08323588bfeb`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 7.2 MB (7152053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a83e724674ef99b3a02f95d6f99edb74d6da86f3e952d96df426d2e24ffad54`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 167.0 MB (166978959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5788f6ecbfd19db9de8f1ebca0a309877c17b3a68e2b6927db7178a38dd3e2ea`  
		Last Modified: Mon, 05 May 2025 16:34:57 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c12c8cb54ca9170c10677abfac3c0cd2a66c86322bdbab8b6e6fe92cc0137`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477777a3fe047b2d393a11522c673d966c5106c04a594f53822905dfb3099ed`  
		Last Modified: Mon, 05 May 2025 16:34:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357524fb1f1cb1c745bd69563a49c927ad2294938d4f470a351f5f65404ffdc`  
		Last Modified: Mon, 05 May 2025 16:34:59 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89b4acb36be4c123b76a5f2e389268a91bc95467c65d1b794c398fd8fb1631`  
		Last Modified: Mon, 05 May 2025 16:34:59 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0faf7dfca35f7610a11768af5806f14de92c5d3c6878fe530ace15f313771a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56563ead7314ab3dda2382afd2bc4d4d832666426dbd96304c321466b2e7722e`

```dockerfile
```

-	Layers:
	-	`sha256:001a2ba99704453b4192ecf76574a83ce56a72dc98bb29362403dd51dea2e99c`  
		Last Modified: Mon, 05 May 2025 16:34:57 GMT  
		Size: 25.9 KB (25874 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:641cd40cc4e90fff20a5e6a3388a2d862362b1ca4fbfb99227bfa4190b23ea77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192035226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972daccc52695628d0a97703050d19c600e6618b622b76f30d0fc538fab8a0c8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 28 Apr 2025 09:46:27 GMT
ARG RELEASE
# Mon, 28 Apr 2025 09:46:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Apr 2025 09:46:27 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 28 Apr 2025 09:46:30 GMT
ADD file:da80d592df77a4ddbc2c4267be13e1ead72bc1d7f4535f967c511ae736520d7a in / 
# Mon, 28 Apr 2025 09:46:30 GMT
CMD ["/bin/bash"]
# Fri, 02 May 2025 10:04:11 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 02 May 2025 10:04:11 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ARG REPO_CHANNEL=stable
# Fri, 02 May 2025 10:04:11 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 02 May 2025 10:04:11 GMT
ARG VERSION=25.3.3.42
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 02 May 2025 10:04:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 02 May 2025 10:04:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 02 May 2025 10:04:11 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 02 May 2025 10:04:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 02 May 2025 10:04:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:67b06617bd6bbb299a723709813a971289b935f40eaff66a3348adf478cd41f6`  
		Last Modified: Mon, 28 Apr 2025 10:43:51 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be04f390c597833173d77846d1293ad9897baf5e3a03f35936564cf8357f23d0`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 7.1 MB (7127782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63304746e0be595e8c18791c88e140ffcce7ef167770cb0eed5751a00ae24c97`  
		Last Modified: Mon, 05 May 2025 16:38:34 GMT  
		Size: 156.7 MB (156682982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3a65e1ba7a953198688fcc235a4aa5964d0f2579898b986d2df707007fade3`  
		Last Modified: Mon, 05 May 2025 16:38:29 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b201d0974da903e0cdb374d1c08192a2b464ec8048c2a9663a887ed549deb8e`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d384269f2cbb93d090459b306fac19a3f928e07fb6661a56d4a9a5a622d1676b`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b89a2a8dbd8bb92760956b84348fe7e88a495d07ab09fc6ac96aeee9be29109`  
		Last Modified: Mon, 05 May 2025 16:38:31 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423d17743661f544353b767293e75d841505deef68df1b0f01a77d1ae0189a8a`  
		Last Modified: Mon, 05 May 2025 16:38:31 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ce50101a43b7bc7af719b6306abf2eed03069509ccaeedb29ad994a9f08c395b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66dec5164ea12453fde66e209a44499f7785d422ad48fa1a4cdfec7132f70843`

```dockerfile
```

-	Layers:
	-	`sha256:1710dd56b0182fa3009a6a1f008d8ee7f69b543253b84d6e7738a98b83af284f`  
		Last Modified: Mon, 05 May 2025 16:38:30 GMT  
		Size: 26.1 KB (26087 bytes)  
		MIME: application/vnd.in-toto+json
