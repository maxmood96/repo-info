<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:24.8`](#clickhouse248)
-	[`clickhouse:24.8-focal`](#clickhouse248-focal)
-	[`clickhouse:24.8.14`](#clickhouse24814)
-	[`clickhouse:24.8.14-focal`](#clickhouse24814-focal)
-	[`clickhouse:24.8.14.39`](#clickhouse2481439)
-	[`clickhouse:24.8.14.39-focal`](#clickhouse2481439-focal)
-	[`clickhouse:25.2`](#clickhouse252)
-	[`clickhouse:25.2-jammy`](#clickhouse252-jammy)
-	[`clickhouse:25.2.2`](#clickhouse2522)
-	[`clickhouse:25.2.2-jammy`](#clickhouse2522-jammy)
-	[`clickhouse:25.2.2.39`](#clickhouse252239)
-	[`clickhouse:25.2.2.39-jammy`](#clickhouse252239-jammy)
-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.3`](#clickhouse2533)
-	[`clickhouse:25.3.3-jammy`](#clickhouse2533-jammy)
-	[`clickhouse:25.3.3.42`](#clickhouse253342)
-	[`clickhouse:25.3.3.42-jammy`](#clickhouse253342-jammy)
-	[`clickhouse:25.4`](#clickhouse254)
-	[`clickhouse:25.4-jammy`](#clickhouse254-jammy)
-	[`clickhouse:25.4.2`](#clickhouse2542)
-	[`clickhouse:25.4.2-jammy`](#clickhouse2542-jammy)
-	[`clickhouse:25.4.2.31`](#clickhouse254231)
-	[`clickhouse:25.4.2.31-jammy`](#clickhouse254231-jammy)
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e1243e412a6a0201cd184f8fa51a0e71d129b8f4de79db7d193183afec4c6d`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 8.8 MB (8799908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac9af3af17b3193492bcdfd91f391c8c334911aaf3922fa6311319cbe6a33f4`  
		Last Modified: Thu, 08 May 2025 19:21:19 GMT  
		Size: 141.7 MB (141696924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c4bb93ab79bf3904707d3c99cd46e7835928d2a2f90c2ba21b912ce560de83`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36637523a27e51acb137f07a48d0ad9849a41a41c0c60b84c41ab4498429ab56`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382d8e10b9f36a4c5dea337b013c269860abca3be162c5463a80174e6d98eb1f`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcae91c2cf4a08b42245af59422ab5c439de48c7cd6f00c4ada6ee64c324b39`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acffb612a4bc15abbb5b81b9384d4534df6a5e5854abc7d5add9464619084de8`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef4febeaa9a96a464e61f373f7883b7bf2e04bca608d6f01b00d574f182900`  
		Last Modified: Thu, 08 May 2025 18:51:07 GMT  
		Size: 8.7 MB (8658757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a0789ea10e651f70441e6da73550d2821aabb69bc62b7f062631cb21cb3be`  
		Last Modified: Thu, 08 May 2025 18:51:15 GMT  
		Size: 136.8 MB (136750682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798c2b06438cfb8c040af039a5404f2eb18b7e887f0e03c4221bdf23bf423e7`  
		Last Modified: Thu, 08 May 2025 18:51:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f94512f579ab88482ec7b65bbdf5c4be1554b0fc7be38134d2655b6a3a2ba1`  
		Last Modified: Thu, 08 May 2025 18:51:09 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c9df5310d0e344009510a490a161d18ef94d62c24fa9a240d03af5ab2cefb3`  
		Last Modified: Thu, 08 May 2025 18:51:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cec40ddbc5ae51f53198099e6bdff6123006e041994449d5d13aedf54f4377`  
		Last Modified: Thu, 08 May 2025 18:51:10 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7506d9e38ab7aa6336f39aeb3ec50c386a354f0cfd2d921f65bf9384d597d8e5`  
		Last Modified: Thu, 08 May 2025 18:51:10 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e1243e412a6a0201cd184f8fa51a0e71d129b8f4de79db7d193183afec4c6d`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 8.8 MB (8799908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac9af3af17b3193492bcdfd91f391c8c334911aaf3922fa6311319cbe6a33f4`  
		Last Modified: Thu, 08 May 2025 19:21:19 GMT  
		Size: 141.7 MB (141696924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c4bb93ab79bf3904707d3c99cd46e7835928d2a2f90c2ba21b912ce560de83`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36637523a27e51acb137f07a48d0ad9849a41a41c0c60b84c41ab4498429ab56`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382d8e10b9f36a4c5dea337b013c269860abca3be162c5463a80174e6d98eb1f`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcae91c2cf4a08b42245af59422ab5c439de48c7cd6f00c4ada6ee64c324b39`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acffb612a4bc15abbb5b81b9384d4534df6a5e5854abc7d5add9464619084de8`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef4febeaa9a96a464e61f373f7883b7bf2e04bca608d6f01b00d574f182900`  
		Last Modified: Thu, 08 May 2025 18:51:07 GMT  
		Size: 8.7 MB (8658757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a0789ea10e651f70441e6da73550d2821aabb69bc62b7f062631cb21cb3be`  
		Last Modified: Thu, 08 May 2025 18:51:15 GMT  
		Size: 136.8 MB (136750682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798c2b06438cfb8c040af039a5404f2eb18b7e887f0e03c4221bdf23bf423e7`  
		Last Modified: Thu, 08 May 2025 18:51:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f94512f579ab88482ec7b65bbdf5c4be1554b0fc7be38134d2655b6a3a2ba1`  
		Last Modified: Thu, 08 May 2025 18:51:09 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c9df5310d0e344009510a490a161d18ef94d62c24fa9a240d03af5ab2cefb3`  
		Last Modified: Thu, 08 May 2025 18:51:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cec40ddbc5ae51f53198099e6bdff6123006e041994449d5d13aedf54f4377`  
		Last Modified: Thu, 08 May 2025 18:51:10 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7506d9e38ab7aa6336f39aeb3ec50c386a354f0cfd2d921f65bf9384d597d8e5`  
		Last Modified: Thu, 08 May 2025 18:51:10 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e1243e412a6a0201cd184f8fa51a0e71d129b8f4de79db7d193183afec4c6d`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 8.8 MB (8799908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac9af3af17b3193492bcdfd91f391c8c334911aaf3922fa6311319cbe6a33f4`  
		Last Modified: Thu, 08 May 2025 19:21:19 GMT  
		Size: 141.7 MB (141696924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c4bb93ab79bf3904707d3c99cd46e7835928d2a2f90c2ba21b912ce560de83`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36637523a27e51acb137f07a48d0ad9849a41a41c0c60b84c41ab4498429ab56`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382d8e10b9f36a4c5dea337b013c269860abca3be162c5463a80174e6d98eb1f`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcae91c2cf4a08b42245af59422ab5c439de48c7cd6f00c4ada6ee64c324b39`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acffb612a4bc15abbb5b81b9384d4534df6a5e5854abc7d5add9464619084de8`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef4febeaa9a96a464e61f373f7883b7bf2e04bca608d6f01b00d574f182900`  
		Last Modified: Thu, 08 May 2025 18:51:07 GMT  
		Size: 8.7 MB (8658757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a0789ea10e651f70441e6da73550d2821aabb69bc62b7f062631cb21cb3be`  
		Last Modified: Thu, 08 May 2025 18:51:15 GMT  
		Size: 136.8 MB (136750682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798c2b06438cfb8c040af039a5404f2eb18b7e887f0e03c4221bdf23bf423e7`  
		Last Modified: Thu, 08 May 2025 18:51:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f94512f579ab88482ec7b65bbdf5c4be1554b0fc7be38134d2655b6a3a2ba1`  
		Last Modified: Thu, 08 May 2025 18:51:09 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c9df5310d0e344009510a490a161d18ef94d62c24fa9a240d03af5ab2cefb3`  
		Last Modified: Thu, 08 May 2025 18:51:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cec40ddbc5ae51f53198099e6bdff6123006e041994449d5d13aedf54f4377`  
		Last Modified: Thu, 08 May 2025 18:51:10 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7506d9e38ab7aa6336f39aeb3ec50c386a354f0cfd2d921f65bf9384d597d8e5`  
		Last Modified: Thu, 08 May 2025 18:51:10 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e1243e412a6a0201cd184f8fa51a0e71d129b8f4de79db7d193183afec4c6d`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 8.8 MB (8799908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac9af3af17b3193492bcdfd91f391c8c334911aaf3922fa6311319cbe6a33f4`  
		Last Modified: Thu, 08 May 2025 19:21:19 GMT  
		Size: 141.7 MB (141696924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c4bb93ab79bf3904707d3c99cd46e7835928d2a2f90c2ba21b912ce560de83`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36637523a27e51acb137f07a48d0ad9849a41a41c0c60b84c41ab4498429ab56`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382d8e10b9f36a4c5dea337b013c269860abca3be162c5463a80174e6d98eb1f`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcae91c2cf4a08b42245af59422ab5c439de48c7cd6f00c4ada6ee64c324b39`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acffb612a4bc15abbb5b81b9384d4534df6a5e5854abc7d5add9464619084de8`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef4febeaa9a96a464e61f373f7883b7bf2e04bca608d6f01b00d574f182900`  
		Last Modified: Thu, 08 May 2025 18:51:07 GMT  
		Size: 8.7 MB (8658757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a0789ea10e651f70441e6da73550d2821aabb69bc62b7f062631cb21cb3be`  
		Last Modified: Thu, 08 May 2025 18:51:15 GMT  
		Size: 136.8 MB (136750682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798c2b06438cfb8c040af039a5404f2eb18b7e887f0e03c4221bdf23bf423e7`  
		Last Modified: Thu, 08 May 2025 18:51:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f94512f579ab88482ec7b65bbdf5c4be1554b0fc7be38134d2655b6a3a2ba1`  
		Last Modified: Thu, 08 May 2025 18:51:09 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c9df5310d0e344009510a490a161d18ef94d62c24fa9a240d03af5ab2cefb3`  
		Last Modified: Thu, 08 May 2025 18:51:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cec40ddbc5ae51f53198099e6bdff6123006e041994449d5d13aedf54f4377`  
		Last Modified: Thu, 08 May 2025 18:51:10 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7506d9e38ab7aa6336f39aeb3ec50c386a354f0cfd2d921f65bf9384d597d8e5`  
		Last Modified: Thu, 08 May 2025 18:51:10 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e1243e412a6a0201cd184f8fa51a0e71d129b8f4de79db7d193183afec4c6d`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 8.8 MB (8799908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac9af3af17b3193492bcdfd91f391c8c334911aaf3922fa6311319cbe6a33f4`  
		Last Modified: Thu, 08 May 2025 19:21:19 GMT  
		Size: 141.7 MB (141696924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c4bb93ab79bf3904707d3c99cd46e7835928d2a2f90c2ba21b912ce560de83`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36637523a27e51acb137f07a48d0ad9849a41a41c0c60b84c41ab4498429ab56`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382d8e10b9f36a4c5dea337b013c269860abca3be162c5463a80174e6d98eb1f`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcae91c2cf4a08b42245af59422ab5c439de48c7cd6f00c4ada6ee64c324b39`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acffb612a4bc15abbb5b81b9384d4534df6a5e5854abc7d5add9464619084de8`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef4febeaa9a96a464e61f373f7883b7bf2e04bca608d6f01b00d574f182900`  
		Last Modified: Thu, 08 May 2025 18:51:07 GMT  
		Size: 8.7 MB (8658757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a0789ea10e651f70441e6da73550d2821aabb69bc62b7f062631cb21cb3be`  
		Last Modified: Thu, 08 May 2025 18:51:15 GMT  
		Size: 136.8 MB (136750682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798c2b06438cfb8c040af039a5404f2eb18b7e887f0e03c4221bdf23bf423e7`  
		Last Modified: Thu, 08 May 2025 18:51:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f94512f579ab88482ec7b65bbdf5c4be1554b0fc7be38134d2655b6a3a2ba1`  
		Last Modified: Thu, 08 May 2025 18:51:09 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c9df5310d0e344009510a490a161d18ef94d62c24fa9a240d03af5ab2cefb3`  
		Last Modified: Thu, 08 May 2025 18:51:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cec40ddbc5ae51f53198099e6bdff6123006e041994449d5d13aedf54f4377`  
		Last Modified: Thu, 08 May 2025 18:51:10 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7506d9e38ab7aa6336f39aeb3ec50c386a354f0cfd2d921f65bf9384d597d8e5`  
		Last Modified: Thu, 08 May 2025 18:51:10 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 27.5 MB (27510394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e1243e412a6a0201cd184f8fa51a0e71d129b8f4de79db7d193183afec4c6d`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 8.8 MB (8799908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac9af3af17b3193492bcdfd91f391c8c334911aaf3922fa6311319cbe6a33f4`  
		Last Modified: Thu, 08 May 2025 19:21:19 GMT  
		Size: 141.7 MB (141696924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c4bb93ab79bf3904707d3c99cd46e7835928d2a2f90c2ba21b912ce560de83`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36637523a27e51acb137f07a48d0ad9849a41a41c0c60b84c41ab4498429ab56`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
		Size: 863.5 KB (863471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382d8e10b9f36a4c5dea337b013c269860abca3be162c5463a80174e6d98eb1f`  
		Last Modified: Thu, 08 May 2025 19:21:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcae91c2cf4a08b42245af59422ab5c439de48c7cd6f00c4ada6ee64c324b39`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acffb612a4bc15abbb5b81b9384d4534df6a5e5854abc7d5add9464619084de8`  
		Last Modified: Thu, 08 May 2025 19:21:09 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:17 GMT  
		Size: 26.0 MB (25977661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ef4febeaa9a96a464e61f373f7883b7bf2e04bca608d6f01b00d574f182900`  
		Last Modified: Thu, 08 May 2025 18:51:07 GMT  
		Size: 8.7 MB (8658757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97a0789ea10e651f70441e6da73550d2821aabb69bc62b7f062631cb21cb3be`  
		Last Modified: Thu, 08 May 2025 18:51:15 GMT  
		Size: 136.8 MB (136750682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5798c2b06438cfb8c040af039a5404f2eb18b7e887f0e03c4221bdf23bf423e7`  
		Last Modified: Thu, 08 May 2025 18:51:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55f94512f579ab88482ec7b65bbdf5c4be1554b0fc7be38134d2655b6a3a2ba1`  
		Last Modified: Thu, 08 May 2025 18:51:09 GMT  
		Size: 863.5 KB (863474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c9df5310d0e344009510a490a161d18ef94d62c24fa9a240d03af5ab2cefb3`  
		Last Modified: Thu, 08 May 2025 18:51:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66cec40ddbc5ae51f53198099e6bdff6123006e041994449d5d13aedf54f4377`  
		Last Modified: Thu, 08 May 2025 18:51:10 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7506d9e38ab7aa6336f39aeb3ec50c386a354f0cfd2d921f65bf9384d597d8e5`  
		Last Modified: Thu, 08 May 2025 18:51:10 GMT  
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

## `clickhouse:25.2`

```console
$ docker pull clickhouse@sha256:209c65d8ac571b60b4df855dbc33fa4583bcf9166c0cb1e773b0202d551259b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:1c7ab5c2821448b1c7bdac0ba0390129b0d08376b1f41d67b717f34ad9f7e8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201038524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bda720cd19d45045e610e97a0ce285dd2ddbba7d1d69670eb48feca5678a17e`
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
ARG VERSION=25.2.2.39
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd29a11d43f1555155db0fce404f902ef3bad2831afe42aa365462b9ea3f94a`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 7.2 MB (7152003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4f2347b92dc8855cabe20ae8f923750c4914f4fc185d126ebd0b45c74c5afa`  
		Last Modified: Mon, 05 May 2025 16:35:02 GMT  
		Size: 163.5 MB (163483662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa229fde3037391d2d9e1f41491f0edd3d4c5262362fe238ea9677ce2bb5e7d0`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefad61b8d2561ad05d1e0b079e324f79ca22962be96444167b4c5a2a3a8fa84`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d95aad3cbaaee058c992daaf50b97c33a24a2443e022178411ef8469f8bce0`  
		Last Modified: Mon, 05 May 2025 16:35:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fcba0c76695edd14120741b09f20c0385e081139123c8b70a3142536193f5c`  
		Last Modified: Mon, 05 May 2025 16:35:01 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0971434600ddab52556bd5215d5c0750b752484c697aa49d3102c977013ea5`  
		Last Modified: Mon, 05 May 2025 16:35:02 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:df741c5c9aa08bd7e53f775158ec15744d11a43218170c6ba3365364db977cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c8df4915af87cdd7568f13acbde297229ee84f0b61c0ab9bb425315b2934`

```dockerfile
```

-	Layers:
	-	`sha256:301a69e9419993e05a5b8677d653b71783a36a18d69728e762aa713b09a93185`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:fb5ba72392c48faac8a9844c388b09b120a3aac704c3615cf8ddb663b62f5898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190277258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66a03c51b78c28524f7d71961d877fad78076dab0c5ba8f8ee0e2fc35bf95a8`
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
ARG VERSION=25.2.2.39
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e72c3d041ecec5ce7624b380a7061a9e4c49443a3e1638c2542365cc33fb51`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 7.1 MB (7127802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a725e77cd8d9412d5286cdf144011c253d69423682dffb760b57695a3f3048`  
		Last Modified: Mon, 05 May 2025 16:39:43 GMT  
		Size: 154.9 MB (154924997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf04f5446b1f8d607492258603292031f12665d4fe9d4e56c8c10dcf1fad667`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bca871663cf835b83ee63db02bd9539b4922efccccee36dc978dab8199541e`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3bd4975d985ffe89ab410dda6a3c4437c38dcb610f5cc9d6edab708a28fde8`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0296d4c10038c81ec4bd76d9f4085848e4bb2eddf9c6c74c111b938192bf2fc0`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87e34f9bdffa66b18177d5af3f5588b7d8abd2e4af6e9c0559451bdb2fe31b1`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a8ed966c683644a26afc88eace546226edc32fe60e556fb3f005eeaf920ea73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1ff77f32f04e4a40ca7dac5de05eea0da742beae4ce19ad11c4786090bee49`

```dockerfile
```

-	Layers:
	-	`sha256:327c7894a76594f66b510054cb1756bdaa0bfee2ebf37f941f98c46d88a8ecbc`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.2-jammy`

```console
$ docker pull clickhouse@sha256:209c65d8ac571b60b4df855dbc33fa4583bcf9166c0cb1e773b0202d551259b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1c7ab5c2821448b1c7bdac0ba0390129b0d08376b1f41d67b717f34ad9f7e8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201038524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bda720cd19d45045e610e97a0ce285dd2ddbba7d1d69670eb48feca5678a17e`
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
ARG VERSION=25.2.2.39
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd29a11d43f1555155db0fce404f902ef3bad2831afe42aa365462b9ea3f94a`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 7.2 MB (7152003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4f2347b92dc8855cabe20ae8f923750c4914f4fc185d126ebd0b45c74c5afa`  
		Last Modified: Mon, 05 May 2025 16:35:02 GMT  
		Size: 163.5 MB (163483662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa229fde3037391d2d9e1f41491f0edd3d4c5262362fe238ea9677ce2bb5e7d0`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefad61b8d2561ad05d1e0b079e324f79ca22962be96444167b4c5a2a3a8fa84`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d95aad3cbaaee058c992daaf50b97c33a24a2443e022178411ef8469f8bce0`  
		Last Modified: Mon, 05 May 2025 16:35:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fcba0c76695edd14120741b09f20c0385e081139123c8b70a3142536193f5c`  
		Last Modified: Mon, 05 May 2025 16:35:01 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0971434600ddab52556bd5215d5c0750b752484c697aa49d3102c977013ea5`  
		Last Modified: Mon, 05 May 2025 16:35:02 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:df741c5c9aa08bd7e53f775158ec15744d11a43218170c6ba3365364db977cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c8df4915af87cdd7568f13acbde297229ee84f0b61c0ab9bb425315b2934`

```dockerfile
```

-	Layers:
	-	`sha256:301a69e9419993e05a5b8677d653b71783a36a18d69728e762aa713b09a93185`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:fb5ba72392c48faac8a9844c388b09b120a3aac704c3615cf8ddb663b62f5898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190277258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66a03c51b78c28524f7d71961d877fad78076dab0c5ba8f8ee0e2fc35bf95a8`
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
ARG VERSION=25.2.2.39
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e72c3d041ecec5ce7624b380a7061a9e4c49443a3e1638c2542365cc33fb51`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 7.1 MB (7127802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a725e77cd8d9412d5286cdf144011c253d69423682dffb760b57695a3f3048`  
		Last Modified: Mon, 05 May 2025 16:39:43 GMT  
		Size: 154.9 MB (154924997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf04f5446b1f8d607492258603292031f12665d4fe9d4e56c8c10dcf1fad667`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bca871663cf835b83ee63db02bd9539b4922efccccee36dc978dab8199541e`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3bd4975d985ffe89ab410dda6a3c4437c38dcb610f5cc9d6edab708a28fde8`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0296d4c10038c81ec4bd76d9f4085848e4bb2eddf9c6c74c111b938192bf2fc0`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87e34f9bdffa66b18177d5af3f5588b7d8abd2e4af6e9c0559451bdb2fe31b1`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a8ed966c683644a26afc88eace546226edc32fe60e556fb3f005eeaf920ea73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1ff77f32f04e4a40ca7dac5de05eea0da742beae4ce19ad11c4786090bee49`

```dockerfile
```

-	Layers:
	-	`sha256:327c7894a76594f66b510054cb1756bdaa0bfee2ebf37f941f98c46d88a8ecbc`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.2.2`

```console
$ docker pull clickhouse@sha256:209c65d8ac571b60b4df855dbc33fa4583bcf9166c0cb1e773b0202d551259b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:1c7ab5c2821448b1c7bdac0ba0390129b0d08376b1f41d67b717f34ad9f7e8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201038524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bda720cd19d45045e610e97a0ce285dd2ddbba7d1d69670eb48feca5678a17e`
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
ARG VERSION=25.2.2.39
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd29a11d43f1555155db0fce404f902ef3bad2831afe42aa365462b9ea3f94a`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 7.2 MB (7152003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4f2347b92dc8855cabe20ae8f923750c4914f4fc185d126ebd0b45c74c5afa`  
		Last Modified: Mon, 05 May 2025 16:35:02 GMT  
		Size: 163.5 MB (163483662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa229fde3037391d2d9e1f41491f0edd3d4c5262362fe238ea9677ce2bb5e7d0`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefad61b8d2561ad05d1e0b079e324f79ca22962be96444167b4c5a2a3a8fa84`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d95aad3cbaaee058c992daaf50b97c33a24a2443e022178411ef8469f8bce0`  
		Last Modified: Mon, 05 May 2025 16:35:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fcba0c76695edd14120741b09f20c0385e081139123c8b70a3142536193f5c`  
		Last Modified: Mon, 05 May 2025 16:35:01 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0971434600ddab52556bd5215d5c0750b752484c697aa49d3102c977013ea5`  
		Last Modified: Mon, 05 May 2025 16:35:02 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:df741c5c9aa08bd7e53f775158ec15744d11a43218170c6ba3365364db977cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c8df4915af87cdd7568f13acbde297229ee84f0b61c0ab9bb425315b2934`

```dockerfile
```

-	Layers:
	-	`sha256:301a69e9419993e05a5b8677d653b71783a36a18d69728e762aa713b09a93185`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:fb5ba72392c48faac8a9844c388b09b120a3aac704c3615cf8ddb663b62f5898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190277258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66a03c51b78c28524f7d71961d877fad78076dab0c5ba8f8ee0e2fc35bf95a8`
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
ARG VERSION=25.2.2.39
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e72c3d041ecec5ce7624b380a7061a9e4c49443a3e1638c2542365cc33fb51`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 7.1 MB (7127802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a725e77cd8d9412d5286cdf144011c253d69423682dffb760b57695a3f3048`  
		Last Modified: Mon, 05 May 2025 16:39:43 GMT  
		Size: 154.9 MB (154924997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf04f5446b1f8d607492258603292031f12665d4fe9d4e56c8c10dcf1fad667`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bca871663cf835b83ee63db02bd9539b4922efccccee36dc978dab8199541e`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3bd4975d985ffe89ab410dda6a3c4437c38dcb610f5cc9d6edab708a28fde8`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0296d4c10038c81ec4bd76d9f4085848e4bb2eddf9c6c74c111b938192bf2fc0`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87e34f9bdffa66b18177d5af3f5588b7d8abd2e4af6e9c0559451bdb2fe31b1`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a8ed966c683644a26afc88eace546226edc32fe60e556fb3f005eeaf920ea73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1ff77f32f04e4a40ca7dac5de05eea0da742beae4ce19ad11c4786090bee49`

```dockerfile
```

-	Layers:
	-	`sha256:327c7894a76594f66b510054cb1756bdaa0bfee2ebf37f941f98c46d88a8ecbc`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.2.2-jammy`

```console
$ docker pull clickhouse@sha256:209c65d8ac571b60b4df855dbc33fa4583bcf9166c0cb1e773b0202d551259b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1c7ab5c2821448b1c7bdac0ba0390129b0d08376b1f41d67b717f34ad9f7e8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201038524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bda720cd19d45045e610e97a0ce285dd2ddbba7d1d69670eb48feca5678a17e`
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
ARG VERSION=25.2.2.39
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd29a11d43f1555155db0fce404f902ef3bad2831afe42aa365462b9ea3f94a`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 7.2 MB (7152003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4f2347b92dc8855cabe20ae8f923750c4914f4fc185d126ebd0b45c74c5afa`  
		Last Modified: Mon, 05 May 2025 16:35:02 GMT  
		Size: 163.5 MB (163483662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa229fde3037391d2d9e1f41491f0edd3d4c5262362fe238ea9677ce2bb5e7d0`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefad61b8d2561ad05d1e0b079e324f79ca22962be96444167b4c5a2a3a8fa84`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d95aad3cbaaee058c992daaf50b97c33a24a2443e022178411ef8469f8bce0`  
		Last Modified: Mon, 05 May 2025 16:35:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fcba0c76695edd14120741b09f20c0385e081139123c8b70a3142536193f5c`  
		Last Modified: Mon, 05 May 2025 16:35:01 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0971434600ddab52556bd5215d5c0750b752484c697aa49d3102c977013ea5`  
		Last Modified: Mon, 05 May 2025 16:35:02 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:df741c5c9aa08bd7e53f775158ec15744d11a43218170c6ba3365364db977cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c8df4915af87cdd7568f13acbde297229ee84f0b61c0ab9bb425315b2934`

```dockerfile
```

-	Layers:
	-	`sha256:301a69e9419993e05a5b8677d653b71783a36a18d69728e762aa713b09a93185`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:fb5ba72392c48faac8a9844c388b09b120a3aac704c3615cf8ddb663b62f5898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190277258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66a03c51b78c28524f7d71961d877fad78076dab0c5ba8f8ee0e2fc35bf95a8`
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
ARG VERSION=25.2.2.39
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e72c3d041ecec5ce7624b380a7061a9e4c49443a3e1638c2542365cc33fb51`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 7.1 MB (7127802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a725e77cd8d9412d5286cdf144011c253d69423682dffb760b57695a3f3048`  
		Last Modified: Mon, 05 May 2025 16:39:43 GMT  
		Size: 154.9 MB (154924997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf04f5446b1f8d607492258603292031f12665d4fe9d4e56c8c10dcf1fad667`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bca871663cf835b83ee63db02bd9539b4922efccccee36dc978dab8199541e`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3bd4975d985ffe89ab410dda6a3c4437c38dcb610f5cc9d6edab708a28fde8`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0296d4c10038c81ec4bd76d9f4085848e4bb2eddf9c6c74c111b938192bf2fc0`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87e34f9bdffa66b18177d5af3f5588b7d8abd2e4af6e9c0559451bdb2fe31b1`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a8ed966c683644a26afc88eace546226edc32fe60e556fb3f005eeaf920ea73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1ff77f32f04e4a40ca7dac5de05eea0da742beae4ce19ad11c4786090bee49`

```dockerfile
```

-	Layers:
	-	`sha256:327c7894a76594f66b510054cb1756bdaa0bfee2ebf37f941f98c46d88a8ecbc`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.2.2.39`

```console
$ docker pull clickhouse@sha256:209c65d8ac571b60b4df855dbc33fa4583bcf9166c0cb1e773b0202d551259b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2.2.39` - linux; amd64

```console
$ docker pull clickhouse@sha256:1c7ab5c2821448b1c7bdac0ba0390129b0d08376b1f41d67b717f34ad9f7e8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201038524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bda720cd19d45045e610e97a0ce285dd2ddbba7d1d69670eb48feca5678a17e`
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
ARG VERSION=25.2.2.39
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd29a11d43f1555155db0fce404f902ef3bad2831afe42aa365462b9ea3f94a`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 7.2 MB (7152003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4f2347b92dc8855cabe20ae8f923750c4914f4fc185d126ebd0b45c74c5afa`  
		Last Modified: Mon, 05 May 2025 16:35:02 GMT  
		Size: 163.5 MB (163483662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa229fde3037391d2d9e1f41491f0edd3d4c5262362fe238ea9677ce2bb5e7d0`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefad61b8d2561ad05d1e0b079e324f79ca22962be96444167b4c5a2a3a8fa84`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d95aad3cbaaee058c992daaf50b97c33a24a2443e022178411ef8469f8bce0`  
		Last Modified: Mon, 05 May 2025 16:35:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fcba0c76695edd14120741b09f20c0385e081139123c8b70a3142536193f5c`  
		Last Modified: Mon, 05 May 2025 16:35:01 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0971434600ddab52556bd5215d5c0750b752484c697aa49d3102c977013ea5`  
		Last Modified: Mon, 05 May 2025 16:35:02 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2.39` - unknown; unknown

```console
$ docker pull clickhouse@sha256:df741c5c9aa08bd7e53f775158ec15744d11a43218170c6ba3365364db977cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c8df4915af87cdd7568f13acbde297229ee84f0b61c0ab9bb425315b2934`

```dockerfile
```

-	Layers:
	-	`sha256:301a69e9419993e05a5b8677d653b71783a36a18d69728e762aa713b09a93185`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2.2.39` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:fb5ba72392c48faac8a9844c388b09b120a3aac704c3615cf8ddb663b62f5898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190277258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66a03c51b78c28524f7d71961d877fad78076dab0c5ba8f8ee0e2fc35bf95a8`
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
ARG VERSION=25.2.2.39
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e72c3d041ecec5ce7624b380a7061a9e4c49443a3e1638c2542365cc33fb51`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 7.1 MB (7127802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a725e77cd8d9412d5286cdf144011c253d69423682dffb760b57695a3f3048`  
		Last Modified: Mon, 05 May 2025 16:39:43 GMT  
		Size: 154.9 MB (154924997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf04f5446b1f8d607492258603292031f12665d4fe9d4e56c8c10dcf1fad667`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bca871663cf835b83ee63db02bd9539b4922efccccee36dc978dab8199541e`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3bd4975d985ffe89ab410dda6a3c4437c38dcb610f5cc9d6edab708a28fde8`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0296d4c10038c81ec4bd76d9f4085848e4bb2eddf9c6c74c111b938192bf2fc0`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87e34f9bdffa66b18177d5af3f5588b7d8abd2e4af6e9c0559451bdb2fe31b1`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2.39` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a8ed966c683644a26afc88eace546226edc32fe60e556fb3f005eeaf920ea73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1ff77f32f04e4a40ca7dac5de05eea0da742beae4ce19ad11c4786090bee49`

```dockerfile
```

-	Layers:
	-	`sha256:327c7894a76594f66b510054cb1756bdaa0bfee2ebf37f941f98c46d88a8ecbc`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.2.2.39-jammy`

```console
$ docker pull clickhouse@sha256:209c65d8ac571b60b4df855dbc33fa4583bcf9166c0cb1e773b0202d551259b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2.2.39-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1c7ab5c2821448b1c7bdac0ba0390129b0d08376b1f41d67b717f34ad9f7e8a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201038524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bda720cd19d45045e610e97a0ce285dd2ddbba7d1d69670eb48feca5678a17e`
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
ARG VERSION=25.2.2.39
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd29a11d43f1555155db0fce404f902ef3bad2831afe42aa365462b9ea3f94a`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 7.2 MB (7152003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4f2347b92dc8855cabe20ae8f923750c4914f4fc185d126ebd0b45c74c5afa`  
		Last Modified: Mon, 05 May 2025 16:35:02 GMT  
		Size: 163.5 MB (163483662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa229fde3037391d2d9e1f41491f0edd3d4c5262362fe238ea9677ce2bb5e7d0`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eefad61b8d2561ad05d1e0b079e324f79ca22962be96444167b4c5a2a3a8fa84`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d95aad3cbaaee058c992daaf50b97c33a24a2443e022178411ef8469f8bce0`  
		Last Modified: Mon, 05 May 2025 16:35:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39fcba0c76695edd14120741b09f20c0385e081139123c8b70a3142536193f5c`  
		Last Modified: Mon, 05 May 2025 16:35:01 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0971434600ddab52556bd5215d5c0750b752484c697aa49d3102c977013ea5`  
		Last Modified: Mon, 05 May 2025 16:35:02 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2.39-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:df741c5c9aa08bd7e53f775158ec15744d11a43218170c6ba3365364db977cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea28c8df4915af87cdd7568f13acbde297229ee84f0b61c0ab9bb425315b2934`

```dockerfile
```

-	Layers:
	-	`sha256:301a69e9419993e05a5b8677d653b71783a36a18d69728e762aa713b09a93185`  
		Last Modified: Mon, 05 May 2025 16:35:00 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2.2.39-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:fb5ba72392c48faac8a9844c388b09b120a3aac704c3615cf8ddb663b62f5898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190277258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66a03c51b78c28524f7d71961d877fad78076dab0c5ba8f8ee0e2fc35bf95a8`
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
ARG VERSION=25.2.2.39
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e72c3d041ecec5ce7624b380a7061a9e4c49443a3e1638c2542365cc33fb51`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 7.1 MB (7127802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a725e77cd8d9412d5286cdf144011c253d69423682dffb760b57695a3f3048`  
		Last Modified: Mon, 05 May 2025 16:39:43 GMT  
		Size: 154.9 MB (154924997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcf04f5446b1f8d607492258603292031f12665d4fe9d4e56c8c10dcf1fad667`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8bca871663cf835b83ee63db02bd9539b4922efccccee36dc978dab8199541e`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a3bd4975d985ffe89ab410dda6a3c4437c38dcb610f5cc9d6edab708a28fde8`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0296d4c10038c81ec4bd76d9f4085848e4bb2eddf9c6c74c111b938192bf2fc0`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87e34f9bdffa66b18177d5af3f5588b7d8abd2e4af6e9c0559451bdb2fe31b1`  
		Last Modified: Mon, 05 May 2025 16:39:40 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2.39-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9a8ed966c683644a26afc88eace546226edc32fe60e556fb3f005eeaf920ea73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc1ff77f32f04e4a40ca7dac5de05eea0da742beae4ce19ad11c4786090bee49`

```dockerfile
```

-	Layers:
	-	`sha256:327c7894a76594f66b510054cb1756bdaa0bfee2ebf37f941f98c46d88a8ecbc`  
		Last Modified: Mon, 05 May 2025 16:39:39 GMT  
		Size: 25.5 KB (25451 bytes)  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293c18414ddc6b5045bd255b1d3fff2b475d11f7bd01cf6f63c08323588bfeb`  
		Last Modified: Thu, 08 May 2025 17:14:45 GMT  
		Size: 7.2 MB (7152053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a83e724674ef99b3a02f95d6f99edb74d6da86f3e952d96df426d2e24ffad54`  
		Last Modified: Thu, 08 May 2025 17:14:52 GMT  
		Size: 167.0 MB (166978959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5788f6ecbfd19db9de8f1ebca0a309877c17b3a68e2b6927db7178a38dd3e2ea`  
		Last Modified: Thu, 08 May 2025 17:14:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c12c8cb54ca9170c10677abfac3c0cd2a66c86322bdbab8b6e6fe92cc0137`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477777a3fe047b2d393a11522c673d966c5106c04a594f53822905dfb3099ed`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357524fb1f1cb1c745bd69563a49c927ad2294938d4f470a351f5f65404ffdc`  
		Last Modified: Thu, 08 May 2025 17:14:49 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89b4acb36be4c123b76a5f2e389268a91bc95467c65d1b794c398fd8fb1631`  
		Last Modified: Thu, 08 May 2025 17:14:49 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293c18414ddc6b5045bd255b1d3fff2b475d11f7bd01cf6f63c08323588bfeb`  
		Last Modified: Thu, 08 May 2025 17:14:45 GMT  
		Size: 7.2 MB (7152053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a83e724674ef99b3a02f95d6f99edb74d6da86f3e952d96df426d2e24ffad54`  
		Last Modified: Thu, 08 May 2025 17:14:52 GMT  
		Size: 167.0 MB (166978959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5788f6ecbfd19db9de8f1ebca0a309877c17b3a68e2b6927db7178a38dd3e2ea`  
		Last Modified: Thu, 08 May 2025 17:14:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c12c8cb54ca9170c10677abfac3c0cd2a66c86322bdbab8b6e6fe92cc0137`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477777a3fe047b2d393a11522c673d966c5106c04a594f53822905dfb3099ed`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357524fb1f1cb1c745bd69563a49c927ad2294938d4f470a351f5f65404ffdc`  
		Last Modified: Thu, 08 May 2025 17:14:49 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89b4acb36be4c123b76a5f2e389268a91bc95467c65d1b794c398fd8fb1631`  
		Last Modified: Thu, 08 May 2025 17:14:49 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293c18414ddc6b5045bd255b1d3fff2b475d11f7bd01cf6f63c08323588bfeb`  
		Last Modified: Thu, 08 May 2025 17:14:45 GMT  
		Size: 7.2 MB (7152053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a83e724674ef99b3a02f95d6f99edb74d6da86f3e952d96df426d2e24ffad54`  
		Last Modified: Thu, 08 May 2025 17:14:52 GMT  
		Size: 167.0 MB (166978959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5788f6ecbfd19db9de8f1ebca0a309877c17b3a68e2b6927db7178a38dd3e2ea`  
		Last Modified: Thu, 08 May 2025 17:14:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c12c8cb54ca9170c10677abfac3c0cd2a66c86322bdbab8b6e6fe92cc0137`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477777a3fe047b2d393a11522c673d966c5106c04a594f53822905dfb3099ed`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357524fb1f1cb1c745bd69563a49c927ad2294938d4f470a351f5f65404ffdc`  
		Last Modified: Thu, 08 May 2025 17:14:49 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89b4acb36be4c123b76a5f2e389268a91bc95467c65d1b794c398fd8fb1631`  
		Last Modified: Thu, 08 May 2025 17:14:49 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293c18414ddc6b5045bd255b1d3fff2b475d11f7bd01cf6f63c08323588bfeb`  
		Last Modified: Thu, 08 May 2025 17:14:45 GMT  
		Size: 7.2 MB (7152053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a83e724674ef99b3a02f95d6f99edb74d6da86f3e952d96df426d2e24ffad54`  
		Last Modified: Thu, 08 May 2025 17:14:52 GMT  
		Size: 167.0 MB (166978959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5788f6ecbfd19db9de8f1ebca0a309877c17b3a68e2b6927db7178a38dd3e2ea`  
		Last Modified: Thu, 08 May 2025 17:14:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c12c8cb54ca9170c10677abfac3c0cd2a66c86322bdbab8b6e6fe92cc0137`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477777a3fe047b2d393a11522c673d966c5106c04a594f53822905dfb3099ed`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357524fb1f1cb1c745bd69563a49c927ad2294938d4f470a351f5f65404ffdc`  
		Last Modified: Thu, 08 May 2025 17:14:49 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89b4acb36be4c123b76a5f2e389268a91bc95467c65d1b794c398fd8fb1631`  
		Last Modified: Thu, 08 May 2025 17:14:49 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293c18414ddc6b5045bd255b1d3fff2b475d11f7bd01cf6f63c08323588bfeb`  
		Last Modified: Thu, 08 May 2025 17:14:45 GMT  
		Size: 7.2 MB (7152053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a83e724674ef99b3a02f95d6f99edb74d6da86f3e952d96df426d2e24ffad54`  
		Last Modified: Thu, 08 May 2025 17:14:52 GMT  
		Size: 167.0 MB (166978959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5788f6ecbfd19db9de8f1ebca0a309877c17b3a68e2b6927db7178a38dd3e2ea`  
		Last Modified: Thu, 08 May 2025 17:14:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c12c8cb54ca9170c10677abfac3c0cd2a66c86322bdbab8b6e6fe92cc0137`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477777a3fe047b2d393a11522c673d966c5106c04a594f53822905dfb3099ed`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357524fb1f1cb1c745bd69563a49c927ad2294938d4f470a351f5f65404ffdc`  
		Last Modified: Thu, 08 May 2025 17:14:49 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89b4acb36be4c123b76a5f2e389268a91bc95467c65d1b794c398fd8fb1631`  
		Last Modified: Thu, 08 May 2025 17:14:49 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293c18414ddc6b5045bd255b1d3fff2b475d11f7bd01cf6f63c08323588bfeb`  
		Last Modified: Thu, 08 May 2025 17:14:45 GMT  
		Size: 7.2 MB (7152053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a83e724674ef99b3a02f95d6f99edb74d6da86f3e952d96df426d2e24ffad54`  
		Last Modified: Thu, 08 May 2025 17:14:52 GMT  
		Size: 167.0 MB (166978959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5788f6ecbfd19db9de8f1ebca0a309877c17b3a68e2b6927db7178a38dd3e2ea`  
		Last Modified: Thu, 08 May 2025 17:14:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c12c8cb54ca9170c10677abfac3c0cd2a66c86322bdbab8b6e6fe92cc0137`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477777a3fe047b2d393a11522c673d966c5106c04a594f53822905dfb3099ed`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357524fb1f1cb1c745bd69563a49c927ad2294938d4f470a351f5f65404ffdc`  
		Last Modified: Thu, 08 May 2025 17:14:49 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89b4acb36be4c123b76a5f2e389268a91bc95467c65d1b794c398fd8fb1631`  
		Last Modified: Thu, 08 May 2025 17:14:49 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
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
$ docker pull clickhouse@sha256:639f5710b90f9a7f12772d6460b104b8d201b74efd2737346413d6adb5d6777e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:e582fda66d604d0f31d5815bea0c290b1b50a2b08bcb0c47e9120a391483ad30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202682168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc9f9d141c3d53f63fa966cf0403e650e0ea48e897c127cc943fe3567f41882`
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
ARG VERSION=25.4.2.31
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb3f27ffd917411d1b8798c3b7cad886f6862ba256261577893839cc0aa62e1`  
		Last Modified: Thu, 08 May 2025 17:18:50 GMT  
		Size: 7.2 MB (7151953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6cfef0a2e6413ede53483f57f0dcae70228e3aaed0debb966afabf38fd64fa`  
		Last Modified: Thu, 08 May 2025 18:08:01 GMT  
		Size: 165.1 MB (165127358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d7cf7d1bcbbcb13b7450db65bc70dfd19fb5f7590b356df3fab940fbf8cba`  
		Last Modified: Thu, 08 May 2025 17:19:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96de288013cc309eecd9eec102ad88fe7736a6bd14ab1250069113640b5b884`  
		Last Modified: Thu, 08 May 2025 17:19:21 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c67694a6825b4ce284ed8193bd9c3f9658273314b8449e35abb0c1bdcdf3db`  
		Last Modified: Thu, 08 May 2025 17:19:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a05a4b12342b57a21b89d33e6cbd2004cc99635efb1a1527c107c524ce5144f`  
		Last Modified: Thu, 08 May 2025 17:19:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c723b07660005078bbffb13f4edbc39e5ca99559e99b7fa5a7881afda50fafa`  
		Last Modified: Thu, 08 May 2025 17:19:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea6b7a326d5f089edc5616fb30bafc907839c65863fb036265c224ba3cf7e4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4398f32d35bbf9acb5c320c91c257e857d0f67450f6b663d1853c3922b38cc`

```dockerfile
```

-	Layers:
	-	`sha256:996a7ea981380fdb8779cac29b72e46e49ffaeb1c5ec35b1dfee35a443103fd4`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 25.9 KB (25872 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:43af4f67ca2fd47a7a69e270df107d480af42361b4d84b353031a2424d55a33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190013531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa07bd41ac94c406f079bc0f24fa9fd2f5eef9da44b04ad6ed1c22f5e7fa329a`
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
ARG VERSION=25.4.2.31
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bedbc25c514084e050c01a33fdff22e0249a4bdff2c072e38ba6a638dd7e18`  
		Last Modified: Thu, 08 May 2025 18:45:06 GMT  
		Size: 7.1 MB (7127833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a90118e42e4bdad3c7a8532ef133cac468a38065cbb6ef4e93b90ee1a67ca1`  
		Last Modified: Thu, 08 May 2025 18:45:23 GMT  
		Size: 154.7 MB (154661236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c81ecb567fd0321e1c1d04e20db1e12dca63731dcd560060624c7c783a1f46`  
		Last Modified: Thu, 08 May 2025 18:45:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cf4ee70f161e497192b458535b6defb153a22b7240b6ceedac143c46b626df`  
		Last Modified: Thu, 08 May 2025 18:45:08 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bab3c3d33f76349a90ee85942aef784402295347c75d30b1f94d9850a1325c`  
		Last Modified: Thu, 08 May 2025 18:45:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66347907d5b0d3d7ff59cc5ffea5c64dc0628356861b658c038bd592355ea530`  
		Last Modified: Thu, 08 May 2025 18:45:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9324ca125c1023b49ccec61906adf262c5549fe72322f96b788f8de12289e860`  
		Last Modified: Thu, 08 May 2025 18:45:10 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3c116def71e273097ffe59b356846b12dd9d76c01d5637109d14d8b53c360c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf5e5a1959b9e794e278e3f76537696257f2874b767a01c579c3b2328b1678f`

```dockerfile
```

-	Layers:
	-	`sha256:8d92e3637869e89c265b496e794a8804be72074d90bdd494525b9a0b5bbb93d9`  
		Last Modified: Mon, 05 May 2025 16:37:25 GMT  
		Size: 26.1 KB (26085 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4-jammy`

```console
$ docker pull clickhouse@sha256:639f5710b90f9a7f12772d6460b104b8d201b74efd2737346413d6adb5d6777e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e582fda66d604d0f31d5815bea0c290b1b50a2b08bcb0c47e9120a391483ad30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202682168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc9f9d141c3d53f63fa966cf0403e650e0ea48e897c127cc943fe3567f41882`
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
ARG VERSION=25.4.2.31
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb3f27ffd917411d1b8798c3b7cad886f6862ba256261577893839cc0aa62e1`  
		Last Modified: Thu, 08 May 2025 17:18:50 GMT  
		Size: 7.2 MB (7151953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6cfef0a2e6413ede53483f57f0dcae70228e3aaed0debb966afabf38fd64fa`  
		Last Modified: Thu, 08 May 2025 18:08:01 GMT  
		Size: 165.1 MB (165127358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d7cf7d1bcbbcb13b7450db65bc70dfd19fb5f7590b356df3fab940fbf8cba`  
		Last Modified: Thu, 08 May 2025 17:19:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96de288013cc309eecd9eec102ad88fe7736a6bd14ab1250069113640b5b884`  
		Last Modified: Thu, 08 May 2025 17:19:21 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c67694a6825b4ce284ed8193bd9c3f9658273314b8449e35abb0c1bdcdf3db`  
		Last Modified: Thu, 08 May 2025 17:19:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a05a4b12342b57a21b89d33e6cbd2004cc99635efb1a1527c107c524ce5144f`  
		Last Modified: Thu, 08 May 2025 17:19:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c723b07660005078bbffb13f4edbc39e5ca99559e99b7fa5a7881afda50fafa`  
		Last Modified: Thu, 08 May 2025 17:19:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea6b7a326d5f089edc5616fb30bafc907839c65863fb036265c224ba3cf7e4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4398f32d35bbf9acb5c320c91c257e857d0f67450f6b663d1853c3922b38cc`

```dockerfile
```

-	Layers:
	-	`sha256:996a7ea981380fdb8779cac29b72e46e49ffaeb1c5ec35b1dfee35a443103fd4`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 25.9 KB (25872 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:43af4f67ca2fd47a7a69e270df107d480af42361b4d84b353031a2424d55a33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190013531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa07bd41ac94c406f079bc0f24fa9fd2f5eef9da44b04ad6ed1c22f5e7fa329a`
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
ARG VERSION=25.4.2.31
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bedbc25c514084e050c01a33fdff22e0249a4bdff2c072e38ba6a638dd7e18`  
		Last Modified: Thu, 08 May 2025 18:45:06 GMT  
		Size: 7.1 MB (7127833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a90118e42e4bdad3c7a8532ef133cac468a38065cbb6ef4e93b90ee1a67ca1`  
		Last Modified: Thu, 08 May 2025 18:45:23 GMT  
		Size: 154.7 MB (154661236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c81ecb567fd0321e1c1d04e20db1e12dca63731dcd560060624c7c783a1f46`  
		Last Modified: Thu, 08 May 2025 18:45:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cf4ee70f161e497192b458535b6defb153a22b7240b6ceedac143c46b626df`  
		Last Modified: Thu, 08 May 2025 18:45:08 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bab3c3d33f76349a90ee85942aef784402295347c75d30b1f94d9850a1325c`  
		Last Modified: Thu, 08 May 2025 18:45:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66347907d5b0d3d7ff59cc5ffea5c64dc0628356861b658c038bd592355ea530`  
		Last Modified: Thu, 08 May 2025 18:45:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9324ca125c1023b49ccec61906adf262c5549fe72322f96b788f8de12289e860`  
		Last Modified: Thu, 08 May 2025 18:45:10 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3c116def71e273097ffe59b356846b12dd9d76c01d5637109d14d8b53c360c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf5e5a1959b9e794e278e3f76537696257f2874b767a01c579c3b2328b1678f`

```dockerfile
```

-	Layers:
	-	`sha256:8d92e3637869e89c265b496e794a8804be72074d90bdd494525b9a0b5bbb93d9`  
		Last Modified: Mon, 05 May 2025 16:37:25 GMT  
		Size: 26.1 KB (26085 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.2`

```console
$ docker pull clickhouse@sha256:639f5710b90f9a7f12772d6460b104b8d201b74efd2737346413d6adb5d6777e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:e582fda66d604d0f31d5815bea0c290b1b50a2b08bcb0c47e9120a391483ad30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202682168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc9f9d141c3d53f63fa966cf0403e650e0ea48e897c127cc943fe3567f41882`
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
ARG VERSION=25.4.2.31
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb3f27ffd917411d1b8798c3b7cad886f6862ba256261577893839cc0aa62e1`  
		Last Modified: Thu, 08 May 2025 17:18:50 GMT  
		Size: 7.2 MB (7151953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6cfef0a2e6413ede53483f57f0dcae70228e3aaed0debb966afabf38fd64fa`  
		Last Modified: Thu, 08 May 2025 18:08:01 GMT  
		Size: 165.1 MB (165127358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d7cf7d1bcbbcb13b7450db65bc70dfd19fb5f7590b356df3fab940fbf8cba`  
		Last Modified: Thu, 08 May 2025 17:19:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96de288013cc309eecd9eec102ad88fe7736a6bd14ab1250069113640b5b884`  
		Last Modified: Thu, 08 May 2025 17:19:21 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c67694a6825b4ce284ed8193bd9c3f9658273314b8449e35abb0c1bdcdf3db`  
		Last Modified: Thu, 08 May 2025 17:19:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a05a4b12342b57a21b89d33e6cbd2004cc99635efb1a1527c107c524ce5144f`  
		Last Modified: Thu, 08 May 2025 17:19:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c723b07660005078bbffb13f4edbc39e5ca99559e99b7fa5a7881afda50fafa`  
		Last Modified: Thu, 08 May 2025 17:19:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea6b7a326d5f089edc5616fb30bafc907839c65863fb036265c224ba3cf7e4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4398f32d35bbf9acb5c320c91c257e857d0f67450f6b663d1853c3922b38cc`

```dockerfile
```

-	Layers:
	-	`sha256:996a7ea981380fdb8779cac29b72e46e49ffaeb1c5ec35b1dfee35a443103fd4`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 25.9 KB (25872 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:43af4f67ca2fd47a7a69e270df107d480af42361b4d84b353031a2424d55a33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190013531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa07bd41ac94c406f079bc0f24fa9fd2f5eef9da44b04ad6ed1c22f5e7fa329a`
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
ARG VERSION=25.4.2.31
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bedbc25c514084e050c01a33fdff22e0249a4bdff2c072e38ba6a638dd7e18`  
		Last Modified: Thu, 08 May 2025 18:45:06 GMT  
		Size: 7.1 MB (7127833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a90118e42e4bdad3c7a8532ef133cac468a38065cbb6ef4e93b90ee1a67ca1`  
		Last Modified: Thu, 08 May 2025 18:45:23 GMT  
		Size: 154.7 MB (154661236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c81ecb567fd0321e1c1d04e20db1e12dca63731dcd560060624c7c783a1f46`  
		Last Modified: Thu, 08 May 2025 18:45:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cf4ee70f161e497192b458535b6defb153a22b7240b6ceedac143c46b626df`  
		Last Modified: Thu, 08 May 2025 18:45:08 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bab3c3d33f76349a90ee85942aef784402295347c75d30b1f94d9850a1325c`  
		Last Modified: Thu, 08 May 2025 18:45:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66347907d5b0d3d7ff59cc5ffea5c64dc0628356861b658c038bd592355ea530`  
		Last Modified: Thu, 08 May 2025 18:45:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9324ca125c1023b49ccec61906adf262c5549fe72322f96b788f8de12289e860`  
		Last Modified: Thu, 08 May 2025 18:45:10 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3c116def71e273097ffe59b356846b12dd9d76c01d5637109d14d8b53c360c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf5e5a1959b9e794e278e3f76537696257f2874b767a01c579c3b2328b1678f`

```dockerfile
```

-	Layers:
	-	`sha256:8d92e3637869e89c265b496e794a8804be72074d90bdd494525b9a0b5bbb93d9`  
		Last Modified: Mon, 05 May 2025 16:37:25 GMT  
		Size: 26.1 KB (26085 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.2-jammy`

```console
$ docker pull clickhouse@sha256:639f5710b90f9a7f12772d6460b104b8d201b74efd2737346413d6adb5d6777e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e582fda66d604d0f31d5815bea0c290b1b50a2b08bcb0c47e9120a391483ad30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202682168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc9f9d141c3d53f63fa966cf0403e650e0ea48e897c127cc943fe3567f41882`
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
ARG VERSION=25.4.2.31
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb3f27ffd917411d1b8798c3b7cad886f6862ba256261577893839cc0aa62e1`  
		Last Modified: Thu, 08 May 2025 17:18:50 GMT  
		Size: 7.2 MB (7151953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6cfef0a2e6413ede53483f57f0dcae70228e3aaed0debb966afabf38fd64fa`  
		Last Modified: Thu, 08 May 2025 18:08:01 GMT  
		Size: 165.1 MB (165127358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d7cf7d1bcbbcb13b7450db65bc70dfd19fb5f7590b356df3fab940fbf8cba`  
		Last Modified: Thu, 08 May 2025 17:19:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96de288013cc309eecd9eec102ad88fe7736a6bd14ab1250069113640b5b884`  
		Last Modified: Thu, 08 May 2025 17:19:21 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c67694a6825b4ce284ed8193bd9c3f9658273314b8449e35abb0c1bdcdf3db`  
		Last Modified: Thu, 08 May 2025 17:19:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a05a4b12342b57a21b89d33e6cbd2004cc99635efb1a1527c107c524ce5144f`  
		Last Modified: Thu, 08 May 2025 17:19:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c723b07660005078bbffb13f4edbc39e5ca99559e99b7fa5a7881afda50fafa`  
		Last Modified: Thu, 08 May 2025 17:19:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea6b7a326d5f089edc5616fb30bafc907839c65863fb036265c224ba3cf7e4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4398f32d35bbf9acb5c320c91c257e857d0f67450f6b663d1853c3922b38cc`

```dockerfile
```

-	Layers:
	-	`sha256:996a7ea981380fdb8779cac29b72e46e49ffaeb1c5ec35b1dfee35a443103fd4`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 25.9 KB (25872 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:43af4f67ca2fd47a7a69e270df107d480af42361b4d84b353031a2424d55a33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190013531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa07bd41ac94c406f079bc0f24fa9fd2f5eef9da44b04ad6ed1c22f5e7fa329a`
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
ARG VERSION=25.4.2.31
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bedbc25c514084e050c01a33fdff22e0249a4bdff2c072e38ba6a638dd7e18`  
		Last Modified: Thu, 08 May 2025 18:45:06 GMT  
		Size: 7.1 MB (7127833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a90118e42e4bdad3c7a8532ef133cac468a38065cbb6ef4e93b90ee1a67ca1`  
		Last Modified: Thu, 08 May 2025 18:45:23 GMT  
		Size: 154.7 MB (154661236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c81ecb567fd0321e1c1d04e20db1e12dca63731dcd560060624c7c783a1f46`  
		Last Modified: Thu, 08 May 2025 18:45:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cf4ee70f161e497192b458535b6defb153a22b7240b6ceedac143c46b626df`  
		Last Modified: Thu, 08 May 2025 18:45:08 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bab3c3d33f76349a90ee85942aef784402295347c75d30b1f94d9850a1325c`  
		Last Modified: Thu, 08 May 2025 18:45:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66347907d5b0d3d7ff59cc5ffea5c64dc0628356861b658c038bd592355ea530`  
		Last Modified: Thu, 08 May 2025 18:45:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9324ca125c1023b49ccec61906adf262c5549fe72322f96b788f8de12289e860`  
		Last Modified: Thu, 08 May 2025 18:45:10 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3c116def71e273097ffe59b356846b12dd9d76c01d5637109d14d8b53c360c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf5e5a1959b9e794e278e3f76537696257f2874b767a01c579c3b2328b1678f`

```dockerfile
```

-	Layers:
	-	`sha256:8d92e3637869e89c265b496e794a8804be72074d90bdd494525b9a0b5bbb93d9`  
		Last Modified: Mon, 05 May 2025 16:37:25 GMT  
		Size: 26.1 KB (26085 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.2.31`

```console
$ docker pull clickhouse@sha256:639f5710b90f9a7f12772d6460b104b8d201b74efd2737346413d6adb5d6777e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.2.31` - linux; amd64

```console
$ docker pull clickhouse@sha256:e582fda66d604d0f31d5815bea0c290b1b50a2b08bcb0c47e9120a391483ad30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202682168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc9f9d141c3d53f63fa966cf0403e650e0ea48e897c127cc943fe3567f41882`
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
ARG VERSION=25.4.2.31
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb3f27ffd917411d1b8798c3b7cad886f6862ba256261577893839cc0aa62e1`  
		Last Modified: Thu, 08 May 2025 17:18:50 GMT  
		Size: 7.2 MB (7151953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6cfef0a2e6413ede53483f57f0dcae70228e3aaed0debb966afabf38fd64fa`  
		Last Modified: Thu, 08 May 2025 18:08:01 GMT  
		Size: 165.1 MB (165127358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d7cf7d1bcbbcb13b7450db65bc70dfd19fb5f7590b356df3fab940fbf8cba`  
		Last Modified: Thu, 08 May 2025 17:19:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96de288013cc309eecd9eec102ad88fe7736a6bd14ab1250069113640b5b884`  
		Last Modified: Thu, 08 May 2025 17:19:21 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c67694a6825b4ce284ed8193bd9c3f9658273314b8449e35abb0c1bdcdf3db`  
		Last Modified: Thu, 08 May 2025 17:19:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a05a4b12342b57a21b89d33e6cbd2004cc99635efb1a1527c107c524ce5144f`  
		Last Modified: Thu, 08 May 2025 17:19:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c723b07660005078bbffb13f4edbc39e5ca99559e99b7fa5a7881afda50fafa`  
		Last Modified: Thu, 08 May 2025 17:19:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.2.31` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea6b7a326d5f089edc5616fb30bafc907839c65863fb036265c224ba3cf7e4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4398f32d35bbf9acb5c320c91c257e857d0f67450f6b663d1853c3922b38cc`

```dockerfile
```

-	Layers:
	-	`sha256:996a7ea981380fdb8779cac29b72e46e49ffaeb1c5ec35b1dfee35a443103fd4`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 25.9 KB (25872 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.2.31` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:43af4f67ca2fd47a7a69e270df107d480af42361b4d84b353031a2424d55a33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190013531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa07bd41ac94c406f079bc0f24fa9fd2f5eef9da44b04ad6ed1c22f5e7fa329a`
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
ARG VERSION=25.4.2.31
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bedbc25c514084e050c01a33fdff22e0249a4bdff2c072e38ba6a638dd7e18`  
		Last Modified: Thu, 08 May 2025 18:45:06 GMT  
		Size: 7.1 MB (7127833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a90118e42e4bdad3c7a8532ef133cac468a38065cbb6ef4e93b90ee1a67ca1`  
		Last Modified: Thu, 08 May 2025 18:45:23 GMT  
		Size: 154.7 MB (154661236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c81ecb567fd0321e1c1d04e20db1e12dca63731dcd560060624c7c783a1f46`  
		Last Modified: Thu, 08 May 2025 18:45:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cf4ee70f161e497192b458535b6defb153a22b7240b6ceedac143c46b626df`  
		Last Modified: Thu, 08 May 2025 18:45:08 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bab3c3d33f76349a90ee85942aef784402295347c75d30b1f94d9850a1325c`  
		Last Modified: Thu, 08 May 2025 18:45:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66347907d5b0d3d7ff59cc5ffea5c64dc0628356861b658c038bd592355ea530`  
		Last Modified: Thu, 08 May 2025 18:45:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9324ca125c1023b49ccec61906adf262c5549fe72322f96b788f8de12289e860`  
		Last Modified: Thu, 08 May 2025 18:45:10 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.2.31` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3c116def71e273097ffe59b356846b12dd9d76c01d5637109d14d8b53c360c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf5e5a1959b9e794e278e3f76537696257f2874b767a01c579c3b2328b1678f`

```dockerfile
```

-	Layers:
	-	`sha256:8d92e3637869e89c265b496e794a8804be72074d90bdd494525b9a0b5bbb93d9`  
		Last Modified: Mon, 05 May 2025 16:37:25 GMT  
		Size: 26.1 KB (26085 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.2.31-jammy`

```console
$ docker pull clickhouse@sha256:639f5710b90f9a7f12772d6460b104b8d201b74efd2737346413d6adb5d6777e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4.2.31-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e582fda66d604d0f31d5815bea0c290b1b50a2b08bcb0c47e9120a391483ad30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202682168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc9f9d141c3d53f63fa966cf0403e650e0ea48e897c127cc943fe3567f41882`
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
ARG VERSION=25.4.2.31
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb3f27ffd917411d1b8798c3b7cad886f6862ba256261577893839cc0aa62e1`  
		Last Modified: Thu, 08 May 2025 17:18:50 GMT  
		Size: 7.2 MB (7151953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6cfef0a2e6413ede53483f57f0dcae70228e3aaed0debb966afabf38fd64fa`  
		Last Modified: Thu, 08 May 2025 18:08:01 GMT  
		Size: 165.1 MB (165127358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d7cf7d1bcbbcb13b7450db65bc70dfd19fb5f7590b356df3fab940fbf8cba`  
		Last Modified: Thu, 08 May 2025 17:19:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96de288013cc309eecd9eec102ad88fe7736a6bd14ab1250069113640b5b884`  
		Last Modified: Thu, 08 May 2025 17:19:21 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c67694a6825b4ce284ed8193bd9c3f9658273314b8449e35abb0c1bdcdf3db`  
		Last Modified: Thu, 08 May 2025 17:19:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a05a4b12342b57a21b89d33e6cbd2004cc99635efb1a1527c107c524ce5144f`  
		Last Modified: Thu, 08 May 2025 17:19:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c723b07660005078bbffb13f4edbc39e5ca99559e99b7fa5a7881afda50fafa`  
		Last Modified: Thu, 08 May 2025 17:19:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.2.31-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea6b7a326d5f089edc5616fb30bafc907839c65863fb036265c224ba3cf7e4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4398f32d35bbf9acb5c320c91c257e857d0f67450f6b663d1853c3922b38cc`

```dockerfile
```

-	Layers:
	-	`sha256:996a7ea981380fdb8779cac29b72e46e49ffaeb1c5ec35b1dfee35a443103fd4`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 25.9 KB (25872 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4.2.31-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:43af4f67ca2fd47a7a69e270df107d480af42361b4d84b353031a2424d55a33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190013531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa07bd41ac94c406f079bc0f24fa9fd2f5eef9da44b04ad6ed1c22f5e7fa329a`
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
ARG VERSION=25.4.2.31
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bedbc25c514084e050c01a33fdff22e0249a4bdff2c072e38ba6a638dd7e18`  
		Last Modified: Thu, 08 May 2025 18:45:06 GMT  
		Size: 7.1 MB (7127833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a90118e42e4bdad3c7a8532ef133cac468a38065cbb6ef4e93b90ee1a67ca1`  
		Last Modified: Thu, 08 May 2025 18:45:23 GMT  
		Size: 154.7 MB (154661236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c81ecb567fd0321e1c1d04e20db1e12dca63731dcd560060624c7c783a1f46`  
		Last Modified: Thu, 08 May 2025 18:45:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cf4ee70f161e497192b458535b6defb153a22b7240b6ceedac143c46b626df`  
		Last Modified: Thu, 08 May 2025 18:45:08 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bab3c3d33f76349a90ee85942aef784402295347c75d30b1f94d9850a1325c`  
		Last Modified: Thu, 08 May 2025 18:45:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66347907d5b0d3d7ff59cc5ffea5c64dc0628356861b658c038bd592355ea530`  
		Last Modified: Thu, 08 May 2025 18:45:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9324ca125c1023b49ccec61906adf262c5549fe72322f96b788f8de12289e860`  
		Last Modified: Thu, 08 May 2025 18:45:10 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4.2.31-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3c116def71e273097ffe59b356846b12dd9d76c01d5637109d14d8b53c360c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf5e5a1959b9e794e278e3f76537696257f2874b767a01c579c3b2328b1678f`

```dockerfile
```

-	Layers:
	-	`sha256:8d92e3637869e89c265b496e794a8804be72074d90bdd494525b9a0b5bbb93d9`  
		Last Modified: Mon, 05 May 2025 16:37:25 GMT  
		Size: 26.1 KB (26085 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:639f5710b90f9a7f12772d6460b104b8d201b74efd2737346413d6adb5d6777e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e582fda66d604d0f31d5815bea0c290b1b50a2b08bcb0c47e9120a391483ad30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202682168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc9f9d141c3d53f63fa966cf0403e650e0ea48e897c127cc943fe3567f41882`
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
ARG VERSION=25.4.2.31
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb3f27ffd917411d1b8798c3b7cad886f6862ba256261577893839cc0aa62e1`  
		Last Modified: Thu, 08 May 2025 17:18:50 GMT  
		Size: 7.2 MB (7151953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6cfef0a2e6413ede53483f57f0dcae70228e3aaed0debb966afabf38fd64fa`  
		Last Modified: Thu, 08 May 2025 18:08:01 GMT  
		Size: 165.1 MB (165127358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d7cf7d1bcbbcb13b7450db65bc70dfd19fb5f7590b356df3fab940fbf8cba`  
		Last Modified: Thu, 08 May 2025 17:19:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96de288013cc309eecd9eec102ad88fe7736a6bd14ab1250069113640b5b884`  
		Last Modified: Thu, 08 May 2025 17:19:21 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c67694a6825b4ce284ed8193bd9c3f9658273314b8449e35abb0c1bdcdf3db`  
		Last Modified: Thu, 08 May 2025 17:19:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a05a4b12342b57a21b89d33e6cbd2004cc99635efb1a1527c107c524ce5144f`  
		Last Modified: Thu, 08 May 2025 17:19:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c723b07660005078bbffb13f4edbc39e5ca99559e99b7fa5a7881afda50fafa`  
		Last Modified: Thu, 08 May 2025 17:19:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea6b7a326d5f089edc5616fb30bafc907839c65863fb036265c224ba3cf7e4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4398f32d35bbf9acb5c320c91c257e857d0f67450f6b663d1853c3922b38cc`

```dockerfile
```

-	Layers:
	-	`sha256:996a7ea981380fdb8779cac29b72e46e49ffaeb1c5ec35b1dfee35a443103fd4`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 25.9 KB (25872 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:43af4f67ca2fd47a7a69e270df107d480af42361b4d84b353031a2424d55a33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190013531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa07bd41ac94c406f079bc0f24fa9fd2f5eef9da44b04ad6ed1c22f5e7fa329a`
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
ARG VERSION=25.4.2.31
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bedbc25c514084e050c01a33fdff22e0249a4bdff2c072e38ba6a638dd7e18`  
		Last Modified: Thu, 08 May 2025 18:45:06 GMT  
		Size: 7.1 MB (7127833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a90118e42e4bdad3c7a8532ef133cac468a38065cbb6ef4e93b90ee1a67ca1`  
		Last Modified: Thu, 08 May 2025 18:45:23 GMT  
		Size: 154.7 MB (154661236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c81ecb567fd0321e1c1d04e20db1e12dca63731dcd560060624c7c783a1f46`  
		Last Modified: Thu, 08 May 2025 18:45:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cf4ee70f161e497192b458535b6defb153a22b7240b6ceedac143c46b626df`  
		Last Modified: Thu, 08 May 2025 18:45:08 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bab3c3d33f76349a90ee85942aef784402295347c75d30b1f94d9850a1325c`  
		Last Modified: Thu, 08 May 2025 18:45:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66347907d5b0d3d7ff59cc5ffea5c64dc0628356861b658c038bd592355ea530`  
		Last Modified: Thu, 08 May 2025 18:45:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9324ca125c1023b49ccec61906adf262c5549fe72322f96b788f8de12289e860`  
		Last Modified: Thu, 08 May 2025 18:45:10 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3c116def71e273097ffe59b356846b12dd9d76c01d5637109d14d8b53c360c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf5e5a1959b9e794e278e3f76537696257f2874b767a01c579c3b2328b1678f`

```dockerfile
```

-	Layers:
	-	`sha256:8d92e3637869e89c265b496e794a8804be72074d90bdd494525b9a0b5bbb93d9`  
		Last Modified: Mon, 05 May 2025 16:37:25 GMT  
		Size: 26.1 KB (26085 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:639f5710b90f9a7f12772d6460b104b8d201b74efd2737346413d6adb5d6777e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:e582fda66d604d0f31d5815bea0c290b1b50a2b08bcb0c47e9120a391483ad30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202682168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc9f9d141c3d53f63fa966cf0403e650e0ea48e897c127cc943fe3567f41882`
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
ARG VERSION=25.4.2.31
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb3f27ffd917411d1b8798c3b7cad886f6862ba256261577893839cc0aa62e1`  
		Last Modified: Thu, 08 May 2025 17:18:50 GMT  
		Size: 7.2 MB (7151953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6cfef0a2e6413ede53483f57f0dcae70228e3aaed0debb966afabf38fd64fa`  
		Last Modified: Thu, 08 May 2025 18:08:01 GMT  
		Size: 165.1 MB (165127358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1d7cf7d1bcbbcb13b7450db65bc70dfd19fb5f7590b356df3fab940fbf8cba`  
		Last Modified: Thu, 08 May 2025 17:19:19 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96de288013cc309eecd9eec102ad88fe7736a6bd14ab1250069113640b5b884`  
		Last Modified: Thu, 08 May 2025 17:19:21 GMT  
		Size: 865.7 KB (865744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c67694a6825b4ce284ed8193bd9c3f9658273314b8449e35abb0c1bdcdf3db`  
		Last Modified: Thu, 08 May 2025 17:19:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a05a4b12342b57a21b89d33e6cbd2004cc99635efb1a1527c107c524ce5144f`  
		Last Modified: Thu, 08 May 2025 17:19:30 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c723b07660005078bbffb13f4edbc39e5ca99559e99b7fa5a7881afda50fafa`  
		Last Modified: Thu, 08 May 2025 17:19:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea6b7a326d5f089edc5616fb30bafc907839c65863fb036265c224ba3cf7e4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff4398f32d35bbf9acb5c320c91c257e857d0f67450f6b663d1853c3922b38cc`

```dockerfile
```

-	Layers:
	-	`sha256:996a7ea981380fdb8779cac29b72e46e49ffaeb1c5ec35b1dfee35a443103fd4`  
		Last Modified: Mon, 05 May 2025 16:34:56 GMT  
		Size: 25.9 KB (25872 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:43af4f67ca2fd47a7a69e270df107d480af42361b4d84b353031a2424d55a33f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190013531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa07bd41ac94c406f079bc0f24fa9fd2f5eef9da44b04ad6ed1c22f5e7fa329a`
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
ARG VERSION=25.4.2.31
# Fri, 02 May 2025 10:04:11 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 02 May 2025 10:04:11 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 May 2025 10:04:11 GMT
ENV TZ=UTC
# Fri, 02 May 2025 10:04:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.4.2.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 27.4 MB (27354211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11bedbc25c514084e050c01a33fdff22e0249a4bdff2c072e38ba6a638dd7e18`  
		Last Modified: Thu, 08 May 2025 18:45:06 GMT  
		Size: 7.1 MB (7127833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a90118e42e4bdad3c7a8532ef133cac468a38065cbb6ef4e93b90ee1a67ca1`  
		Last Modified: Thu, 08 May 2025 18:45:23 GMT  
		Size: 154.7 MB (154661236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69c81ecb567fd0321e1c1d04e20db1e12dca63731dcd560060624c7c783a1f46`  
		Last Modified: Thu, 08 May 2025 18:45:07 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cf4ee70f161e497192b458535b6defb153a22b7240b6ceedac143c46b626df`  
		Last Modified: Thu, 08 May 2025 18:45:08 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bab3c3d33f76349a90ee85942aef784402295347c75d30b1f94d9850a1325c`  
		Last Modified: Thu, 08 May 2025 18:45:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66347907d5b0d3d7ff59cc5ffea5c64dc0628356861b658c038bd592355ea530`  
		Last Modified: Thu, 08 May 2025 18:45:09 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9324ca125c1023b49ccec61906adf262c5549fe72322f96b788f8de12289e860`  
		Last Modified: Thu, 08 May 2025 18:45:10 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3c116def71e273097ffe59b356846b12dd9d76c01d5637109d14d8b53c360c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bf5e5a1959b9e794e278e3f76537696257f2874b767a01c579c3b2328b1678f`

```dockerfile
```

-	Layers:
	-	`sha256:8d92e3637869e89c265b496e794a8804be72074d90bdd494525b9a0b5bbb93d9`  
		Last Modified: Mon, 05 May 2025 16:37:25 GMT  
		Size: 26.1 KB (26085 bytes)  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293c18414ddc6b5045bd255b1d3fff2b475d11f7bd01cf6f63c08323588bfeb`  
		Last Modified: Thu, 08 May 2025 17:14:45 GMT  
		Size: 7.2 MB (7152053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a83e724674ef99b3a02f95d6f99edb74d6da86f3e952d96df426d2e24ffad54`  
		Last Modified: Thu, 08 May 2025 17:14:52 GMT  
		Size: 167.0 MB (166978959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5788f6ecbfd19db9de8f1ebca0a309877c17b3a68e2b6927db7178a38dd3e2ea`  
		Last Modified: Thu, 08 May 2025 17:14:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c12c8cb54ca9170c10677abfac3c0cd2a66c86322bdbab8b6e6fe92cc0137`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477777a3fe047b2d393a11522c673d966c5106c04a594f53822905dfb3099ed`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357524fb1f1cb1c745bd69563a49c927ad2294938d4f470a351f5f65404ffdc`  
		Last Modified: Thu, 08 May 2025 17:14:49 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89b4acb36be4c123b76a5f2e389268a91bc95467c65d1b794c398fd8fb1631`  
		Last Modified: Thu, 08 May 2025 17:14:49 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
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
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5293c18414ddc6b5045bd255b1d3fff2b475d11f7bd01cf6f63c08323588bfeb`  
		Last Modified: Thu, 08 May 2025 17:14:45 GMT  
		Size: 7.2 MB (7152053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a83e724674ef99b3a02f95d6f99edb74d6da86f3e952d96df426d2e24ffad54`  
		Last Modified: Thu, 08 May 2025 17:14:52 GMT  
		Size: 167.0 MB (166978959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5788f6ecbfd19db9de8f1ebca0a309877c17b3a68e2b6927db7178a38dd3e2ea`  
		Last Modified: Thu, 08 May 2025 17:14:46 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c12c8cb54ca9170c10677abfac3c0cd2a66c86322bdbab8b6e6fe92cc0137`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477777a3fe047b2d393a11522c673d966c5106c04a594f53822905dfb3099ed`  
		Last Modified: Thu, 08 May 2025 17:14:48 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5357524fb1f1cb1c745bd69563a49c927ad2294938d4f470a351f5f65404ffdc`  
		Last Modified: Thu, 08 May 2025 17:14:49 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c89b4acb36be4c123b76a5f2e389268a91bc95467c65d1b794c398fd8fb1631`  
		Last Modified: Thu, 08 May 2025 17:14:49 GMT  
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
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
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
