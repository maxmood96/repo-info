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
-	[`clickhouse:25.4.7`](#clickhouse2547)
-	[`clickhouse:25.4.7-jammy`](#clickhouse2547-jammy)
-	[`clickhouse:25.4.7.66`](#clickhouse254766)
-	[`clickhouse:25.4.7.66-jammy`](#clickhouse254766-jammy)
-	[`clickhouse:25.5`](#clickhouse255)
-	[`clickhouse:25.5-jammy`](#clickhouse255-jammy)
-	[`clickhouse:25.5.3`](#clickhouse2553)
-	[`clickhouse:25.5.3-jammy`](#clickhouse2553-jammy)
-	[`clickhouse:25.5.3.75`](#clickhouse255375)
-	[`clickhouse:25.5.3.75-jammy`](#clickhouse255375-jammy)
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

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:a13b72e1ccf25aef8be2e4f1aebfed42a348ca963ecf3fa833669c3b440b9f15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:3642182a619cec92e3d796525e5e7324f533a11ca460eeadcd9cb2fcb2599809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710b81e76d9f3be348143654072f49b51aefd55f6456b10204d1c9d1547a4ce7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
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
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1164d17c203def662aa15fa7537b0c471e391a406322ea048fc04ce7049e3c`  
		Last Modified: Tue, 03 Jun 2025 13:35:50 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9942f24a20ba860cdcabc61c00fad11a6e1175d95231af361420459328ce7`  
		Last Modified: Tue, 03 Jun 2025 13:36:06 GMT  
		Size: 167.0 MB (166978781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e126fc138f8f2a0fb43764a8992715dc41159afa1a5de6c8082b400de39b2926`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eea866cba85dc8756e04f79927fd55592350d08b96b27a3c770383aa9903d2`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d0918ffa972436db12d329a437bcd647a4a28e3bbd2568e06ae0e6c7098d8`  
		Last Modified: Tue, 03 Jun 2025 13:35:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263c331f3d7ad8bfbf09c052ef8f93e8e10ca419c3d5b37fde68cdcdfeb0910`  
		Last Modified: Tue, 03 Jun 2025 13:35:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a10302743efc73ef39922a2eaed3f6046e29820028151c06f37b875f4966ae1`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a1871b03ebda7524b20dbe45b0fb8c17e3e28c8b648700ee4c8fcc556e886611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5084401e3632c3b300d60fbb95b1248320dc5ff262d9864e4e37bb42493b8b4`

```dockerfile
```

-	Layers:
	-	`sha256:4fb376b0725185667bf473b112fbfd93df7c33f3f53904103450d279cef15619`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:97f5119c9be0aeed23b93f06162ac401eceb4b5f36276f6b46dfc99c8064f210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192036654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaa1a1ac10e1650228fe42d49b26d8ca3140669507795ddda87bf3bde3be4b6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
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
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230b813b118aa053f351c3a882051f13c87cbc0aa9093eab452d39e8521bb180`  
		Last Modified: Tue, 03 Jun 2025 13:31:07 GMT  
		Size: 7.1 MB (7127800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec841349f8ced4ed21f3bfc7f105713814cb35b0811b93ec29ba59d79f94abe3`  
		Last Modified: Tue, 03 Jun 2025 13:31:35 GMT  
		Size: 156.7 MB (156683026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147790bdc5cc722beb6e6475e3ecb592d9a8b6a2aa0a06969f738f1f118047e`  
		Last Modified: Tue, 03 Jun 2025 13:31:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75706d9bdb4454a8b5e8a927afade509f01dde0a0dd15cbd6dd621962bc2b63`  
		Last Modified: Tue, 03 Jun 2025 13:31:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9297cb454be3bfb83d1be25a36e26e571d91379f464f1f78e2c26cb6b80f11c`  
		Last Modified: Tue, 03 Jun 2025 13:31:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ca170954ac44c9ded2ab1245ffded8a53b48465b0f0afdde712d63692ae2be`  
		Last Modified: Tue, 03 Jun 2025 13:31:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6350e0fff42f552f29b13465836afb26aae82804876da67ba8f173cca0c55b8`  
		Last Modified: Tue, 03 Jun 2025 13:31:17 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f5f4450ab24c67170e5e6ea53247899f99b367124b61cd40475f75c8cc51c0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851417b84955eb5b5ea7f0020fd28abdf49e7b08b6a4b6953292a0e35966bf4f`

```dockerfile
```

-	Layers:
	-	`sha256:8ab0b0448fd4735e24b7ffe6b9280a64ecf1e6669d3571e4e8c76d71ff785474`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 26.1 KB (26086 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:a13b72e1ccf25aef8be2e4f1aebfed42a348ca963ecf3fa833669c3b440b9f15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:3642182a619cec92e3d796525e5e7324f533a11ca460eeadcd9cb2fcb2599809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710b81e76d9f3be348143654072f49b51aefd55f6456b10204d1c9d1547a4ce7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
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
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1164d17c203def662aa15fa7537b0c471e391a406322ea048fc04ce7049e3c`  
		Last Modified: Tue, 03 Jun 2025 13:35:50 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9942f24a20ba860cdcabc61c00fad11a6e1175d95231af361420459328ce7`  
		Last Modified: Tue, 03 Jun 2025 13:36:06 GMT  
		Size: 167.0 MB (166978781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e126fc138f8f2a0fb43764a8992715dc41159afa1a5de6c8082b400de39b2926`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eea866cba85dc8756e04f79927fd55592350d08b96b27a3c770383aa9903d2`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d0918ffa972436db12d329a437bcd647a4a28e3bbd2568e06ae0e6c7098d8`  
		Last Modified: Tue, 03 Jun 2025 13:35:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263c331f3d7ad8bfbf09c052ef8f93e8e10ca419c3d5b37fde68cdcdfeb0910`  
		Last Modified: Tue, 03 Jun 2025 13:35:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a10302743efc73ef39922a2eaed3f6046e29820028151c06f37b875f4966ae1`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a1871b03ebda7524b20dbe45b0fb8c17e3e28c8b648700ee4c8fcc556e886611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5084401e3632c3b300d60fbb95b1248320dc5ff262d9864e4e37bb42493b8b4`

```dockerfile
```

-	Layers:
	-	`sha256:4fb376b0725185667bf473b112fbfd93df7c33f3f53904103450d279cef15619`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:97f5119c9be0aeed23b93f06162ac401eceb4b5f36276f6b46dfc99c8064f210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192036654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaa1a1ac10e1650228fe42d49b26d8ca3140669507795ddda87bf3bde3be4b6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
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
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230b813b118aa053f351c3a882051f13c87cbc0aa9093eab452d39e8521bb180`  
		Last Modified: Tue, 03 Jun 2025 13:31:07 GMT  
		Size: 7.1 MB (7127800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec841349f8ced4ed21f3bfc7f105713814cb35b0811b93ec29ba59d79f94abe3`  
		Last Modified: Tue, 03 Jun 2025 13:31:35 GMT  
		Size: 156.7 MB (156683026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147790bdc5cc722beb6e6475e3ecb592d9a8b6a2aa0a06969f738f1f118047e`  
		Last Modified: Tue, 03 Jun 2025 13:31:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75706d9bdb4454a8b5e8a927afade509f01dde0a0dd15cbd6dd621962bc2b63`  
		Last Modified: Tue, 03 Jun 2025 13:31:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9297cb454be3bfb83d1be25a36e26e571d91379f464f1f78e2c26cb6b80f11c`  
		Last Modified: Tue, 03 Jun 2025 13:31:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ca170954ac44c9ded2ab1245ffded8a53b48465b0f0afdde712d63692ae2be`  
		Last Modified: Tue, 03 Jun 2025 13:31:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6350e0fff42f552f29b13465836afb26aae82804876da67ba8f173cca0c55b8`  
		Last Modified: Tue, 03 Jun 2025 13:31:17 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f5f4450ab24c67170e5e6ea53247899f99b367124b61cd40475f75c8cc51c0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851417b84955eb5b5ea7f0020fd28abdf49e7b08b6a4b6953292a0e35966bf4f`

```dockerfile
```

-	Layers:
	-	`sha256:8ab0b0448fd4735e24b7ffe6b9280a64ecf1e6669d3571e4e8c76d71ff785474`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 26.1 KB (26086 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.3`

```console
$ docker pull clickhouse@sha256:a13b72e1ccf25aef8be2e4f1aebfed42a348ca963ecf3fa833669c3b440b9f15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:3642182a619cec92e3d796525e5e7324f533a11ca460eeadcd9cb2fcb2599809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710b81e76d9f3be348143654072f49b51aefd55f6456b10204d1c9d1547a4ce7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
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
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1164d17c203def662aa15fa7537b0c471e391a406322ea048fc04ce7049e3c`  
		Last Modified: Tue, 03 Jun 2025 13:35:50 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9942f24a20ba860cdcabc61c00fad11a6e1175d95231af361420459328ce7`  
		Last Modified: Tue, 03 Jun 2025 13:36:06 GMT  
		Size: 167.0 MB (166978781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e126fc138f8f2a0fb43764a8992715dc41159afa1a5de6c8082b400de39b2926`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eea866cba85dc8756e04f79927fd55592350d08b96b27a3c770383aa9903d2`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d0918ffa972436db12d329a437bcd647a4a28e3bbd2568e06ae0e6c7098d8`  
		Last Modified: Tue, 03 Jun 2025 13:35:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263c331f3d7ad8bfbf09c052ef8f93e8e10ca419c3d5b37fde68cdcdfeb0910`  
		Last Modified: Tue, 03 Jun 2025 13:35:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a10302743efc73ef39922a2eaed3f6046e29820028151c06f37b875f4966ae1`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a1871b03ebda7524b20dbe45b0fb8c17e3e28c8b648700ee4c8fcc556e886611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5084401e3632c3b300d60fbb95b1248320dc5ff262d9864e4e37bb42493b8b4`

```dockerfile
```

-	Layers:
	-	`sha256:4fb376b0725185667bf473b112fbfd93df7c33f3f53904103450d279cef15619`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:97f5119c9be0aeed23b93f06162ac401eceb4b5f36276f6b46dfc99c8064f210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192036654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaa1a1ac10e1650228fe42d49b26d8ca3140669507795ddda87bf3bde3be4b6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
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
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230b813b118aa053f351c3a882051f13c87cbc0aa9093eab452d39e8521bb180`  
		Last Modified: Tue, 03 Jun 2025 13:31:07 GMT  
		Size: 7.1 MB (7127800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec841349f8ced4ed21f3bfc7f105713814cb35b0811b93ec29ba59d79f94abe3`  
		Last Modified: Tue, 03 Jun 2025 13:31:35 GMT  
		Size: 156.7 MB (156683026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147790bdc5cc722beb6e6475e3ecb592d9a8b6a2aa0a06969f738f1f118047e`  
		Last Modified: Tue, 03 Jun 2025 13:31:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75706d9bdb4454a8b5e8a927afade509f01dde0a0dd15cbd6dd621962bc2b63`  
		Last Modified: Tue, 03 Jun 2025 13:31:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9297cb454be3bfb83d1be25a36e26e571d91379f464f1f78e2c26cb6b80f11c`  
		Last Modified: Tue, 03 Jun 2025 13:31:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ca170954ac44c9ded2ab1245ffded8a53b48465b0f0afdde712d63692ae2be`  
		Last Modified: Tue, 03 Jun 2025 13:31:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6350e0fff42f552f29b13465836afb26aae82804876da67ba8f173cca0c55b8`  
		Last Modified: Tue, 03 Jun 2025 13:31:17 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f5f4450ab24c67170e5e6ea53247899f99b367124b61cd40475f75c8cc51c0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851417b84955eb5b5ea7f0020fd28abdf49e7b08b6a4b6953292a0e35966bf4f`

```dockerfile
```

-	Layers:
	-	`sha256:8ab0b0448fd4735e24b7ffe6b9280a64ecf1e6669d3571e4e8c76d71ff785474`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 26.1 KB (26086 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.3-jammy`

```console
$ docker pull clickhouse@sha256:a13b72e1ccf25aef8be2e4f1aebfed42a348ca963ecf3fa833669c3b440b9f15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:3642182a619cec92e3d796525e5e7324f533a11ca460eeadcd9cb2fcb2599809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710b81e76d9f3be348143654072f49b51aefd55f6456b10204d1c9d1547a4ce7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
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
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1164d17c203def662aa15fa7537b0c471e391a406322ea048fc04ce7049e3c`  
		Last Modified: Tue, 03 Jun 2025 13:35:50 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9942f24a20ba860cdcabc61c00fad11a6e1175d95231af361420459328ce7`  
		Last Modified: Tue, 03 Jun 2025 13:36:06 GMT  
		Size: 167.0 MB (166978781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e126fc138f8f2a0fb43764a8992715dc41159afa1a5de6c8082b400de39b2926`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eea866cba85dc8756e04f79927fd55592350d08b96b27a3c770383aa9903d2`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d0918ffa972436db12d329a437bcd647a4a28e3bbd2568e06ae0e6c7098d8`  
		Last Modified: Tue, 03 Jun 2025 13:35:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263c331f3d7ad8bfbf09c052ef8f93e8e10ca419c3d5b37fde68cdcdfeb0910`  
		Last Modified: Tue, 03 Jun 2025 13:35:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a10302743efc73ef39922a2eaed3f6046e29820028151c06f37b875f4966ae1`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a1871b03ebda7524b20dbe45b0fb8c17e3e28c8b648700ee4c8fcc556e886611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5084401e3632c3b300d60fbb95b1248320dc5ff262d9864e4e37bb42493b8b4`

```dockerfile
```

-	Layers:
	-	`sha256:4fb376b0725185667bf473b112fbfd93df7c33f3f53904103450d279cef15619`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:97f5119c9be0aeed23b93f06162ac401eceb4b5f36276f6b46dfc99c8064f210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192036654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaa1a1ac10e1650228fe42d49b26d8ca3140669507795ddda87bf3bde3be4b6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
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
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230b813b118aa053f351c3a882051f13c87cbc0aa9093eab452d39e8521bb180`  
		Last Modified: Tue, 03 Jun 2025 13:31:07 GMT  
		Size: 7.1 MB (7127800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec841349f8ced4ed21f3bfc7f105713814cb35b0811b93ec29ba59d79f94abe3`  
		Last Modified: Tue, 03 Jun 2025 13:31:35 GMT  
		Size: 156.7 MB (156683026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147790bdc5cc722beb6e6475e3ecb592d9a8b6a2aa0a06969f738f1f118047e`  
		Last Modified: Tue, 03 Jun 2025 13:31:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75706d9bdb4454a8b5e8a927afade509f01dde0a0dd15cbd6dd621962bc2b63`  
		Last Modified: Tue, 03 Jun 2025 13:31:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9297cb454be3bfb83d1be25a36e26e571d91379f464f1f78e2c26cb6b80f11c`  
		Last Modified: Tue, 03 Jun 2025 13:31:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ca170954ac44c9ded2ab1245ffded8a53b48465b0f0afdde712d63692ae2be`  
		Last Modified: Tue, 03 Jun 2025 13:31:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6350e0fff42f552f29b13465836afb26aae82804876da67ba8f173cca0c55b8`  
		Last Modified: Tue, 03 Jun 2025 13:31:17 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f5f4450ab24c67170e5e6ea53247899f99b367124b61cd40475f75c8cc51c0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851417b84955eb5b5ea7f0020fd28abdf49e7b08b6a4b6953292a0e35966bf4f`

```dockerfile
```

-	Layers:
	-	`sha256:8ab0b0448fd4735e24b7ffe6b9280a64ecf1e6669d3571e4e8c76d71ff785474`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 26.1 KB (26086 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.3.42`

```console
$ docker pull clickhouse@sha256:a13b72e1ccf25aef8be2e4f1aebfed42a348ca963ecf3fa833669c3b440b9f15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.3.42` - linux; amd64

```console
$ docker pull clickhouse@sha256:3642182a619cec92e3d796525e5e7324f533a11ca460eeadcd9cb2fcb2599809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710b81e76d9f3be348143654072f49b51aefd55f6456b10204d1c9d1547a4ce7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
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
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1164d17c203def662aa15fa7537b0c471e391a406322ea048fc04ce7049e3c`  
		Last Modified: Tue, 03 Jun 2025 13:35:50 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9942f24a20ba860cdcabc61c00fad11a6e1175d95231af361420459328ce7`  
		Last Modified: Tue, 03 Jun 2025 13:36:06 GMT  
		Size: 167.0 MB (166978781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e126fc138f8f2a0fb43764a8992715dc41159afa1a5de6c8082b400de39b2926`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eea866cba85dc8756e04f79927fd55592350d08b96b27a3c770383aa9903d2`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d0918ffa972436db12d329a437bcd647a4a28e3bbd2568e06ae0e6c7098d8`  
		Last Modified: Tue, 03 Jun 2025 13:35:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263c331f3d7ad8bfbf09c052ef8f93e8e10ca419c3d5b37fde68cdcdfeb0910`  
		Last Modified: Tue, 03 Jun 2025 13:35:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a10302743efc73ef39922a2eaed3f6046e29820028151c06f37b875f4966ae1`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.3.42` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a1871b03ebda7524b20dbe45b0fb8c17e3e28c8b648700ee4c8fcc556e886611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5084401e3632c3b300d60fbb95b1248320dc5ff262d9864e4e37bb42493b8b4`

```dockerfile
```

-	Layers:
	-	`sha256:4fb376b0725185667bf473b112fbfd93df7c33f3f53904103450d279cef15619`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.3.42` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:97f5119c9be0aeed23b93f06162ac401eceb4b5f36276f6b46dfc99c8064f210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192036654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaa1a1ac10e1650228fe42d49b26d8ca3140669507795ddda87bf3bde3be4b6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
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
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230b813b118aa053f351c3a882051f13c87cbc0aa9093eab452d39e8521bb180`  
		Last Modified: Tue, 03 Jun 2025 13:31:07 GMT  
		Size: 7.1 MB (7127800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec841349f8ced4ed21f3bfc7f105713814cb35b0811b93ec29ba59d79f94abe3`  
		Last Modified: Tue, 03 Jun 2025 13:31:35 GMT  
		Size: 156.7 MB (156683026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147790bdc5cc722beb6e6475e3ecb592d9a8b6a2aa0a06969f738f1f118047e`  
		Last Modified: Tue, 03 Jun 2025 13:31:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75706d9bdb4454a8b5e8a927afade509f01dde0a0dd15cbd6dd621962bc2b63`  
		Last Modified: Tue, 03 Jun 2025 13:31:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9297cb454be3bfb83d1be25a36e26e571d91379f464f1f78e2c26cb6b80f11c`  
		Last Modified: Tue, 03 Jun 2025 13:31:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ca170954ac44c9ded2ab1245ffded8a53b48465b0f0afdde712d63692ae2be`  
		Last Modified: Tue, 03 Jun 2025 13:31:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6350e0fff42f552f29b13465836afb26aae82804876da67ba8f173cca0c55b8`  
		Last Modified: Tue, 03 Jun 2025 13:31:17 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.3.42` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f5f4450ab24c67170e5e6ea53247899f99b367124b61cd40475f75c8cc51c0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851417b84955eb5b5ea7f0020fd28abdf49e7b08b6a4b6953292a0e35966bf4f`

```dockerfile
```

-	Layers:
	-	`sha256:8ab0b0448fd4735e24b7ffe6b9280a64ecf1e6669d3571e4e8c76d71ff785474`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 26.1 KB (26086 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.3.42-jammy`

```console
$ docker pull clickhouse@sha256:a13b72e1ccf25aef8be2e4f1aebfed42a348ca963ecf3fa833669c3b440b9f15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.3.42-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:3642182a619cec92e3d796525e5e7324f533a11ca460eeadcd9cb2fcb2599809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710b81e76d9f3be348143654072f49b51aefd55f6456b10204d1c9d1547a4ce7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
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
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1164d17c203def662aa15fa7537b0c471e391a406322ea048fc04ce7049e3c`  
		Last Modified: Tue, 03 Jun 2025 13:35:50 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9942f24a20ba860cdcabc61c00fad11a6e1175d95231af361420459328ce7`  
		Last Modified: Tue, 03 Jun 2025 13:36:06 GMT  
		Size: 167.0 MB (166978781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e126fc138f8f2a0fb43764a8992715dc41159afa1a5de6c8082b400de39b2926`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eea866cba85dc8756e04f79927fd55592350d08b96b27a3c770383aa9903d2`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d0918ffa972436db12d329a437bcd647a4a28e3bbd2568e06ae0e6c7098d8`  
		Last Modified: Tue, 03 Jun 2025 13:35:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263c331f3d7ad8bfbf09c052ef8f93e8e10ca419c3d5b37fde68cdcdfeb0910`  
		Last Modified: Tue, 03 Jun 2025 13:35:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a10302743efc73ef39922a2eaed3f6046e29820028151c06f37b875f4966ae1`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.3.42-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a1871b03ebda7524b20dbe45b0fb8c17e3e28c8b648700ee4c8fcc556e886611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5084401e3632c3b300d60fbb95b1248320dc5ff262d9864e4e37bb42493b8b4`

```dockerfile
```

-	Layers:
	-	`sha256:4fb376b0725185667bf473b112fbfd93df7c33f3f53904103450d279cef15619`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.3.42-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:97f5119c9be0aeed23b93f06162ac401eceb4b5f36276f6b46dfc99c8064f210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192036654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaa1a1ac10e1650228fe42d49b26d8ca3140669507795ddda87bf3bde3be4b6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
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
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230b813b118aa053f351c3a882051f13c87cbc0aa9093eab452d39e8521bb180`  
		Last Modified: Tue, 03 Jun 2025 13:31:07 GMT  
		Size: 7.1 MB (7127800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec841349f8ced4ed21f3bfc7f105713814cb35b0811b93ec29ba59d79f94abe3`  
		Last Modified: Tue, 03 Jun 2025 13:31:35 GMT  
		Size: 156.7 MB (156683026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147790bdc5cc722beb6e6475e3ecb592d9a8b6a2aa0a06969f738f1f118047e`  
		Last Modified: Tue, 03 Jun 2025 13:31:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75706d9bdb4454a8b5e8a927afade509f01dde0a0dd15cbd6dd621962bc2b63`  
		Last Modified: Tue, 03 Jun 2025 13:31:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9297cb454be3bfb83d1be25a36e26e571d91379f464f1f78e2c26cb6b80f11c`  
		Last Modified: Tue, 03 Jun 2025 13:31:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ca170954ac44c9ded2ab1245ffded8a53b48465b0f0afdde712d63692ae2be`  
		Last Modified: Tue, 03 Jun 2025 13:31:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6350e0fff42f552f29b13465836afb26aae82804876da67ba8f173cca0c55b8`  
		Last Modified: Tue, 03 Jun 2025 13:31:17 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.3.42-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f5f4450ab24c67170e5e6ea53247899f99b367124b61cd40475f75c8cc51c0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851417b84955eb5b5ea7f0020fd28abdf49e7b08b6a4b6953292a0e35966bf4f`

```dockerfile
```

-	Layers:
	-	`sha256:8ab0b0448fd4735e24b7ffe6b9280a64ecf1e6669d3571e4e8c76d71ff785474`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 26.1 KB (26086 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4`

```console
$ docker pull clickhouse@sha256:ad201eec325abb23e558e344d46d81bc9e2eba5a011fc02af440c124a27a1a61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:e8705831ea751658a66e7c40fbb13819df49fc13654efa9daf0ceebde4a87366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202712235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d98d8450981ae16b3b9032195f8a95cfc9b1d83831a202da4e5783257fbf15`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db75183102cd447e26ac155a974ed846226f3695c6db557b742f11dfacf1f2c2`  
		Last Modified: Tue, 03 Jun 2025 16:13:59 GMT  
		Size: 7.2 MB (7151686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e343021d0decbeb7ca7aed69d71cf2fff6abdc109539420ef7311ad000c1e4`  
		Last Modified: Tue, 03 Jun 2025 16:14:12 GMT  
		Size: 165.2 MB (165157299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e126fc138f8f2a0fb43764a8992715dc41159afa1a5de6c8082b400de39b2926`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eea866cba85dc8756e04f79927fd55592350d08b96b27a3c770383aa9903d2`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d0918ffa972436db12d329a437bcd647a4a28e3bbd2568e06ae0e6c7098d8`  
		Last Modified: Tue, 03 Jun 2025 13:35:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027db73f7bc3dc7665a19370548ea0ac3c0c20e7302bbb0ceb6b92645c7c5e6a`  
		Last Modified: Tue, 03 Jun 2025 16:14:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1aed4e6f3f36204f3701b71a3a3bcbc4760d5cee7e4fd46922be3867f337768`  
		Last Modified: Tue, 03 Jun 2025 16:14:01 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50bfb050c2fbc26d0f73c94a7a439799638e2e02af0f60ab26c72831dc1bf8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bc07eb7c1232d3d53de59ca78c15eaec13f628dea0e3b7387e6cdcf11680a1`

```dockerfile
```

-	Layers:
	-	`sha256:28dc7046f111fda0f8dd1dd57976b8f3da347652065b1a54a2f39301757f24f5`  
		Last Modified: Sat, 07 Jun 2025 02:44:17 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45ebad3cda4deef061827bb845434fbcec0a7bc11db0580d3865d25c8be6232e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190045903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:398ba20f498fbfb67d329e5fdccb87290c0d673d0acd9d3be3430c084254ac5c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2cff09b21a29489a5754d40a9b08ccc3d9c9a194d8748e096d39e6334d61c`  
		Last Modified: Tue, 03 Jun 2025 16:38:30 GMT  
		Size: 7.1 MB (7127827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaa525398bbd99663d7384f2451213d2debd665b1af761aa9f8846ecd337d8e`  
		Last Modified: Tue, 03 Jun 2025 16:38:42 GMT  
		Size: 154.7 MB (154692243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3599164049e06fd6df4f0d5b59eb6fd10e2061dd1efa09a508a1820e35be63`  
		Last Modified: Tue, 03 Jun 2025 16:38:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf112416afd6b8a5876403d01c7fe72c57abdcee40068eee09c96635f318485a`  
		Last Modified: Tue, 03 Jun 2025 16:38:31 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024e9a7deb846b26454058f620c152458507913353bd071a989bdde2f2af8dcb`  
		Last Modified: Tue, 03 Jun 2025 16:38:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8007d4343374f48e98d88d7c20a822a4d5bf0ef63b239320249b587122be34cc`  
		Last Modified: Tue, 03 Jun 2025 16:38:30 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061f7781258c7c48129eba045aff514e0cdfdf3b437489d674fd75baea525b04`  
		Last Modified: Tue, 03 Jun 2025 16:38:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9b28672270ff8994e9a8cd736c25e9618c2fcca97a7da9af235ad7910132ea67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ec23bbd6a6740a8350c8cba376a3c6f2144b69349d11e04c891c6762b0d6ed`

```dockerfile
```

-	Layers:
	-	`sha256:60502332b35cb0a4c063b5aec824284ee642442b9a01d1cede2dd635fb819f2a`  
		Last Modified: Sat, 07 Jun 2025 02:44:17 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4-jammy`

```console
$ docker pull clickhouse@sha256:ad201eec325abb23e558e344d46d81bc9e2eba5a011fc02af440c124a27a1a61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e8705831ea751658a66e7c40fbb13819df49fc13654efa9daf0ceebde4a87366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **202.7 MB (202712235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37d98d8450981ae16b3b9032195f8a95cfc9b1d83831a202da4e5783257fbf15`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db75183102cd447e26ac155a974ed846226f3695c6db557b742f11dfacf1f2c2`  
		Last Modified: Tue, 03 Jun 2025 16:13:59 GMT  
		Size: 7.2 MB (7151686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e343021d0decbeb7ca7aed69d71cf2fff6abdc109539420ef7311ad000c1e4`  
		Last Modified: Tue, 03 Jun 2025 16:14:12 GMT  
		Size: 165.2 MB (165157299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e126fc138f8f2a0fb43764a8992715dc41159afa1a5de6c8082b400de39b2926`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eea866cba85dc8756e04f79927fd55592350d08b96b27a3c770383aa9903d2`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d0918ffa972436db12d329a437bcd647a4a28e3bbd2568e06ae0e6c7098d8`  
		Last Modified: Tue, 03 Jun 2025 13:35:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027db73f7bc3dc7665a19370548ea0ac3c0c20e7302bbb0ceb6b92645c7c5e6a`  
		Last Modified: Tue, 03 Jun 2025 16:14:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1aed4e6f3f36204f3701b71a3a3bcbc4760d5cee7e4fd46922be3867f337768`  
		Last Modified: Tue, 03 Jun 2025 16:14:01 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50bfb050c2fbc26d0f73c94a7a439799638e2e02af0f60ab26c72831dc1bf8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34bc07eb7c1232d3d53de59ca78c15eaec13f628dea0e3b7387e6cdcf11680a1`

```dockerfile
```

-	Layers:
	-	`sha256:28dc7046f111fda0f8dd1dd57976b8f3da347652065b1a54a2f39301757f24f5`  
		Last Modified: Sat, 07 Jun 2025 02:44:17 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45ebad3cda4deef061827bb845434fbcec0a7bc11db0580d3865d25c8be6232e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (190045903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:398ba20f498fbfb67d329e5fdccb87290c0d673d0acd9d3be3430c084254ac5c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f2cff09b21a29489a5754d40a9b08ccc3d9c9a194d8748e096d39e6334d61c`  
		Last Modified: Tue, 03 Jun 2025 16:38:30 GMT  
		Size: 7.1 MB (7127827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdaa525398bbd99663d7384f2451213d2debd665b1af761aa9f8846ecd337d8e`  
		Last Modified: Tue, 03 Jun 2025 16:38:42 GMT  
		Size: 154.7 MB (154692243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3599164049e06fd6df4f0d5b59eb6fd10e2061dd1efa09a508a1820e35be63`  
		Last Modified: Tue, 03 Jun 2025 16:38:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf112416afd6b8a5876403d01c7fe72c57abdcee40068eee09c96635f318485a`  
		Last Modified: Tue, 03 Jun 2025 16:38:31 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024e9a7deb846b26454058f620c152458507913353bd071a989bdde2f2af8dcb`  
		Last Modified: Tue, 03 Jun 2025 16:38:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8007d4343374f48e98d88d7c20a822a4d5bf0ef63b239320249b587122be34cc`  
		Last Modified: Tue, 03 Jun 2025 16:38:30 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061f7781258c7c48129eba045aff514e0cdfdf3b437489d674fd75baea525b04`  
		Last Modified: Tue, 03 Jun 2025 16:38:30 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9b28672270ff8994e9a8cd736c25e9618c2fcca97a7da9af235ad7910132ea67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51ec23bbd6a6740a8350c8cba376a3c6f2144b69349d11e04c891c6762b0d6ed`

```dockerfile
```

-	Layers:
	-	`sha256:60502332b35cb0a4c063b5aec824284ee642442b9a01d1cede2dd635fb819f2a`  
		Last Modified: Sat, 07 Jun 2025 02:44:17 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.4.7`

**does not exist** (yet?)

## `clickhouse:25.4.7-jammy`

**does not exist** (yet?)

## `clickhouse:25.4.7.66`

**does not exist** (yet?)

## `clickhouse:25.4.7.66-jammy`

**does not exist** (yet?)

## `clickhouse:25.5`

```console
$ docker pull clickhouse@sha256:668cf02c7d67eaafb8f3e4614f7a8d24caf05130acf551616b887401ad89ea8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:4643fe917573fe06f4c8dd4dfadef5d3ebe7151ed4b96f611c61d763e3748ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205992528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e032593a9b1d712a6691d4dd875ee034429aee64aee1378d602f1a05ba54c26`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca18d4ea7ff898eccbdea1b99a52ed6bdaaea18e98a4bf7af4ca5bfaa621ec23`  
		Last Modified: Tue, 03 Jun 2025 13:34:10 GMT  
		Size: 7.2 MB (7151670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48829f4421d0dc1bbbd6afcd428c3faec27c484876b236ac7e8a8c4ee51baf8`  
		Last Modified: Tue, 03 Jun 2025 13:34:21 GMT  
		Size: 168.4 MB (168437610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c811205cc2b9315b293d4e880a8ad4f5754d52b97b914a8f6352f95ea6622eaf`  
		Last Modified: Tue, 03 Jun 2025 13:34:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6534354a8849b34990c5ed5890969dc652fbfa136ab05e4cefab0f590b1d4078`  
		Last Modified: Tue, 03 Jun 2025 13:34:10 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379441ad211fd0d8c6ec812815a3b8606491121410986aae2b00ea51d5044a0c`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f5d8424dd133095c22862d02ae4f4c94fe85e8fce55a80ff81dc361f046852`  
		Last Modified: Tue, 03 Jun 2025 13:34:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944eae3ea89105f619ac2cfb8c646ec888c46cf07833e2ce12e0358eb0837e01`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:02aedb60d80131305dfb8d4b1b8218e2679c1d37d9abf20a1fefd4901f96534c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d838c21a4277e4e8ea3a128d2819b0df050fd16d96ed68af5a11fe8f943c09`

```dockerfile
```

-	Layers:
	-	`sha256:edc7d8f4736b9ae1f52da66199f68cf486442ffe98e72122d2db61909ac143f4`  
		Last Modified: Thu, 05 Jun 2025 10:41:41 GMT  
		Size: 25.9 KB (25899 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d9ddfa0947aecce3ff098371cdfeae355a9b7d08de5eeccdca15d2b37ba8172d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192488684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dedafce23b87a9ea7f6f39756bfc693a5da8c391d2935f2bf98e5d1931c12d1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c5b38a39c18549c81527aeb48892dfc585c974a9a93e66ca884ef8f820e0bb`  
		Last Modified: Tue, 03 Jun 2025 15:48:18 GMT  
		Size: 7.1 MB (7127793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9e8d6308303920e9c697de9ede1387bdd197d6956d6a41ac8842e7bfb5bd75`  
		Last Modified: Tue, 03 Jun 2025 15:48:41 GMT  
		Size: 157.1 MB (157135063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c044a90340fc36e81cc8e57c8142c9c4c66b59009d6db03191c5164689db72`  
		Last Modified: Tue, 03 Jun 2025 15:48:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337c3a68ef15e5229ad768ec84c430df2eeea6f52d92a20a184feac13be30294`  
		Last Modified: Tue, 03 Jun 2025 15:48:15 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376439689a943599fdeba7d8d47b32eb05623a1a107d3d581a024b2667b427de`  
		Last Modified: Tue, 03 Jun 2025 15:48:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ae75e427a60ab183d457bb0286429b0156fde1596cf3cfa4cffaab4e866f02`  
		Last Modified: Tue, 03 Jun 2025 15:48:17 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bdb5196123393dcbeae3363eea4352814819c479b7bea9f0c824b8b7ac96ab`  
		Last Modified: Tue, 03 Jun 2025 15:48:15 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f4ab474a83ef83d13412e1c671e86e3ece02eefedf10ef94cde070bf4fcdef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e24c0ce6ab07378dc1724d7f5a76f1233cc852b02d6941a6aa8ccc14cfdb383`

```dockerfile
```

-	Layers:
	-	`sha256:a3df743e65c02fd92d1afe55481b59d7a2399accd6e3c326d22f2b3ce101c60f`  
		Last Modified: Thu, 05 Jun 2025 10:41:42 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5-jammy`

```console
$ docker pull clickhouse@sha256:668cf02c7d67eaafb8f3e4614f7a8d24caf05130acf551616b887401ad89ea8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:4643fe917573fe06f4c8dd4dfadef5d3ebe7151ed4b96f611c61d763e3748ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205992528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e032593a9b1d712a6691d4dd875ee034429aee64aee1378d602f1a05ba54c26`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca18d4ea7ff898eccbdea1b99a52ed6bdaaea18e98a4bf7af4ca5bfaa621ec23`  
		Last Modified: Tue, 03 Jun 2025 13:34:10 GMT  
		Size: 7.2 MB (7151670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48829f4421d0dc1bbbd6afcd428c3faec27c484876b236ac7e8a8c4ee51baf8`  
		Last Modified: Tue, 03 Jun 2025 13:34:21 GMT  
		Size: 168.4 MB (168437610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c811205cc2b9315b293d4e880a8ad4f5754d52b97b914a8f6352f95ea6622eaf`  
		Last Modified: Tue, 03 Jun 2025 13:34:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6534354a8849b34990c5ed5890969dc652fbfa136ab05e4cefab0f590b1d4078`  
		Last Modified: Tue, 03 Jun 2025 13:34:10 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379441ad211fd0d8c6ec812815a3b8606491121410986aae2b00ea51d5044a0c`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f5d8424dd133095c22862d02ae4f4c94fe85e8fce55a80ff81dc361f046852`  
		Last Modified: Tue, 03 Jun 2025 13:34:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944eae3ea89105f619ac2cfb8c646ec888c46cf07833e2ce12e0358eb0837e01`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:02aedb60d80131305dfb8d4b1b8218e2679c1d37d9abf20a1fefd4901f96534c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d838c21a4277e4e8ea3a128d2819b0df050fd16d96ed68af5a11fe8f943c09`

```dockerfile
```

-	Layers:
	-	`sha256:edc7d8f4736b9ae1f52da66199f68cf486442ffe98e72122d2db61909ac143f4`  
		Last Modified: Thu, 05 Jun 2025 10:41:41 GMT  
		Size: 25.9 KB (25899 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d9ddfa0947aecce3ff098371cdfeae355a9b7d08de5eeccdca15d2b37ba8172d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192488684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dedafce23b87a9ea7f6f39756bfc693a5da8c391d2935f2bf98e5d1931c12d1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c5b38a39c18549c81527aeb48892dfc585c974a9a93e66ca884ef8f820e0bb`  
		Last Modified: Tue, 03 Jun 2025 15:48:18 GMT  
		Size: 7.1 MB (7127793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9e8d6308303920e9c697de9ede1387bdd197d6956d6a41ac8842e7bfb5bd75`  
		Last Modified: Tue, 03 Jun 2025 15:48:41 GMT  
		Size: 157.1 MB (157135063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c044a90340fc36e81cc8e57c8142c9c4c66b59009d6db03191c5164689db72`  
		Last Modified: Tue, 03 Jun 2025 15:48:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337c3a68ef15e5229ad768ec84c430df2eeea6f52d92a20a184feac13be30294`  
		Last Modified: Tue, 03 Jun 2025 15:48:15 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376439689a943599fdeba7d8d47b32eb05623a1a107d3d581a024b2667b427de`  
		Last Modified: Tue, 03 Jun 2025 15:48:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ae75e427a60ab183d457bb0286429b0156fde1596cf3cfa4cffaab4e866f02`  
		Last Modified: Tue, 03 Jun 2025 15:48:17 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bdb5196123393dcbeae3363eea4352814819c479b7bea9f0c824b8b7ac96ab`  
		Last Modified: Tue, 03 Jun 2025 15:48:15 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f4ab474a83ef83d13412e1c671e86e3ece02eefedf10ef94cde070bf4fcdef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e24c0ce6ab07378dc1724d7f5a76f1233cc852b02d6941a6aa8ccc14cfdb383`

```dockerfile
```

-	Layers:
	-	`sha256:a3df743e65c02fd92d1afe55481b59d7a2399accd6e3c326d22f2b3ce101c60f`  
		Last Modified: Thu, 05 Jun 2025 10:41:42 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.5.3`

**does not exist** (yet?)

## `clickhouse:25.5.3-jammy`

**does not exist** (yet?)

## `clickhouse:25.5.3.75`

**does not exist** (yet?)

## `clickhouse:25.5.3.75-jammy`

**does not exist** (yet?)

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:668cf02c7d67eaafb8f3e4614f7a8d24caf05130acf551616b887401ad89ea8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:4643fe917573fe06f4c8dd4dfadef5d3ebe7151ed4b96f611c61d763e3748ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205992528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e032593a9b1d712a6691d4dd875ee034429aee64aee1378d602f1a05ba54c26`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca18d4ea7ff898eccbdea1b99a52ed6bdaaea18e98a4bf7af4ca5bfaa621ec23`  
		Last Modified: Tue, 03 Jun 2025 13:34:10 GMT  
		Size: 7.2 MB (7151670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48829f4421d0dc1bbbd6afcd428c3faec27c484876b236ac7e8a8c4ee51baf8`  
		Last Modified: Tue, 03 Jun 2025 13:34:21 GMT  
		Size: 168.4 MB (168437610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c811205cc2b9315b293d4e880a8ad4f5754d52b97b914a8f6352f95ea6622eaf`  
		Last Modified: Tue, 03 Jun 2025 13:34:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6534354a8849b34990c5ed5890969dc652fbfa136ab05e4cefab0f590b1d4078`  
		Last Modified: Tue, 03 Jun 2025 13:34:10 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379441ad211fd0d8c6ec812815a3b8606491121410986aae2b00ea51d5044a0c`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f5d8424dd133095c22862d02ae4f4c94fe85e8fce55a80ff81dc361f046852`  
		Last Modified: Tue, 03 Jun 2025 13:34:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944eae3ea89105f619ac2cfb8c646ec888c46cf07833e2ce12e0358eb0837e01`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:02aedb60d80131305dfb8d4b1b8218e2679c1d37d9abf20a1fefd4901f96534c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d838c21a4277e4e8ea3a128d2819b0df050fd16d96ed68af5a11fe8f943c09`

```dockerfile
```

-	Layers:
	-	`sha256:edc7d8f4736b9ae1f52da66199f68cf486442ffe98e72122d2db61909ac143f4`  
		Last Modified: Thu, 05 Jun 2025 10:41:41 GMT  
		Size: 25.9 KB (25899 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d9ddfa0947aecce3ff098371cdfeae355a9b7d08de5eeccdca15d2b37ba8172d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192488684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dedafce23b87a9ea7f6f39756bfc693a5da8c391d2935f2bf98e5d1931c12d1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c5b38a39c18549c81527aeb48892dfc585c974a9a93e66ca884ef8f820e0bb`  
		Last Modified: Tue, 03 Jun 2025 15:48:18 GMT  
		Size: 7.1 MB (7127793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9e8d6308303920e9c697de9ede1387bdd197d6956d6a41ac8842e7bfb5bd75`  
		Last Modified: Tue, 03 Jun 2025 15:48:41 GMT  
		Size: 157.1 MB (157135063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c044a90340fc36e81cc8e57c8142c9c4c66b59009d6db03191c5164689db72`  
		Last Modified: Tue, 03 Jun 2025 15:48:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337c3a68ef15e5229ad768ec84c430df2eeea6f52d92a20a184feac13be30294`  
		Last Modified: Tue, 03 Jun 2025 15:48:15 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376439689a943599fdeba7d8d47b32eb05623a1a107d3d581a024b2667b427de`  
		Last Modified: Tue, 03 Jun 2025 15:48:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ae75e427a60ab183d457bb0286429b0156fde1596cf3cfa4cffaab4e866f02`  
		Last Modified: Tue, 03 Jun 2025 15:48:17 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bdb5196123393dcbeae3363eea4352814819c479b7bea9f0c824b8b7ac96ab`  
		Last Modified: Tue, 03 Jun 2025 15:48:15 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f4ab474a83ef83d13412e1c671e86e3ece02eefedf10ef94cde070bf4fcdef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e24c0ce6ab07378dc1724d7f5a76f1233cc852b02d6941a6aa8ccc14cfdb383`

```dockerfile
```

-	Layers:
	-	`sha256:a3df743e65c02fd92d1afe55481b59d7a2399accd6e3c326d22f2b3ce101c60f`  
		Last Modified: Thu, 05 Jun 2025 10:41:42 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:668cf02c7d67eaafb8f3e4614f7a8d24caf05130acf551616b887401ad89ea8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:4643fe917573fe06f4c8dd4dfadef5d3ebe7151ed4b96f611c61d763e3748ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.0 MB (205992528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e032593a9b1d712a6691d4dd875ee034429aee64aee1378d602f1a05ba54c26`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca18d4ea7ff898eccbdea1b99a52ed6bdaaea18e98a4bf7af4ca5bfaa621ec23`  
		Last Modified: Tue, 03 Jun 2025 13:34:10 GMT  
		Size: 7.2 MB (7151670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e48829f4421d0dc1bbbd6afcd428c3faec27c484876b236ac7e8a8c4ee51baf8`  
		Last Modified: Tue, 03 Jun 2025 13:34:21 GMT  
		Size: 168.4 MB (168437610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c811205cc2b9315b293d4e880a8ad4f5754d52b97b914a8f6352f95ea6622eaf`  
		Last Modified: Tue, 03 Jun 2025 13:34:09 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6534354a8849b34990c5ed5890969dc652fbfa136ab05e4cefab0f590b1d4078`  
		Last Modified: Tue, 03 Jun 2025 13:34:10 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379441ad211fd0d8c6ec812815a3b8606491121410986aae2b00ea51d5044a0c`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f5d8424dd133095c22862d02ae4f4c94fe85e8fce55a80ff81dc361f046852`  
		Last Modified: Tue, 03 Jun 2025 13:34:12 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:944eae3ea89105f619ac2cfb8c646ec888c46cf07833e2ce12e0358eb0837e01`  
		Last Modified: Tue, 03 Jun 2025 13:34:11 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:02aedb60d80131305dfb8d4b1b8218e2679c1d37d9abf20a1fefd4901f96534c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d838c21a4277e4e8ea3a128d2819b0df050fd16d96ed68af5a11fe8f943c09`

```dockerfile
```

-	Layers:
	-	`sha256:edc7d8f4736b9ae1f52da66199f68cf486442ffe98e72122d2db61909ac143f4`  
		Last Modified: Thu, 05 Jun 2025 10:41:41 GMT  
		Size: 25.9 KB (25899 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:d9ddfa0947aecce3ff098371cdfeae355a9b7d08de5eeccdca15d2b37ba8172d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.5 MB (192488684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dedafce23b87a9ea7f6f39756bfc693a5da8c391d2935f2bf98e5d1931c12d1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78c5b38a39c18549c81527aeb48892dfc585c974a9a93e66ca884ef8f820e0bb`  
		Last Modified: Tue, 03 Jun 2025 15:48:18 GMT  
		Size: 7.1 MB (7127793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a9e8d6308303920e9c697de9ede1387bdd197d6956d6a41ac8842e7bfb5bd75`  
		Last Modified: Tue, 03 Jun 2025 15:48:41 GMT  
		Size: 157.1 MB (157135063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c044a90340fc36e81cc8e57c8142c9c4c66b59009d6db03191c5164689db72`  
		Last Modified: Tue, 03 Jun 2025 15:48:15 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337c3a68ef15e5229ad768ec84c430df2eeea6f52d92a20a184feac13be30294`  
		Last Modified: Tue, 03 Jun 2025 15:48:15 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376439689a943599fdeba7d8d47b32eb05623a1a107d3d581a024b2667b427de`  
		Last Modified: Tue, 03 Jun 2025 15:48:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ae75e427a60ab183d457bb0286429b0156fde1596cf3cfa4cffaab4e866f02`  
		Last Modified: Tue, 03 Jun 2025 15:48:17 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bdb5196123393dcbeae3363eea4352814819c479b7bea9f0c824b8b7ac96ab`  
		Last Modified: Tue, 03 Jun 2025 15:48:15 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8f4ab474a83ef83d13412e1c671e86e3ece02eefedf10ef94cde070bf4fcdef2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e24c0ce6ab07378dc1724d7f5a76f1233cc852b02d6941a6aa8ccc14cfdb383`

```dockerfile
```

-	Layers:
	-	`sha256:a3df743e65c02fd92d1afe55481b59d7a2399accd6e3c326d22f2b3ce101c60f`  
		Last Modified: Thu, 05 Jun 2025 10:41:42 GMT  
		Size: 26.1 KB (26111 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:a13b72e1ccf25aef8be2e4f1aebfed42a348ca963ecf3fa833669c3b440b9f15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:3642182a619cec92e3d796525e5e7324f533a11ca460eeadcd9cb2fcb2599809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710b81e76d9f3be348143654072f49b51aefd55f6456b10204d1c9d1547a4ce7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
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
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1164d17c203def662aa15fa7537b0c471e391a406322ea048fc04ce7049e3c`  
		Last Modified: Tue, 03 Jun 2025 13:35:50 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9942f24a20ba860cdcabc61c00fad11a6e1175d95231af361420459328ce7`  
		Last Modified: Tue, 03 Jun 2025 13:36:06 GMT  
		Size: 167.0 MB (166978781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e126fc138f8f2a0fb43764a8992715dc41159afa1a5de6c8082b400de39b2926`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eea866cba85dc8756e04f79927fd55592350d08b96b27a3c770383aa9903d2`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d0918ffa972436db12d329a437bcd647a4a28e3bbd2568e06ae0e6c7098d8`  
		Last Modified: Tue, 03 Jun 2025 13:35:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263c331f3d7ad8bfbf09c052ef8f93e8e10ca419c3d5b37fde68cdcdfeb0910`  
		Last Modified: Tue, 03 Jun 2025 13:35:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a10302743efc73ef39922a2eaed3f6046e29820028151c06f37b875f4966ae1`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a1871b03ebda7524b20dbe45b0fb8c17e3e28c8b648700ee4c8fcc556e886611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5084401e3632c3b300d60fbb95b1248320dc5ff262d9864e4e37bb42493b8b4`

```dockerfile
```

-	Layers:
	-	`sha256:4fb376b0725185667bf473b112fbfd93df7c33f3f53904103450d279cef15619`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:97f5119c9be0aeed23b93f06162ac401eceb4b5f36276f6b46dfc99c8064f210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192036654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaa1a1ac10e1650228fe42d49b26d8ca3140669507795ddda87bf3bde3be4b6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
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
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230b813b118aa053f351c3a882051f13c87cbc0aa9093eab452d39e8521bb180`  
		Last Modified: Tue, 03 Jun 2025 13:31:07 GMT  
		Size: 7.1 MB (7127800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec841349f8ced4ed21f3bfc7f105713814cb35b0811b93ec29ba59d79f94abe3`  
		Last Modified: Tue, 03 Jun 2025 13:31:35 GMT  
		Size: 156.7 MB (156683026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147790bdc5cc722beb6e6475e3ecb592d9a8b6a2aa0a06969f738f1f118047e`  
		Last Modified: Tue, 03 Jun 2025 13:31:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75706d9bdb4454a8b5e8a927afade509f01dde0a0dd15cbd6dd621962bc2b63`  
		Last Modified: Tue, 03 Jun 2025 13:31:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9297cb454be3bfb83d1be25a36e26e571d91379f464f1f78e2c26cb6b80f11c`  
		Last Modified: Tue, 03 Jun 2025 13:31:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ca170954ac44c9ded2ab1245ffded8a53b48465b0f0afdde712d63692ae2be`  
		Last Modified: Tue, 03 Jun 2025 13:31:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6350e0fff42f552f29b13465836afb26aae82804876da67ba8f173cca0c55b8`  
		Last Modified: Tue, 03 Jun 2025 13:31:17 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f5f4450ab24c67170e5e6ea53247899f99b367124b61cd40475f75c8cc51c0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851417b84955eb5b5ea7f0020fd28abdf49e7b08b6a4b6953292a0e35966bf4f`

```dockerfile
```

-	Layers:
	-	`sha256:8ab0b0448fd4735e24b7ffe6b9280a64ecf1e6669d3571e4e8c76d71ff785474`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 26.1 KB (26086 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:a13b72e1ccf25aef8be2e4f1aebfed42a348ca963ecf3fa833669c3b440b9f15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:3642182a619cec92e3d796525e5e7324f533a11ca460eeadcd9cb2fcb2599809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204533718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710b81e76d9f3be348143654072f49b51aefd55f6456b10204d1c9d1547a4ce7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:82f38ebced7b2756311fb492d3d44cc131b22654e8620baa93883537a3e355aa in / 
# Fri, 23 May 2025 11:00:13 GMT
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
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:89dc6ea4eae2b38a3550534ece4983005a7d2e90e4fa503ed04dcfc58ee71159`  
		Last Modified: Tue, 03 Jun 2025 13:30:14 GMT  
		Size: 29.5 MB (29533003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1164d17c203def662aa15fa7537b0c471e391a406322ea048fc04ce7049e3c`  
		Last Modified: Tue, 03 Jun 2025 13:35:50 GMT  
		Size: 7.2 MB (7151687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9942f24a20ba860cdcabc61c00fad11a6e1175d95231af361420459328ce7`  
		Last Modified: Tue, 03 Jun 2025 13:36:06 GMT  
		Size: 167.0 MB (166978781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e126fc138f8f2a0fb43764a8992715dc41159afa1a5de6c8082b400de39b2926`  
		Last Modified: Tue, 03 Jun 2025 13:35:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65eea866cba85dc8756e04f79927fd55592350d08b96b27a3c770383aa9903d2`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7d0918ffa972436db12d329a437bcd647a4a28e3bbd2568e06ae0e6c7098d8`  
		Last Modified: Tue, 03 Jun 2025 13:35:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7263c331f3d7ad8bfbf09c052ef8f93e8e10ca419c3d5b37fde68cdcdfeb0910`  
		Last Modified: Tue, 03 Jun 2025 13:35:55 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a10302743efc73ef39922a2eaed3f6046e29820028151c06f37b875f4966ae1`  
		Last Modified: Tue, 03 Jun 2025 13:35:57 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a1871b03ebda7524b20dbe45b0fb8c17e3e28c8b648700ee4c8fcc556e886611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5084401e3632c3b300d60fbb95b1248320dc5ff262d9864e4e37bb42493b8b4`

```dockerfile
```

-	Layers:
	-	`sha256:4fb376b0725185667bf473b112fbfd93df7c33f3f53904103450d279cef15619`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:97f5119c9be0aeed23b93f06162ac401eceb4b5f36276f6b46dfc99c8064f210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192036654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eaa1a1ac10e1650228fe42d49b26d8ca3140669507795ddda87bf3bde3be4b6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 23 May 2025 11:00:13 GMT
ARG RELEASE
# Fri, 23 May 2025 11:00:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 23 May 2025 11:00:13 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 23 May 2025 11:00:13 GMT
ADD file:7adcd25cfa0f5393043ae51833e5654ddd86b0c9fe24cfdacf535c1c2c516c7a in / 
# Fri, 23 May 2025 11:00:13 GMT
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
ARG VERSION=25.3.3.42
# Fri, 23 May 2025 11:00:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 23 May 2025 11:00:13 GMT
ENV LANG=en_US.UTF-8
# Fri, 23 May 2025 11:00:13 GMT
ENV TZ=UTC
# Fri, 23 May 2025 11:00:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.3.42 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0e25612b6db22df273732c47faba1dd81735a0dd9f6ea27b5222f281d67409f5`  
		Last Modified: Tue, 03 Jun 2025 13:30:17 GMT  
		Size: 27.4 MB (27355581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230b813b118aa053f351c3a882051f13c87cbc0aa9093eab452d39e8521bb180`  
		Last Modified: Tue, 03 Jun 2025 13:31:07 GMT  
		Size: 7.1 MB (7127800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec841349f8ced4ed21f3bfc7f105713814cb35b0811b93ec29ba59d79f94abe3`  
		Last Modified: Tue, 03 Jun 2025 13:31:35 GMT  
		Size: 156.7 MB (156683026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a147790bdc5cc722beb6e6475e3ecb592d9a8b6a2aa0a06969f738f1f118047e`  
		Last Modified: Tue, 03 Jun 2025 13:31:10 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75706d9bdb4454a8b5e8a927afade509f01dde0a0dd15cbd6dd621962bc2b63`  
		Last Modified: Tue, 03 Jun 2025 13:31:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9297cb454be3bfb83d1be25a36e26e571d91379f464f1f78e2c26cb6b80f11c`  
		Last Modified: Tue, 03 Jun 2025 13:31:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ca170954ac44c9ded2ab1245ffded8a53b48465b0f0afdde712d63692ae2be`  
		Last Modified: Tue, 03 Jun 2025 13:31:16 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6350e0fff42f552f29b13465836afb26aae82804876da67ba8f173cca0c55b8`  
		Last Modified: Tue, 03 Jun 2025 13:31:17 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f5f4450ab24c67170e5e6ea53247899f99b367124b61cd40475f75c8cc51c0f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851417b84955eb5b5ea7f0020fd28abdf49e7b08b6a4b6953292a0e35966bf4f`

```dockerfile
```

-	Layers:
	-	`sha256:8ab0b0448fd4735e24b7ffe6b9280a64ecf1e6669d3571e4e8c76d71ff785474`  
		Last Modified: Sat, 07 Jun 2025 02:46:32 GMT  
		Size: 26.1 KB (26086 bytes)  
		MIME: application/vnd.in-toto+json
