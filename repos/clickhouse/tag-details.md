<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:24.8`](#clickhouse248)
-	[`clickhouse:24.8-focal`](#clickhouse248-focal)
-	[`clickhouse:24.8.14`](#clickhouse24814)
-	[`clickhouse:24.8.14-focal`](#clickhouse24814-focal)
-	[`clickhouse:24.8.14.39`](#clickhouse2481439)
-	[`clickhouse:24.8.14.39-focal`](#clickhouse2481439-focal)
-	[`clickhouse:25.1`](#clickhouse251)
-	[`clickhouse:25.1-jammy`](#clickhouse251-jammy)
-	[`clickhouse:25.1.8`](#clickhouse2518)
-	[`clickhouse:25.1.8-jammy`](#clickhouse2518-jammy)
-	[`clickhouse:25.1.8.25`](#clickhouse251825)
-	[`clickhouse:25.1.8.25-jammy`](#clickhouse251825-jammy)
-	[`clickhouse:25.2`](#clickhouse252)
-	[`clickhouse:25.2-jammy`](#clickhouse252-jammy)
-	[`clickhouse:25.2.2`](#clickhouse2522)
-	[`clickhouse:25.2.2-jammy`](#clickhouse2522-jammy)
-	[`clickhouse:25.2.2.39`](#clickhouse252239)
-	[`clickhouse:25.2.2.39-jammy`](#clickhouse252239-jammy)
-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.2`](#clickhouse2532)
-	[`clickhouse:25.3.2-jammy`](#clickhouse2532-jammy)
-	[`clickhouse:25.3.2.39`](#clickhouse253239)
-	[`clickhouse:25.3.2.39-jammy`](#clickhouse253239-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:24.8`

```console
$ docker pull clickhouse@sha256:5053d2db241c823b7296091aad759bd073b203a63119e8aca7c94d8fd30ed6df
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
$ docker pull clickhouse@sha256:6b1c19acc3471ecc4122833aad9233849418148a479767b70a17ac3a6f5a5e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172247400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7826c9d62c0108c9acd420fcf75168e55956a8c6f94f9afd474a4ac6c5945ad5`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 00:30:57 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a5152bf61aba465be8a8c1591d22dc90016092c1beaad31bbf52908c408216da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9305a4dfd3d84f94d4cb11df80e780a9f8082c8adc53eddcfb78b2156a5c3d`

```dockerfile
```

-	Layers:
	-	`sha256:2dcbd159b26d5da9e1a79dbfbb14a09eb0752aefa8dc2601f6460fb2eef72169`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8-focal`

```console
$ docker pull clickhouse@sha256:5053d2db241c823b7296091aad759bd073b203a63119e8aca7c94d8fd30ed6df
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
$ docker pull clickhouse@sha256:6b1c19acc3471ecc4122833aad9233849418148a479767b70a17ac3a6f5a5e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172247400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7826c9d62c0108c9acd420fcf75168e55956a8c6f94f9afd474a4ac6c5945ad5`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 00:30:57 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a5152bf61aba465be8a8c1591d22dc90016092c1beaad31bbf52908c408216da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9305a4dfd3d84f94d4cb11df80e780a9f8082c8adc53eddcfb78b2156a5c3d`

```dockerfile
```

-	Layers:
	-	`sha256:2dcbd159b26d5da9e1a79dbfbb14a09eb0752aefa8dc2601f6460fb2eef72169`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.14`

```console
$ docker pull clickhouse@sha256:5053d2db241c823b7296091aad759bd073b203a63119e8aca7c94d8fd30ed6df
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
$ docker pull clickhouse@sha256:6b1c19acc3471ecc4122833aad9233849418148a479767b70a17ac3a6f5a5e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172247400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7826c9d62c0108c9acd420fcf75168e55956a8c6f94f9afd474a4ac6c5945ad5`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 00:30:57 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a5152bf61aba465be8a8c1591d22dc90016092c1beaad31bbf52908c408216da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9305a4dfd3d84f94d4cb11df80e780a9f8082c8adc53eddcfb78b2156a5c3d`

```dockerfile
```

-	Layers:
	-	`sha256:2dcbd159b26d5da9e1a79dbfbb14a09eb0752aefa8dc2601f6460fb2eef72169`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.14-focal`

```console
$ docker pull clickhouse@sha256:5053d2db241c823b7296091aad759bd073b203a63119e8aca7c94d8fd30ed6df
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
$ docker pull clickhouse@sha256:6b1c19acc3471ecc4122833aad9233849418148a479767b70a17ac3a6f5a5e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172247400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7826c9d62c0108c9acd420fcf75168e55956a8c6f94f9afd474a4ac6c5945ad5`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 00:30:57 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a5152bf61aba465be8a8c1591d22dc90016092c1beaad31bbf52908c408216da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9305a4dfd3d84f94d4cb11df80e780a9f8082c8adc53eddcfb78b2156a5c3d`

```dockerfile
```

-	Layers:
	-	`sha256:2dcbd159b26d5da9e1a79dbfbb14a09eb0752aefa8dc2601f6460fb2eef72169`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.14.39`

```console
$ docker pull clickhouse@sha256:5053d2db241c823b7296091aad759bd073b203a63119e8aca7c94d8fd30ed6df
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
$ docker pull clickhouse@sha256:6b1c19acc3471ecc4122833aad9233849418148a479767b70a17ac3a6f5a5e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172247400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7826c9d62c0108c9acd420fcf75168e55956a8c6f94f9afd474a4ac6c5945ad5`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 00:30:57 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14.39` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a5152bf61aba465be8a8c1591d22dc90016092c1beaad31bbf52908c408216da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9305a4dfd3d84f94d4cb11df80e780a9f8082c8adc53eddcfb78b2156a5c3d`

```dockerfile
```

-	Layers:
	-	`sha256:2dcbd159b26d5da9e1a79dbfbb14a09eb0752aefa8dc2601f6460fb2eef72169`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.14.39-focal`

```console
$ docker pull clickhouse@sha256:5053d2db241c823b7296091aad759bd073b203a63119e8aca7c94d8fd30ed6df
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
$ docker pull clickhouse@sha256:6b1c19acc3471ecc4122833aad9233849418148a479767b70a17ac3a6f5a5e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.2 MB (172247400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7826c9d62c0108c9acd420fcf75168e55956a8c6f94f9afd474a4ac6c5945ad5`
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
# Thu, 20 Feb 2025 13:03:00 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 20 Feb 2025 13:03:00 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPO_CHANNEL=stable
# Thu, 20 Feb 2025 13:03:00 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 20 Feb 2025 13:03:00 GMT
ARG VERSION=24.8.14.39
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.8.14.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 20 Feb 2025 13:03:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 20 Feb 2025 13:03:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 20 Feb 2025 13:03:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:1b9f3c55f9d4aa5c52eb67a4cb7d0f4726ab85a413b50e3e3fe788befce3d297`  
		Last Modified: Fri, 11 Oct 2024 04:41:30 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 00:30:57 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:30:54 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14.39-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a5152bf61aba465be8a8c1591d22dc90016092c1beaad31bbf52908c408216da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b9305a4dfd3d84f94d4cb11df80e780a9f8082c8adc53eddcfb78b2156a5c3d`

```dockerfile
```

-	Layers:
	-	`sha256:2dcbd159b26d5da9e1a79dbfbb14a09eb0752aefa8dc2601f6460fb2eef72169`  
		Last Modified: Fri, 21 Feb 2025 00:30:53 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1`

```console
$ docker pull clickhouse@sha256:a6d159679b55ab169ae347e4bd46ea326776cdb9c2cb9c7b68cd265b68d48ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:7b0a517fcd0807dad4250971456a98f66aa56543c60c25ee78ededcc2267548c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191116985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1a596952af9f3ed57d947a9521f10500e43f1cd325951e39b4987809f2d81b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.1.8.25
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace14fd0dc506feb5687249d3d2e9678b343ace61c0562988f4b5cadd3199edc`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 7.2 MB (7151699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7781a934857b72e38639e0483c40e1ef2d4834f512bab38cb77302735cf310ad`  
		Last Modified: Wed, 09 Apr 2025 01:12:16 GMT  
		Size: 153.6 MB (153562678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e41820ab00ee5f42c1ab52d541c04abf64d2ad2719aacf452147ec1f31113ea`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b5304b74e3ea0a14f52327e1f9836746da4efb32cb92a74780adfb06732bd7`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a2d55d83415ccbd6a94141c706be66c88c0bb38ee158e027264b45e1411521`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1d989071e1018032c9561fa02b8de3216cbd14b93575067154ce473071767c`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e6d19061d46eb23898fe3e0b3bd5b5dcc899b4026774b630399f6de28a8c7e`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:cac0acd7b09f87e74209a2e4258bc99eea8389a5419d85d936b139d187ddb62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0696ca167162e87f5605a050f92fbc9b932421488fe2d6906b0d9fd84f62ec06`

```dockerfile
```

-	Layers:
	-	`sha256:085ee510c98c99b71b07caf443e51291c1a4295b831d15a24ebbe804fd759f13`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b57470c31395773af07839352bd21f0e60f4d439d83d4dca99061d2c15b8234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181587499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b264701335327689e9952fe111e2f38405d3accccd17f98c035884cd1d4d4b23`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994a6684f3864e36c1023cd8b8c7f55d49a5a2b83843f3c63fdc62d4f74104b8`  
		Last Modified: Wed, 19 Mar 2025 00:41:44 GMT  
		Size: 146.2 MB (146237931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9ed303f69d6af2c83b1c0d459480b0317fea0ea99d58fc64065eda060d0814`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc17d0878a6dc84710c44a60d77af52e058f61698e2893fe2e9d87d9c3e50c`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d730573fa6257d4691d0966798f477537a5ef6eb4dc04929e030418fc421a5`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b7fe09ccdad340a138a3535ccd397565c3e42bd3a9449a7e6aba340dfa4638`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5967c09213d5e28f003439a659208ff9c27290d3b5c3be36ee81ea678a766452`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e409ed82226be54e26f06b4584011c03259d4fbfa4be7e06215ed50fee56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19a653309824ada5498999558631c1e7446cccccf717e46775680ebd90d9337`

```dockerfile
```

-	Layers:
	-	`sha256:831088a90410b9d6d70276807b3a7fb58f5038275794386776139bdb20355d3a`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1-jammy`

```console
$ docker pull clickhouse@sha256:a6d159679b55ab169ae347e4bd46ea326776cdb9c2cb9c7b68cd265b68d48ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:7b0a517fcd0807dad4250971456a98f66aa56543c60c25ee78ededcc2267548c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191116985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1a596952af9f3ed57d947a9521f10500e43f1cd325951e39b4987809f2d81b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.1.8.25
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace14fd0dc506feb5687249d3d2e9678b343ace61c0562988f4b5cadd3199edc`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 7.2 MB (7151699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7781a934857b72e38639e0483c40e1ef2d4834f512bab38cb77302735cf310ad`  
		Last Modified: Wed, 09 Apr 2025 01:12:16 GMT  
		Size: 153.6 MB (153562678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e41820ab00ee5f42c1ab52d541c04abf64d2ad2719aacf452147ec1f31113ea`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b5304b74e3ea0a14f52327e1f9836746da4efb32cb92a74780adfb06732bd7`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a2d55d83415ccbd6a94141c706be66c88c0bb38ee158e027264b45e1411521`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1d989071e1018032c9561fa02b8de3216cbd14b93575067154ce473071767c`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e6d19061d46eb23898fe3e0b3bd5b5dcc899b4026774b630399f6de28a8c7e`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:cac0acd7b09f87e74209a2e4258bc99eea8389a5419d85d936b139d187ddb62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0696ca167162e87f5605a050f92fbc9b932421488fe2d6906b0d9fd84f62ec06`

```dockerfile
```

-	Layers:
	-	`sha256:085ee510c98c99b71b07caf443e51291c1a4295b831d15a24ebbe804fd759f13`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b57470c31395773af07839352bd21f0e60f4d439d83d4dca99061d2c15b8234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181587499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b264701335327689e9952fe111e2f38405d3accccd17f98c035884cd1d4d4b23`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994a6684f3864e36c1023cd8b8c7f55d49a5a2b83843f3c63fdc62d4f74104b8`  
		Last Modified: Wed, 19 Mar 2025 00:41:44 GMT  
		Size: 146.2 MB (146237931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9ed303f69d6af2c83b1c0d459480b0317fea0ea99d58fc64065eda060d0814`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc17d0878a6dc84710c44a60d77af52e058f61698e2893fe2e9d87d9c3e50c`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d730573fa6257d4691d0966798f477537a5ef6eb4dc04929e030418fc421a5`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b7fe09ccdad340a138a3535ccd397565c3e42bd3a9449a7e6aba340dfa4638`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5967c09213d5e28f003439a659208ff9c27290d3b5c3be36ee81ea678a766452`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e409ed82226be54e26f06b4584011c03259d4fbfa4be7e06215ed50fee56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19a653309824ada5498999558631c1e7446cccccf717e46775680ebd90d9337`

```dockerfile
```

-	Layers:
	-	`sha256:831088a90410b9d6d70276807b3a7fb58f5038275794386776139bdb20355d3a`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1.8`

```console
$ docker pull clickhouse@sha256:a6d159679b55ab169ae347e4bd46ea326776cdb9c2cb9c7b68cd265b68d48ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:7b0a517fcd0807dad4250971456a98f66aa56543c60c25ee78ededcc2267548c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191116985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1a596952af9f3ed57d947a9521f10500e43f1cd325951e39b4987809f2d81b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.1.8.25
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace14fd0dc506feb5687249d3d2e9678b343ace61c0562988f4b5cadd3199edc`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 7.2 MB (7151699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7781a934857b72e38639e0483c40e1ef2d4834f512bab38cb77302735cf310ad`  
		Last Modified: Wed, 09 Apr 2025 01:12:16 GMT  
		Size: 153.6 MB (153562678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e41820ab00ee5f42c1ab52d541c04abf64d2ad2719aacf452147ec1f31113ea`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b5304b74e3ea0a14f52327e1f9836746da4efb32cb92a74780adfb06732bd7`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a2d55d83415ccbd6a94141c706be66c88c0bb38ee158e027264b45e1411521`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1d989071e1018032c9561fa02b8de3216cbd14b93575067154ce473071767c`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e6d19061d46eb23898fe3e0b3bd5b5dcc899b4026774b630399f6de28a8c7e`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:cac0acd7b09f87e74209a2e4258bc99eea8389a5419d85d936b139d187ddb62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0696ca167162e87f5605a050f92fbc9b932421488fe2d6906b0d9fd84f62ec06`

```dockerfile
```

-	Layers:
	-	`sha256:085ee510c98c99b71b07caf443e51291c1a4295b831d15a24ebbe804fd759f13`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b57470c31395773af07839352bd21f0e60f4d439d83d4dca99061d2c15b8234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181587499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b264701335327689e9952fe111e2f38405d3accccd17f98c035884cd1d4d4b23`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994a6684f3864e36c1023cd8b8c7f55d49a5a2b83843f3c63fdc62d4f74104b8`  
		Last Modified: Wed, 19 Mar 2025 00:41:44 GMT  
		Size: 146.2 MB (146237931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9ed303f69d6af2c83b1c0d459480b0317fea0ea99d58fc64065eda060d0814`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc17d0878a6dc84710c44a60d77af52e058f61698e2893fe2e9d87d9c3e50c`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d730573fa6257d4691d0966798f477537a5ef6eb4dc04929e030418fc421a5`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b7fe09ccdad340a138a3535ccd397565c3e42bd3a9449a7e6aba340dfa4638`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5967c09213d5e28f003439a659208ff9c27290d3b5c3be36ee81ea678a766452`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e409ed82226be54e26f06b4584011c03259d4fbfa4be7e06215ed50fee56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19a653309824ada5498999558631c1e7446cccccf717e46775680ebd90d9337`

```dockerfile
```

-	Layers:
	-	`sha256:831088a90410b9d6d70276807b3a7fb58f5038275794386776139bdb20355d3a`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1.8-jammy`

```console
$ docker pull clickhouse@sha256:a6d159679b55ab169ae347e4bd46ea326776cdb9c2cb9c7b68cd265b68d48ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:7b0a517fcd0807dad4250971456a98f66aa56543c60c25ee78ededcc2267548c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191116985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1a596952af9f3ed57d947a9521f10500e43f1cd325951e39b4987809f2d81b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.1.8.25
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace14fd0dc506feb5687249d3d2e9678b343ace61c0562988f4b5cadd3199edc`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 7.2 MB (7151699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7781a934857b72e38639e0483c40e1ef2d4834f512bab38cb77302735cf310ad`  
		Last Modified: Wed, 09 Apr 2025 01:12:16 GMT  
		Size: 153.6 MB (153562678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e41820ab00ee5f42c1ab52d541c04abf64d2ad2719aacf452147ec1f31113ea`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b5304b74e3ea0a14f52327e1f9836746da4efb32cb92a74780adfb06732bd7`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a2d55d83415ccbd6a94141c706be66c88c0bb38ee158e027264b45e1411521`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1d989071e1018032c9561fa02b8de3216cbd14b93575067154ce473071767c`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e6d19061d46eb23898fe3e0b3bd5b5dcc899b4026774b630399f6de28a8c7e`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:cac0acd7b09f87e74209a2e4258bc99eea8389a5419d85d936b139d187ddb62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0696ca167162e87f5605a050f92fbc9b932421488fe2d6906b0d9fd84f62ec06`

```dockerfile
```

-	Layers:
	-	`sha256:085ee510c98c99b71b07caf443e51291c1a4295b831d15a24ebbe804fd759f13`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b57470c31395773af07839352bd21f0e60f4d439d83d4dca99061d2c15b8234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181587499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b264701335327689e9952fe111e2f38405d3accccd17f98c035884cd1d4d4b23`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994a6684f3864e36c1023cd8b8c7f55d49a5a2b83843f3c63fdc62d4f74104b8`  
		Last Modified: Wed, 19 Mar 2025 00:41:44 GMT  
		Size: 146.2 MB (146237931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9ed303f69d6af2c83b1c0d459480b0317fea0ea99d58fc64065eda060d0814`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc17d0878a6dc84710c44a60d77af52e058f61698e2893fe2e9d87d9c3e50c`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d730573fa6257d4691d0966798f477537a5ef6eb4dc04929e030418fc421a5`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b7fe09ccdad340a138a3535ccd397565c3e42bd3a9449a7e6aba340dfa4638`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5967c09213d5e28f003439a659208ff9c27290d3b5c3be36ee81ea678a766452`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e409ed82226be54e26f06b4584011c03259d4fbfa4be7e06215ed50fee56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19a653309824ada5498999558631c1e7446cccccf717e46775680ebd90d9337`

```dockerfile
```

-	Layers:
	-	`sha256:831088a90410b9d6d70276807b3a7fb58f5038275794386776139bdb20355d3a`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1.8.25`

```console
$ docker pull clickhouse@sha256:a6d159679b55ab169ae347e4bd46ea326776cdb9c2cb9c7b68cd265b68d48ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1.8.25` - linux; amd64

```console
$ docker pull clickhouse@sha256:7b0a517fcd0807dad4250971456a98f66aa56543c60c25ee78ededcc2267548c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191116985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1a596952af9f3ed57d947a9521f10500e43f1cd325951e39b4987809f2d81b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.1.8.25
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace14fd0dc506feb5687249d3d2e9678b343ace61c0562988f4b5cadd3199edc`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 7.2 MB (7151699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7781a934857b72e38639e0483c40e1ef2d4834f512bab38cb77302735cf310ad`  
		Last Modified: Wed, 09 Apr 2025 01:12:16 GMT  
		Size: 153.6 MB (153562678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e41820ab00ee5f42c1ab52d541c04abf64d2ad2719aacf452147ec1f31113ea`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b5304b74e3ea0a14f52327e1f9836746da4efb32cb92a74780adfb06732bd7`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a2d55d83415ccbd6a94141c706be66c88c0bb38ee158e027264b45e1411521`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1d989071e1018032c9561fa02b8de3216cbd14b93575067154ce473071767c`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e6d19061d46eb23898fe3e0b3bd5b5dcc899b4026774b630399f6de28a8c7e`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.8.25` - unknown; unknown

```console
$ docker pull clickhouse@sha256:cac0acd7b09f87e74209a2e4258bc99eea8389a5419d85d936b139d187ddb62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0696ca167162e87f5605a050f92fbc9b932421488fe2d6906b0d9fd84f62ec06`

```dockerfile
```

-	Layers:
	-	`sha256:085ee510c98c99b71b07caf443e51291c1a4295b831d15a24ebbe804fd759f13`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1.8.25` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b57470c31395773af07839352bd21f0e60f4d439d83d4dca99061d2c15b8234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181587499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b264701335327689e9952fe111e2f38405d3accccd17f98c035884cd1d4d4b23`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994a6684f3864e36c1023cd8b8c7f55d49a5a2b83843f3c63fdc62d4f74104b8`  
		Last Modified: Wed, 19 Mar 2025 00:41:44 GMT  
		Size: 146.2 MB (146237931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9ed303f69d6af2c83b1c0d459480b0317fea0ea99d58fc64065eda060d0814`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc17d0878a6dc84710c44a60d77af52e058f61698e2893fe2e9d87d9c3e50c`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d730573fa6257d4691d0966798f477537a5ef6eb4dc04929e030418fc421a5`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b7fe09ccdad340a138a3535ccd397565c3e42bd3a9449a7e6aba340dfa4638`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5967c09213d5e28f003439a659208ff9c27290d3b5c3be36ee81ea678a766452`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.8.25` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e409ed82226be54e26f06b4584011c03259d4fbfa4be7e06215ed50fee56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19a653309824ada5498999558631c1e7446cccccf717e46775680ebd90d9337`

```dockerfile
```

-	Layers:
	-	`sha256:831088a90410b9d6d70276807b3a7fb58f5038275794386776139bdb20355d3a`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1.8.25-jammy`

```console
$ docker pull clickhouse@sha256:a6d159679b55ab169ae347e4bd46ea326776cdb9c2cb9c7b68cd265b68d48ade
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1.8.25-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:7b0a517fcd0807dad4250971456a98f66aa56543c60c25ee78ededcc2267548c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191116985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1a596952af9f3ed57d947a9521f10500e43f1cd325951e39b4987809f2d81b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.1.8.25
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace14fd0dc506feb5687249d3d2e9678b343ace61c0562988f4b5cadd3199edc`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 7.2 MB (7151699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7781a934857b72e38639e0483c40e1ef2d4834f512bab38cb77302735cf310ad`  
		Last Modified: Wed, 09 Apr 2025 01:12:16 GMT  
		Size: 153.6 MB (153562678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e41820ab00ee5f42c1ab52d541c04abf64d2ad2719aacf452147ec1f31113ea`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7b5304b74e3ea0a14f52327e1f9836746da4efb32cb92a74780adfb06732bd7`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a2d55d83415ccbd6a94141c706be66c88c0bb38ee158e027264b45e1411521`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1d989071e1018032c9561fa02b8de3216cbd14b93575067154ce473071767c`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e6d19061d46eb23898fe3e0b3bd5b5dcc899b4026774b630399f6de28a8c7e`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.8.25-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:cac0acd7b09f87e74209a2e4258bc99eea8389a5419d85d936b139d187ddb62e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0696ca167162e87f5605a050f92fbc9b932421488fe2d6906b0d9fd84f62ec06`

```dockerfile
```

-	Layers:
	-	`sha256:085ee510c98c99b71b07caf443e51291c1a4295b831d15a24ebbe804fd759f13`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1.8.25-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b57470c31395773af07839352bd21f0e60f4d439d83d4dca99061d2c15b8234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181587499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b264701335327689e9952fe111e2f38405d3accccd17f98c035884cd1d4d4b23`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.1.8.25
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994a6684f3864e36c1023cd8b8c7f55d49a5a2b83843f3c63fdc62d4f74104b8`  
		Last Modified: Wed, 19 Mar 2025 00:41:44 GMT  
		Size: 146.2 MB (146237931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9ed303f69d6af2c83b1c0d459480b0317fea0ea99d58fc64065eda060d0814`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79cc17d0878a6dc84710c44a60d77af52e058f61698e2893fe2e9d87d9c3e50c`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d730573fa6257d4691d0966798f477537a5ef6eb4dc04929e030418fc421a5`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b7fe09ccdad340a138a3535ccd397565c3e42bd3a9449a7e6aba340dfa4638`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5967c09213d5e28f003439a659208ff9c27290d3b5c3be36ee81ea678a766452`  
		Last Modified: Wed, 19 Mar 2025 00:41:41 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.8.25-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:410e409ed82226be54e26f06b4584011c03259d4fbfa4be7e06215ed50fee56f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a19a653309824ada5498999558631c1e7446cccccf717e46775680ebd90d9337`

```dockerfile
```

-	Layers:
	-	`sha256:831088a90410b9d6d70276807b3a7fb58f5038275794386776139bdb20355d3a`  
		Last Modified: Wed, 19 Mar 2025 00:41:40 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.2`

```console
$ docker pull clickhouse@sha256:c50ec72c03be1d6d3d5db042abf1398ff6f67c27f8b36e9bfb7a1f75c3cc8810
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:21730b8881e5e4f55eabacf37260eca8e44e37f5bdb0864496ec0ba33ac3ed1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201037858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07abaa6c08ddbdef8f958efd90a8269d0ccaf3fe0ca12e03003fc18d175967c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.2.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa5af23453d5abe59d773600e68245891a7360daa7cfbdb4629423bccdc0415`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 7.2 MB (7151737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63dff5a390e04e18e475153079094f533adac6af5d3194ab7af1b63d93c3d4ff`  
		Last Modified: Wed, 09 Apr 2025 01:12:17 GMT  
		Size: 163.5 MB (163483509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d626032796ed1e26ef9ec42e75f430c7a971ed48cb294b1624fd837485a80012`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1022c58a692463fa09b0b6147c60f9a3a19fe9a7b47342265983b6de2c2c7c1d`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa9d4f3112aaf049cbb59914dd00fb8f407063f9d575e0d4fc68a57c324798`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb91dcef827bde38e930ad473bd16a794b9eb1dbeb63fe696c2c33708573d6d`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d344ba3064cea1677bfae35ab6a40241c32755971c86a0cb9ea8d03775b39f`  
		Last Modified: Wed, 09 Apr 2025 01:12:16 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f8abdf7cd2061b1d59e8555df832e023090bc3e1ec054417c57c5008956a6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04563742e936b091c5a8cf567cb14bf63cf323777ce8660785fec340b22298f1`

```dockerfile
```

-	Layers:
	-	`sha256:f3e1794bcc62c4cc9d3bc2e00feaafea5da6dcd06f812788eb3418df1c478695`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a75fed5360ff6b808cafb4dcb99e090ff93a01b4522324343cbf7735608dbc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190274638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7b3b17c006cf053e573a0bb28cac103ca02443821383b2b7ca13cd15dbc6a2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa558d9144156a45f3ed7f197d2ddf6092b729b6087a74fea31f80286fada93e`  
		Last Modified: Wed, 19 Mar 2025 00:39:28 GMT  
		Size: 154.9 MB (154925069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2164565157c304fc394957f994673438e576c3476d16f1ed5aa480787f5e255`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af9448d2b81924d6bf7cfcdb34916b8763f480af84bbf08d33c46a948e462e`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957f8b2b9228fe64042ba2f96d0e2379ae970a5b37a75eedf53c1238b330677d`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8263229c7cbed64d0964a1858c08b8289333c565208fd5de3a01779aeb97fbb2`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0626950e0e0eac209e960a8025fad60f549fb290a150cde371bf2a33e43bcf3`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:af311b2d9f344317bccf1bce5b6118373aff9f251faaf8e10d9632737d3ed878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d33b64291de222fdb484445106defc2fbb788fc286a49961cbac8e4013197b`

```dockerfile
```

-	Layers:
	-	`sha256:586093a48ca78f5c2390bd7950fc83195856ad4b3623654b9c0fa8ebedde175e`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.2-jammy`

```console
$ docker pull clickhouse@sha256:c50ec72c03be1d6d3d5db042abf1398ff6f67c27f8b36e9bfb7a1f75c3cc8810
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:21730b8881e5e4f55eabacf37260eca8e44e37f5bdb0864496ec0ba33ac3ed1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201037858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07abaa6c08ddbdef8f958efd90a8269d0ccaf3fe0ca12e03003fc18d175967c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.2.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa5af23453d5abe59d773600e68245891a7360daa7cfbdb4629423bccdc0415`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 7.2 MB (7151737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63dff5a390e04e18e475153079094f533adac6af5d3194ab7af1b63d93c3d4ff`  
		Last Modified: Wed, 09 Apr 2025 01:12:17 GMT  
		Size: 163.5 MB (163483509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d626032796ed1e26ef9ec42e75f430c7a971ed48cb294b1624fd837485a80012`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1022c58a692463fa09b0b6147c60f9a3a19fe9a7b47342265983b6de2c2c7c1d`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa9d4f3112aaf049cbb59914dd00fb8f407063f9d575e0d4fc68a57c324798`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb91dcef827bde38e930ad473bd16a794b9eb1dbeb63fe696c2c33708573d6d`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d344ba3064cea1677bfae35ab6a40241c32755971c86a0cb9ea8d03775b39f`  
		Last Modified: Wed, 09 Apr 2025 01:12:16 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f8abdf7cd2061b1d59e8555df832e023090bc3e1ec054417c57c5008956a6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04563742e936b091c5a8cf567cb14bf63cf323777ce8660785fec340b22298f1`

```dockerfile
```

-	Layers:
	-	`sha256:f3e1794bcc62c4cc9d3bc2e00feaafea5da6dcd06f812788eb3418df1c478695`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a75fed5360ff6b808cafb4dcb99e090ff93a01b4522324343cbf7735608dbc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190274638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7b3b17c006cf053e573a0bb28cac103ca02443821383b2b7ca13cd15dbc6a2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa558d9144156a45f3ed7f197d2ddf6092b729b6087a74fea31f80286fada93e`  
		Last Modified: Wed, 19 Mar 2025 00:39:28 GMT  
		Size: 154.9 MB (154925069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2164565157c304fc394957f994673438e576c3476d16f1ed5aa480787f5e255`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af9448d2b81924d6bf7cfcdb34916b8763f480af84bbf08d33c46a948e462e`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957f8b2b9228fe64042ba2f96d0e2379ae970a5b37a75eedf53c1238b330677d`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8263229c7cbed64d0964a1858c08b8289333c565208fd5de3a01779aeb97fbb2`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0626950e0e0eac209e960a8025fad60f549fb290a150cde371bf2a33e43bcf3`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:af311b2d9f344317bccf1bce5b6118373aff9f251faaf8e10d9632737d3ed878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d33b64291de222fdb484445106defc2fbb788fc286a49961cbac8e4013197b`

```dockerfile
```

-	Layers:
	-	`sha256:586093a48ca78f5c2390bd7950fc83195856ad4b3623654b9c0fa8ebedde175e`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.2.2`

```console
$ docker pull clickhouse@sha256:c50ec72c03be1d6d3d5db042abf1398ff6f67c27f8b36e9bfb7a1f75c3cc8810
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:21730b8881e5e4f55eabacf37260eca8e44e37f5bdb0864496ec0ba33ac3ed1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201037858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07abaa6c08ddbdef8f958efd90a8269d0ccaf3fe0ca12e03003fc18d175967c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.2.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa5af23453d5abe59d773600e68245891a7360daa7cfbdb4629423bccdc0415`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 7.2 MB (7151737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63dff5a390e04e18e475153079094f533adac6af5d3194ab7af1b63d93c3d4ff`  
		Last Modified: Wed, 09 Apr 2025 01:12:17 GMT  
		Size: 163.5 MB (163483509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d626032796ed1e26ef9ec42e75f430c7a971ed48cb294b1624fd837485a80012`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1022c58a692463fa09b0b6147c60f9a3a19fe9a7b47342265983b6de2c2c7c1d`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa9d4f3112aaf049cbb59914dd00fb8f407063f9d575e0d4fc68a57c324798`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb91dcef827bde38e930ad473bd16a794b9eb1dbeb63fe696c2c33708573d6d`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d344ba3064cea1677bfae35ab6a40241c32755971c86a0cb9ea8d03775b39f`  
		Last Modified: Wed, 09 Apr 2025 01:12:16 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f8abdf7cd2061b1d59e8555df832e023090bc3e1ec054417c57c5008956a6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04563742e936b091c5a8cf567cb14bf63cf323777ce8660785fec340b22298f1`

```dockerfile
```

-	Layers:
	-	`sha256:f3e1794bcc62c4cc9d3bc2e00feaafea5da6dcd06f812788eb3418df1c478695`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a75fed5360ff6b808cafb4dcb99e090ff93a01b4522324343cbf7735608dbc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190274638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7b3b17c006cf053e573a0bb28cac103ca02443821383b2b7ca13cd15dbc6a2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa558d9144156a45f3ed7f197d2ddf6092b729b6087a74fea31f80286fada93e`  
		Last Modified: Wed, 19 Mar 2025 00:39:28 GMT  
		Size: 154.9 MB (154925069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2164565157c304fc394957f994673438e576c3476d16f1ed5aa480787f5e255`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af9448d2b81924d6bf7cfcdb34916b8763f480af84bbf08d33c46a948e462e`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957f8b2b9228fe64042ba2f96d0e2379ae970a5b37a75eedf53c1238b330677d`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8263229c7cbed64d0964a1858c08b8289333c565208fd5de3a01779aeb97fbb2`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0626950e0e0eac209e960a8025fad60f549fb290a150cde371bf2a33e43bcf3`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:af311b2d9f344317bccf1bce5b6118373aff9f251faaf8e10d9632737d3ed878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d33b64291de222fdb484445106defc2fbb788fc286a49961cbac8e4013197b`

```dockerfile
```

-	Layers:
	-	`sha256:586093a48ca78f5c2390bd7950fc83195856ad4b3623654b9c0fa8ebedde175e`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.2.2-jammy`

```console
$ docker pull clickhouse@sha256:c50ec72c03be1d6d3d5db042abf1398ff6f67c27f8b36e9bfb7a1f75c3cc8810
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:21730b8881e5e4f55eabacf37260eca8e44e37f5bdb0864496ec0ba33ac3ed1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201037858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07abaa6c08ddbdef8f958efd90a8269d0ccaf3fe0ca12e03003fc18d175967c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.2.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa5af23453d5abe59d773600e68245891a7360daa7cfbdb4629423bccdc0415`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 7.2 MB (7151737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63dff5a390e04e18e475153079094f533adac6af5d3194ab7af1b63d93c3d4ff`  
		Last Modified: Wed, 09 Apr 2025 01:12:17 GMT  
		Size: 163.5 MB (163483509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d626032796ed1e26ef9ec42e75f430c7a971ed48cb294b1624fd837485a80012`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1022c58a692463fa09b0b6147c60f9a3a19fe9a7b47342265983b6de2c2c7c1d`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa9d4f3112aaf049cbb59914dd00fb8f407063f9d575e0d4fc68a57c324798`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb91dcef827bde38e930ad473bd16a794b9eb1dbeb63fe696c2c33708573d6d`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d344ba3064cea1677bfae35ab6a40241c32755971c86a0cb9ea8d03775b39f`  
		Last Modified: Wed, 09 Apr 2025 01:12:16 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f8abdf7cd2061b1d59e8555df832e023090bc3e1ec054417c57c5008956a6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04563742e936b091c5a8cf567cb14bf63cf323777ce8660785fec340b22298f1`

```dockerfile
```

-	Layers:
	-	`sha256:f3e1794bcc62c4cc9d3bc2e00feaafea5da6dcd06f812788eb3418df1c478695`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a75fed5360ff6b808cafb4dcb99e090ff93a01b4522324343cbf7735608dbc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190274638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7b3b17c006cf053e573a0bb28cac103ca02443821383b2b7ca13cd15dbc6a2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa558d9144156a45f3ed7f197d2ddf6092b729b6087a74fea31f80286fada93e`  
		Last Modified: Wed, 19 Mar 2025 00:39:28 GMT  
		Size: 154.9 MB (154925069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2164565157c304fc394957f994673438e576c3476d16f1ed5aa480787f5e255`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af9448d2b81924d6bf7cfcdb34916b8763f480af84bbf08d33c46a948e462e`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957f8b2b9228fe64042ba2f96d0e2379ae970a5b37a75eedf53c1238b330677d`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8263229c7cbed64d0964a1858c08b8289333c565208fd5de3a01779aeb97fbb2`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0626950e0e0eac209e960a8025fad60f549fb290a150cde371bf2a33e43bcf3`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:af311b2d9f344317bccf1bce5b6118373aff9f251faaf8e10d9632737d3ed878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d33b64291de222fdb484445106defc2fbb788fc286a49961cbac8e4013197b`

```dockerfile
```

-	Layers:
	-	`sha256:586093a48ca78f5c2390bd7950fc83195856ad4b3623654b9c0fa8ebedde175e`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.2.2.39`

```console
$ docker pull clickhouse@sha256:c50ec72c03be1d6d3d5db042abf1398ff6f67c27f8b36e9bfb7a1f75c3cc8810
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2.2.39` - linux; amd64

```console
$ docker pull clickhouse@sha256:21730b8881e5e4f55eabacf37260eca8e44e37f5bdb0864496ec0ba33ac3ed1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201037858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07abaa6c08ddbdef8f958efd90a8269d0ccaf3fe0ca12e03003fc18d175967c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.2.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa5af23453d5abe59d773600e68245891a7360daa7cfbdb4629423bccdc0415`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 7.2 MB (7151737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63dff5a390e04e18e475153079094f533adac6af5d3194ab7af1b63d93c3d4ff`  
		Last Modified: Wed, 09 Apr 2025 01:12:17 GMT  
		Size: 163.5 MB (163483509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d626032796ed1e26ef9ec42e75f430c7a971ed48cb294b1624fd837485a80012`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1022c58a692463fa09b0b6147c60f9a3a19fe9a7b47342265983b6de2c2c7c1d`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa9d4f3112aaf049cbb59914dd00fb8f407063f9d575e0d4fc68a57c324798`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb91dcef827bde38e930ad473bd16a794b9eb1dbeb63fe696c2c33708573d6d`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d344ba3064cea1677bfae35ab6a40241c32755971c86a0cb9ea8d03775b39f`  
		Last Modified: Wed, 09 Apr 2025 01:12:16 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2.39` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f8abdf7cd2061b1d59e8555df832e023090bc3e1ec054417c57c5008956a6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04563742e936b091c5a8cf567cb14bf63cf323777ce8660785fec340b22298f1`

```dockerfile
```

-	Layers:
	-	`sha256:f3e1794bcc62c4cc9d3bc2e00feaafea5da6dcd06f812788eb3418df1c478695`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2.2.39` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a75fed5360ff6b808cafb4dcb99e090ff93a01b4522324343cbf7735608dbc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190274638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7b3b17c006cf053e573a0bb28cac103ca02443821383b2b7ca13cd15dbc6a2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa558d9144156a45f3ed7f197d2ddf6092b729b6087a74fea31f80286fada93e`  
		Last Modified: Wed, 19 Mar 2025 00:39:28 GMT  
		Size: 154.9 MB (154925069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2164565157c304fc394957f994673438e576c3476d16f1ed5aa480787f5e255`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af9448d2b81924d6bf7cfcdb34916b8763f480af84bbf08d33c46a948e462e`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957f8b2b9228fe64042ba2f96d0e2379ae970a5b37a75eedf53c1238b330677d`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8263229c7cbed64d0964a1858c08b8289333c565208fd5de3a01779aeb97fbb2`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0626950e0e0eac209e960a8025fad60f549fb290a150cde371bf2a33e43bcf3`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2.39` - unknown; unknown

```console
$ docker pull clickhouse@sha256:af311b2d9f344317bccf1bce5b6118373aff9f251faaf8e10d9632737d3ed878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d33b64291de222fdb484445106defc2fbb788fc286a49961cbac8e4013197b`

```dockerfile
```

-	Layers:
	-	`sha256:586093a48ca78f5c2390bd7950fc83195856ad4b3623654b9c0fa8ebedde175e`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.2.2.39-jammy`

```console
$ docker pull clickhouse@sha256:c50ec72c03be1d6d3d5db042abf1398ff6f67c27f8b36e9bfb7a1f75c3cc8810
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.2.2.39-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:21730b8881e5e4f55eabacf37260eca8e44e37f5bdb0864496ec0ba33ac3ed1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **201.0 MB (201037858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07abaa6c08ddbdef8f958efd90a8269d0ccaf3fe0ca12e03003fc18d175967c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.2.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa5af23453d5abe59d773600e68245891a7360daa7cfbdb4629423bccdc0415`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 7.2 MB (7151737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63dff5a390e04e18e475153079094f533adac6af5d3194ab7af1b63d93c3d4ff`  
		Last Modified: Wed, 09 Apr 2025 01:12:17 GMT  
		Size: 163.5 MB (163483509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d626032796ed1e26ef9ec42e75f430c7a971ed48cb294b1624fd837485a80012`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1022c58a692463fa09b0b6147c60f9a3a19fe9a7b47342265983b6de2c2c7c1d`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffa9d4f3112aaf049cbb59914dd00fb8f407063f9d575e0d4fc68a57c324798`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb91dcef827bde38e930ad473bd16a794b9eb1dbeb63fe696c2c33708573d6d`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05d344ba3064cea1677bfae35ab6a40241c32755971c86a0cb9ea8d03775b39f`  
		Last Modified: Wed, 09 Apr 2025 01:12:16 GMT  
		Size: 3.8 KB (3838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2.39-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f8abdf7cd2061b1d59e8555df832e023090bc3e1ec054417c57c5008956a6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04563742e936b091c5a8cf567cb14bf63cf323777ce8660785fec340b22298f1`

```dockerfile
```

-	Layers:
	-	`sha256:f3e1794bcc62c4cc9d3bc2e00feaafea5da6dcd06f812788eb3418df1c478695`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 25.3 KB (25263 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.2.2.39-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a75fed5360ff6b808cafb4dcb99e090ff93a01b4522324343cbf7735608dbc12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.3 MB (190274638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd7b3b17c006cf053e573a0bb28cac103ca02443821383b2b7ca13cd15dbc6a2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
CMD ["/bin/bash"]
# Tue, 18 Mar 2025 11:21:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 18 Mar 2025 11:21:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPO_CHANNEL=stable
# Tue, 18 Mar 2025 11:21:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 18 Mar 2025 11:21:17 GMT
ARG VERSION=25.2.2.39
# Tue, 18 Mar 2025 11:21:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
ENV LANG=en_US.UTF-8
# Tue, 18 Mar 2025 11:21:17 GMT
ENV TZ=UTC
# Tue, 18 Mar 2025 11:21:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.2.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Mar 2025 11:21:17 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 18 Mar 2025 11:21:17 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 18 Mar 2025 11:21:17 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 18 Mar 2025 11:21:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc0fdf78f6ab2fb8e464c884e15d0f5b20144d3f5a3942d27643b466a681628`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 7.1 MB (7121132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa558d9144156a45f3ed7f197d2ddf6092b729b6087a74fea31f80286fada93e`  
		Last Modified: Wed, 19 Mar 2025 00:39:28 GMT  
		Size: 154.9 MB (154925069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2164565157c304fc394957f994673438e576c3476d16f1ed5aa480787f5e255`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7af9448d2b81924d6bf7cfcdb34916b8763f480af84bbf08d33c46a948e462e`  
		Last Modified: Wed, 19 Mar 2025 00:39:24 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957f8b2b9228fe64042ba2f96d0e2379ae970a5b37a75eedf53c1238b330677d`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8263229c7cbed64d0964a1858c08b8289333c565208fd5de3a01779aeb97fbb2`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 366.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0626950e0e0eac209e960a8025fad60f549fb290a150cde371bf2a33e43bcf3`  
		Last Modified: Wed, 19 Mar 2025 00:39:25 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.2.2.39-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:af311b2d9f344317bccf1bce5b6118373aff9f251faaf8e10d9632737d3ed878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d33b64291de222fdb484445106defc2fbb788fc286a49961cbac8e4013197b`

```dockerfile
```

-	Layers:
	-	`sha256:586093a48ca78f5c2390bd7950fc83195856ad4b3623654b9c0fa8ebedde175e`  
		Last Modified: Wed, 19 Mar 2025 00:39:23 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:8745a6efb4d3d761664bcceb450c5cea0da7ac490688df09de61189339b57cac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:0c7dc14e63e6b5d5810d752ca28bb24c0fb6552971a19514d914bceac93f44e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204546084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2aafc8bcd7da81efe8c1ab85cb9fba3b9cab375dccf13c0e9236eb73383d75d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfab47cf5cf3ca9941151a55bb2cb9437b2cc0c0d6115831f174327eedc2a69`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 7.2 MB (7151721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43eab875d7fbca96a916fd1ba2f7c37a188a352643300198235618c41cc771a`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 167.0 MB (166991745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81414aef9f4936ed3818cecd2ac6bbff5e6da3e3d43982e37193209c09b7b12c`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc61bee4cda5c74dc726cf66a2abf6a8e0bdb1c9f5f9782219f7261c2bdf593a`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dec9e3885bcee13eb8c84219b1b5c74c45df3be44af4071fdb9b3f1a5e11b12`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146f8cb5454888fb18a7ec2c09d7c641e0d4ad0f462448ce9b41a3662bd36079`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f0eeb8fc96a82e7d207eda20f28aa4681f1f1b263cfea769ce3096afe210a7`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3486355dbac6d4cb52a1fb1fcd4e5f56919b98e7641f2141237fa8740377728e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3d9b71e8f69fdd20848ac97d9298152adca5338a72b7b5b18696779a3ba2b5`

```dockerfile
```

-	Layers:
	-	`sha256:cbeed85d56a1efd879d6fd443ce9cc2ed8a3e16aac619dd329edfa745aa63942`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:8745a6efb4d3d761664bcceb450c5cea0da7ac490688df09de61189339b57cac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0c7dc14e63e6b5d5810d752ca28bb24c0fb6552971a19514d914bceac93f44e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204546084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2aafc8bcd7da81efe8c1ab85cb9fba3b9cab375dccf13c0e9236eb73383d75d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfab47cf5cf3ca9941151a55bb2cb9437b2cc0c0d6115831f174327eedc2a69`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 7.2 MB (7151721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43eab875d7fbca96a916fd1ba2f7c37a188a352643300198235618c41cc771a`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 167.0 MB (166991745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81414aef9f4936ed3818cecd2ac6bbff5e6da3e3d43982e37193209c09b7b12c`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc61bee4cda5c74dc726cf66a2abf6a8e0bdb1c9f5f9782219f7261c2bdf593a`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dec9e3885bcee13eb8c84219b1b5c74c45df3be44af4071fdb9b3f1a5e11b12`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146f8cb5454888fb18a7ec2c09d7c641e0d4ad0f462448ce9b41a3662bd36079`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f0eeb8fc96a82e7d207eda20f28aa4681f1f1b263cfea769ce3096afe210a7`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3486355dbac6d4cb52a1fb1fcd4e5f56919b98e7641f2141237fa8740377728e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3d9b71e8f69fdd20848ac97d9298152adca5338a72b7b5b18696779a3ba2b5`

```dockerfile
```

-	Layers:
	-	`sha256:cbeed85d56a1efd879d6fd443ce9cc2ed8a3e16aac619dd329edfa745aa63942`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.2`

```console
$ docker pull clickhouse@sha256:8745a6efb4d3d761664bcceb450c5cea0da7ac490688df09de61189339b57cac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:0c7dc14e63e6b5d5810d752ca28bb24c0fb6552971a19514d914bceac93f44e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204546084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2aafc8bcd7da81efe8c1ab85cb9fba3b9cab375dccf13c0e9236eb73383d75d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfab47cf5cf3ca9941151a55bb2cb9437b2cc0c0d6115831f174327eedc2a69`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 7.2 MB (7151721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43eab875d7fbca96a916fd1ba2f7c37a188a352643300198235618c41cc771a`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 167.0 MB (166991745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81414aef9f4936ed3818cecd2ac6bbff5e6da3e3d43982e37193209c09b7b12c`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc61bee4cda5c74dc726cf66a2abf6a8e0bdb1c9f5f9782219f7261c2bdf593a`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dec9e3885bcee13eb8c84219b1b5c74c45df3be44af4071fdb9b3f1a5e11b12`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146f8cb5454888fb18a7ec2c09d7c641e0d4ad0f462448ce9b41a3662bd36079`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f0eeb8fc96a82e7d207eda20f28aa4681f1f1b263cfea769ce3096afe210a7`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3486355dbac6d4cb52a1fb1fcd4e5f56919b98e7641f2141237fa8740377728e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3d9b71e8f69fdd20848ac97d9298152adca5338a72b7b5b18696779a3ba2b5`

```dockerfile
```

-	Layers:
	-	`sha256:cbeed85d56a1efd879d6fd443ce9cc2ed8a3e16aac619dd329edfa745aa63942`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.2-jammy`

```console
$ docker pull clickhouse@sha256:8745a6efb4d3d761664bcceb450c5cea0da7ac490688df09de61189339b57cac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0c7dc14e63e6b5d5810d752ca28bb24c0fb6552971a19514d914bceac93f44e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204546084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2aafc8bcd7da81efe8c1ab85cb9fba3b9cab375dccf13c0e9236eb73383d75d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfab47cf5cf3ca9941151a55bb2cb9437b2cc0c0d6115831f174327eedc2a69`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 7.2 MB (7151721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43eab875d7fbca96a916fd1ba2f7c37a188a352643300198235618c41cc771a`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 167.0 MB (166991745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81414aef9f4936ed3818cecd2ac6bbff5e6da3e3d43982e37193209c09b7b12c`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc61bee4cda5c74dc726cf66a2abf6a8e0bdb1c9f5f9782219f7261c2bdf593a`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dec9e3885bcee13eb8c84219b1b5c74c45df3be44af4071fdb9b3f1a5e11b12`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146f8cb5454888fb18a7ec2c09d7c641e0d4ad0f462448ce9b41a3662bd36079`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f0eeb8fc96a82e7d207eda20f28aa4681f1f1b263cfea769ce3096afe210a7`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3486355dbac6d4cb52a1fb1fcd4e5f56919b98e7641f2141237fa8740377728e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3d9b71e8f69fdd20848ac97d9298152adca5338a72b7b5b18696779a3ba2b5`

```dockerfile
```

-	Layers:
	-	`sha256:cbeed85d56a1efd879d6fd443ce9cc2ed8a3e16aac619dd329edfa745aa63942`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.2.39`

```console
$ docker pull clickhouse@sha256:8745a6efb4d3d761664bcceb450c5cea0da7ac490688df09de61189339b57cac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.2.39` - linux; amd64

```console
$ docker pull clickhouse@sha256:0c7dc14e63e6b5d5810d752ca28bb24c0fb6552971a19514d914bceac93f44e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204546084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2aafc8bcd7da81efe8c1ab85cb9fba3b9cab375dccf13c0e9236eb73383d75d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfab47cf5cf3ca9941151a55bb2cb9437b2cc0c0d6115831f174327eedc2a69`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 7.2 MB (7151721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43eab875d7fbca96a916fd1ba2f7c37a188a352643300198235618c41cc771a`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 167.0 MB (166991745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81414aef9f4936ed3818cecd2ac6bbff5e6da3e3d43982e37193209c09b7b12c`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc61bee4cda5c74dc726cf66a2abf6a8e0bdb1c9f5f9782219f7261c2bdf593a`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dec9e3885bcee13eb8c84219b1b5c74c45df3be44af4071fdb9b3f1a5e11b12`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146f8cb5454888fb18a7ec2c09d7c641e0d4ad0f462448ce9b41a3662bd36079`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f0eeb8fc96a82e7d207eda20f28aa4681f1f1b263cfea769ce3096afe210a7`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.2.39` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3486355dbac6d4cb52a1fb1fcd4e5f56919b98e7641f2141237fa8740377728e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3d9b71e8f69fdd20848ac97d9298152adca5338a72b7b5b18696779a3ba2b5`

```dockerfile
```

-	Layers:
	-	`sha256:cbeed85d56a1efd879d6fd443ce9cc2ed8a3e16aac619dd329edfa745aa63942`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.2.39` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.2.39` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.2.39-jammy`

```console
$ docker pull clickhouse@sha256:8745a6efb4d3d761664bcceb450c5cea0da7ac490688df09de61189339b57cac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.2.39-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0c7dc14e63e6b5d5810d752ca28bb24c0fb6552971a19514d914bceac93f44e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204546084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2aafc8bcd7da81efe8c1ab85cb9fba3b9cab375dccf13c0e9236eb73383d75d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfab47cf5cf3ca9941151a55bb2cb9437b2cc0c0d6115831f174327eedc2a69`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 7.2 MB (7151721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43eab875d7fbca96a916fd1ba2f7c37a188a352643300198235618c41cc771a`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 167.0 MB (166991745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81414aef9f4936ed3818cecd2ac6bbff5e6da3e3d43982e37193209c09b7b12c`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc61bee4cda5c74dc726cf66a2abf6a8e0bdb1c9f5f9782219f7261c2bdf593a`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dec9e3885bcee13eb8c84219b1b5c74c45df3be44af4071fdb9b3f1a5e11b12`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146f8cb5454888fb18a7ec2c09d7c641e0d4ad0f462448ce9b41a3662bd36079`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f0eeb8fc96a82e7d207eda20f28aa4681f1f1b263cfea769ce3096afe210a7`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.2.39-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3486355dbac6d4cb52a1fb1fcd4e5f56919b98e7641f2141237fa8740377728e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3d9b71e8f69fdd20848ac97d9298152adca5338a72b7b5b18696779a3ba2b5`

```dockerfile
```

-	Layers:
	-	`sha256:cbeed85d56a1efd879d6fd443ce9cc2ed8a3e16aac619dd329edfa745aa63942`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.2.39-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.2.39-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:8745a6efb4d3d761664bcceb450c5cea0da7ac490688df09de61189339b57cac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0c7dc14e63e6b5d5810d752ca28bb24c0fb6552971a19514d914bceac93f44e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204546084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2aafc8bcd7da81efe8c1ab85cb9fba3b9cab375dccf13c0e9236eb73383d75d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfab47cf5cf3ca9941151a55bb2cb9437b2cc0c0d6115831f174327eedc2a69`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 7.2 MB (7151721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43eab875d7fbca96a916fd1ba2f7c37a188a352643300198235618c41cc771a`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 167.0 MB (166991745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81414aef9f4936ed3818cecd2ac6bbff5e6da3e3d43982e37193209c09b7b12c`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc61bee4cda5c74dc726cf66a2abf6a8e0bdb1c9f5f9782219f7261c2bdf593a`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dec9e3885bcee13eb8c84219b1b5c74c45df3be44af4071fdb9b3f1a5e11b12`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146f8cb5454888fb18a7ec2c09d7c641e0d4ad0f462448ce9b41a3662bd36079`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f0eeb8fc96a82e7d207eda20f28aa4681f1f1b263cfea769ce3096afe210a7`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3486355dbac6d4cb52a1fb1fcd4e5f56919b98e7641f2141237fa8740377728e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3d9b71e8f69fdd20848ac97d9298152adca5338a72b7b5b18696779a3ba2b5`

```dockerfile
```

-	Layers:
	-	`sha256:cbeed85d56a1efd879d6fd443ce9cc2ed8a3e16aac619dd329edfa745aa63942`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:8745a6efb4d3d761664bcceb450c5cea0da7ac490688df09de61189339b57cac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:0c7dc14e63e6b5d5810d752ca28bb24c0fb6552971a19514d914bceac93f44e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204546084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2aafc8bcd7da81efe8c1ab85cb9fba3b9cab375dccf13c0e9236eb73383d75d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfab47cf5cf3ca9941151a55bb2cb9437b2cc0c0d6115831f174327eedc2a69`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 7.2 MB (7151721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43eab875d7fbca96a916fd1ba2f7c37a188a352643300198235618c41cc771a`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 167.0 MB (166991745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81414aef9f4936ed3818cecd2ac6bbff5e6da3e3d43982e37193209c09b7b12c`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc61bee4cda5c74dc726cf66a2abf6a8e0bdb1c9f5f9782219f7261c2bdf593a`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dec9e3885bcee13eb8c84219b1b5c74c45df3be44af4071fdb9b3f1a5e11b12`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146f8cb5454888fb18a7ec2c09d7c641e0d4ad0f462448ce9b41a3662bd36079`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f0eeb8fc96a82e7d207eda20f28aa4681f1f1b263cfea769ce3096afe210a7`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3486355dbac6d4cb52a1fb1fcd4e5f56919b98e7641f2141237fa8740377728e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3d9b71e8f69fdd20848ac97d9298152adca5338a72b7b5b18696779a3ba2b5`

```dockerfile
```

-	Layers:
	-	`sha256:cbeed85d56a1efd879d6fd443ce9cc2ed8a3e16aac619dd329edfa745aa63942`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:8745a6efb4d3d761664bcceb450c5cea0da7ac490688df09de61189339b57cac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:0c7dc14e63e6b5d5810d752ca28bb24c0fb6552971a19514d914bceac93f44e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204546084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2aafc8bcd7da81efe8c1ab85cb9fba3b9cab375dccf13c0e9236eb73383d75d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfab47cf5cf3ca9941151a55bb2cb9437b2cc0c0d6115831f174327eedc2a69`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 7.2 MB (7151721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43eab875d7fbca96a916fd1ba2f7c37a188a352643300198235618c41cc771a`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 167.0 MB (166991745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81414aef9f4936ed3818cecd2ac6bbff5e6da3e3d43982e37193209c09b7b12c`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc61bee4cda5c74dc726cf66a2abf6a8e0bdb1c9f5f9782219f7261c2bdf593a`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dec9e3885bcee13eb8c84219b1b5c74c45df3be44af4071fdb9b3f1a5e11b12`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146f8cb5454888fb18a7ec2c09d7c641e0d4ad0f462448ce9b41a3662bd36079`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f0eeb8fc96a82e7d207eda20f28aa4681f1f1b263cfea769ce3096afe210a7`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3486355dbac6d4cb52a1fb1fcd4e5f56919b98e7641f2141237fa8740377728e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3d9b71e8f69fdd20848ac97d9298152adca5338a72b7b5b18696779a3ba2b5`

```dockerfile
```

-	Layers:
	-	`sha256:cbeed85d56a1efd879d6fd443ce9cc2ed8a3e16aac619dd329edfa745aa63942`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:8745a6efb4d3d761664bcceb450c5cea0da7ac490688df09de61189339b57cac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0c7dc14e63e6b5d5810d752ca28bb24c0fb6552971a19514d914bceac93f44e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.5 MB (204546084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2aafc8bcd7da81efe8c1ab85cb9fba3b9cab375dccf13c0e9236eb73383d75d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 28 Mar 2025 10:04:18 GMT
ARG RELEASE
# Fri, 28 Mar 2025 10:04:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 28 Mar 2025 10:04:18 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 28 Mar 2025 10:04:18 GMT
ADD file:433cf0b8353e08be3a6582ad5947c57a66bdbb842ed3095246a1ff6876d157f1 in / 
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:30a9c22ae099393b0131322d7f50d8a9d7cd06c5e518cd27a19ac960a4d0aba3`  
		Last Modified: Mon, 07 Apr 2025 08:26:26 GMT  
		Size: 29.5 MB (29532365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecfab47cf5cf3ca9941151a55bb2cb9437b2cc0c0d6115831f174327eedc2a69`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 7.2 MB (7151721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43eab875d7fbca96a916fd1ba2f7c37a188a352643300198235618c41cc771a`  
		Last Modified: Wed, 09 Apr 2025 01:12:15 GMT  
		Size: 167.0 MB (166991745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81414aef9f4936ed3818cecd2ac6bbff5e6da3e3d43982e37193209c09b7b12c`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc61bee4cda5c74dc726cf66a2abf6a8e0bdb1c9f5f9782219f7261c2bdf593a`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dec9e3885bcee13eb8c84219b1b5c74c45df3be44af4071fdb9b3f1a5e11b12`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146f8cb5454888fb18a7ec2c09d7c641e0d4ad0f462448ce9b41a3662bd36079`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66f0eeb8fc96a82e7d207eda20f28aa4681f1f1b263cfea769ce3096afe210a7`  
		Last Modified: Wed, 09 Apr 2025 01:12:14 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3486355dbac6d4cb52a1fb1fcd4e5f56919b98e7641f2141237fa8740377728e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3d9b71e8f69fdd20848ac97d9298152adca5338a72b7b5b18696779a3ba2b5`

```dockerfile
```

-	Layers:
	-	`sha256:cbeed85d56a1efd879d6fd443ce9cc2ed8a3e16aac619dd329edfa745aa63942`  
		Last Modified: Wed, 09 Apr 2025 01:12:13 GMT  
		Size: 26.5 KB (26484 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a94ae2c5d5dc0c1e8bc76c852700d0183fb1b7f26c8ebd09631453651b32e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.0 MB (192049819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd3c7addf89b2a49d702ff7c1e0e8292a510c2e1d97cbd5986509369d41f717`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:32:14 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:32:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:32:14 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:32:17 GMT
ADD file:905ede4ce5ed6db0abca06b5e342a3784cd1f328e2cdc1f59f6d556f6382650d in / 
# Sun, 26 Jan 2025 05:32:17 GMT
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
ARG VERSION=25.3.2.39
# Fri, 28 Mar 2025 10:04:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 28 Mar 2025 10:04:18 GMT
ENV LANG=en_US.UTF-8
# Fri, 28 Mar 2025 10:04:18 GMT
ENV TZ=UTC
# Fri, 28 Mar 2025 10:04:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.2.39 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Sun, 26 Jan 2025 07:02:08 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e2818155487f77355a847a39e694a96cd6d65f56c3495177226d7f5a35a0e3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 7.1 MB (7121914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddeb8c1c1668b1eb613370c4beaa81279f3b4a5ecaea160af3c3d62d0c856f1e`  
		Last Modified: Fri, 28 Mar 2025 21:06:12 GMT  
		Size: 156.7 MB (156699477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293f2f6abd2cb785e163ef6cbbbef53d972335f8b4e12493f93f77cd6a47492f`  
		Last Modified: Fri, 28 Mar 2025 21:06:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7baaf3c769a536ef79817808e5b5a3a98971b5a93eac3b3ffb4bb4c1d512f1da`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae5954d55c733a756963cdb589b33b32956e9895832963a9f90ef3a8246b54c3`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c983b5d363a9f935241fff0db4f44aff1fb3b006bad76a5f129ad377c0f03e`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313edb84484a6be455310c639511a7a7cd1cc210540aa2f071264a7421e052a0`  
		Last Modified: Fri, 28 Mar 2025 21:06:10 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e8380e9eb089c63b13e743c6d2a007fd0d188d1ce79d96eaf605ae1893e1063e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a0fc1571ab201ba55de6669aef907c157be1a949d336c722691943693dbf0`

```dockerfile
```

-	Layers:
	-	`sha256:bdda46dfedfa7aa68a2c4f503af7e5e64dd86f3483d2c66109bfa8ea3444cb5d`  
		Last Modified: Fri, 28 Mar 2025 21:06:09 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json
