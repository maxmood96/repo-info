<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.10`](#clickhouse2510)
-	[`clickhouse:25.10-jammy`](#clickhouse2510-jammy)
-	[`clickhouse:25.10.2`](#clickhouse25102)
-	[`clickhouse:25.10.2-jammy`](#clickhouse25102-jammy)
-	[`clickhouse:25.10.2.65`](#clickhouse2510265)
-	[`clickhouse:25.10.2.65-jammy`](#clickhouse2510265-jammy)
-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.8`](#clickhouse2538)
-	[`clickhouse:25.3.8-jammy`](#clickhouse2538-jammy)
-	[`clickhouse:25.3.8.23`](#clickhouse253823)
-	[`clickhouse:25.3.8.23-jammy`](#clickhouse253823-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.11`](#clickhouse25811)
-	[`clickhouse:25.8.11-jammy`](#clickhouse25811-jammy)
-	[`clickhouse:25.8.11.66`](#clickhouse2581166)
-	[`clickhouse:25.8.11.66-jammy`](#clickhouse2581166-jammy)
-	[`clickhouse:25.9`](#clickhouse259)
-	[`clickhouse:25.9-jammy`](#clickhouse259-jammy)
-	[`clickhouse:25.9.5`](#clickhouse2595)
-	[`clickhouse:25.9.5-jammy`](#clickhouse2595-jammy)
-	[`clickhouse:25.9.5.21`](#clickhouse259521)
-	[`clickhouse:25.9.5.21-jammy`](#clickhouse259521-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.10`

```console
$ docker pull clickhouse@sha256:f6c922be45e9839765fa7fe54d8fd07e7586e582846148d4fbd2411cfb225ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:e01ad927d22e7572a36afe57ca4ca6d7bc8db5d5aa457e9ccc55553989467d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231983028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed18c4d38249cc17224a423ebaa194a45a9879a04ffcc3efbfcad4a7e7cb040e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 19:15:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 19:15:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 19:15:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 19:15:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 19:15:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 19:15:42 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 19:15:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 19:16:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 19:16:08 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 19:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 19:16:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 19:16:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 19:16:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88985e9509ea1629450be2ab8c89146c92ea1cf4931088415b9ff8f449d4b8`  
		Last Modified: Thu, 13 Nov 2025 19:16:38 GMT  
		Size: 7.6 MB (7598439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f06b432c622ea0d9e76cf2e1432beb57e8099347beccb92d5901c44394d867`  
		Last Modified: Thu, 13 Nov 2025 19:24:13 GMT  
		Size: 194.0 MB (193977753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e3ebf007834804cf2fd69e7dcfe475383495c90a6ac018d22a04934ae8deca`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7dbe6c3ddb7197a037aa79c13d3413eb7519c78ff807343b057607e5f3ec46`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88056c2b344343d9ddfe0954ca13142dc996db2762a223ea06389161da8ae559`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524cc5ac590815922ccd84509b08c4ce30328d8491bfa9842fef50a3c9983e9`  
		Last Modified: Thu, 13 Nov 2025 19:16:36 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdbac4f40935b5ea01f16ef1fa1f782e492077f9a8dc39433bbd8afc3b56cdd`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e1d1f753653f1599f8d5f1c7b8e7bad43db50d7cfe829492a20b15d56bf81de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66664220cb146f7442a46a9fac3cae55dfb354386f11cb01777a6402b4a63e0`

```dockerfile
```

-	Layers:
	-	`sha256:d08aa577095fcdbfc4e7d98d089ae82582b0ee863182d769ea728dabba82a8c2`  
		Last Modified: Thu, 13 Nov 2025 22:49:23 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b59dd1ce4e937b016f358760aec66484b9d1ea017d0989f18ee2ec1d154326d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216505212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8a3f952674749e2c89d33889035b2a2a77f004233cd8972010c787390fa1c6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 19:15:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 19:15:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 19:15:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 19:15:34 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 19:15:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 19:15:34 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 19:15:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 19:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 19:16:00 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 19:16:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 19:16:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 19:16:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 19:16:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2fa1f30a833b6e9bf8e350076296e47b08ee1ffd285d54dc19ea7c6530dcd7`  
		Last Modified: Thu, 13 Nov 2025 19:16:30 GMT  
		Size: 7.6 MB (7576778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ddd361ee8ed98381de53c1966c215a47da7ee9dde28c8c09f054874d689b7d`  
		Last Modified: Thu, 13 Nov 2025 22:49:54 GMT  
		Size: 180.7 MB (180675306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4fe93b494f11751b7faae52f9c7f5243d91db541eab1a5f002c56abec049eb`  
		Last Modified: Thu, 13 Nov 2025 19:16:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7152fb6c08ae5cf804a0c6e73c0b37c0c0f15aa85e22e99b8e11f3c3958f13`  
		Last Modified: Thu, 13 Nov 2025 19:16:28 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72536613ce3993059c4aae363c7fd6b4b181282386c4fe1c9e27736690b30dd4`  
		Last Modified: Thu, 13 Nov 2025 19:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57bf763c9fdf56b96abda80c1eb82107a28e79544f1697c4f5c10e89517057b`  
		Last Modified: Thu, 13 Nov 2025 19:16:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c184d7f57e7058688e86fad093b4f63fa671baa0417191603dca9c35136c769`  
		Last Modified: Thu, 13 Nov 2025 19:16:28 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8ca9c6905562a6cb1de62190654202b87c25376a841df82745a5b758f1f70079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20f752b981d0d8b7359ae59f306f7847c7240f4b805bbbd6c3cda40c4c00c94`

```dockerfile
```

-	Layers:
	-	`sha256:be6fbcfc6db556e0e6c963eff3542fd7f0a591dc8e04312ddd9c3c305eb19033`  
		Last Modified: Thu, 13 Nov 2025 22:49:26 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10-jammy`

```console
$ docker pull clickhouse@sha256:f6c922be45e9839765fa7fe54d8fd07e7586e582846148d4fbd2411cfb225ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e01ad927d22e7572a36afe57ca4ca6d7bc8db5d5aa457e9ccc55553989467d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231983028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed18c4d38249cc17224a423ebaa194a45a9879a04ffcc3efbfcad4a7e7cb040e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 19:15:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 19:15:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 19:15:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 19:15:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 19:15:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 19:15:42 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 19:15:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 19:16:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 19:16:08 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 19:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 19:16:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 19:16:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 19:16:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88985e9509ea1629450be2ab8c89146c92ea1cf4931088415b9ff8f449d4b8`  
		Last Modified: Thu, 13 Nov 2025 19:16:38 GMT  
		Size: 7.6 MB (7598439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f06b432c622ea0d9e76cf2e1432beb57e8099347beccb92d5901c44394d867`  
		Last Modified: Thu, 13 Nov 2025 19:24:13 GMT  
		Size: 194.0 MB (193977753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e3ebf007834804cf2fd69e7dcfe475383495c90a6ac018d22a04934ae8deca`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7dbe6c3ddb7197a037aa79c13d3413eb7519c78ff807343b057607e5f3ec46`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88056c2b344343d9ddfe0954ca13142dc996db2762a223ea06389161da8ae559`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524cc5ac590815922ccd84509b08c4ce30328d8491bfa9842fef50a3c9983e9`  
		Last Modified: Thu, 13 Nov 2025 19:16:36 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdbac4f40935b5ea01f16ef1fa1f782e492077f9a8dc39433bbd8afc3b56cdd`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e1d1f753653f1599f8d5f1c7b8e7bad43db50d7cfe829492a20b15d56bf81de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66664220cb146f7442a46a9fac3cae55dfb354386f11cb01777a6402b4a63e0`

```dockerfile
```

-	Layers:
	-	`sha256:d08aa577095fcdbfc4e7d98d089ae82582b0ee863182d769ea728dabba82a8c2`  
		Last Modified: Thu, 13 Nov 2025 22:49:23 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b59dd1ce4e937b016f358760aec66484b9d1ea017d0989f18ee2ec1d154326d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216505212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8a3f952674749e2c89d33889035b2a2a77f004233cd8972010c787390fa1c6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 19:15:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 19:15:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 19:15:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 19:15:34 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 19:15:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 19:15:34 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 19:15:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 19:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 19:16:00 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 19:16:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 19:16:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 19:16:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 19:16:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2fa1f30a833b6e9bf8e350076296e47b08ee1ffd285d54dc19ea7c6530dcd7`  
		Last Modified: Thu, 13 Nov 2025 19:16:30 GMT  
		Size: 7.6 MB (7576778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ddd361ee8ed98381de53c1966c215a47da7ee9dde28c8c09f054874d689b7d`  
		Last Modified: Thu, 13 Nov 2025 22:49:54 GMT  
		Size: 180.7 MB (180675306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4fe93b494f11751b7faae52f9c7f5243d91db541eab1a5f002c56abec049eb`  
		Last Modified: Thu, 13 Nov 2025 19:16:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7152fb6c08ae5cf804a0c6e73c0b37c0c0f15aa85e22e99b8e11f3c3958f13`  
		Last Modified: Thu, 13 Nov 2025 19:16:28 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72536613ce3993059c4aae363c7fd6b4b181282386c4fe1c9e27736690b30dd4`  
		Last Modified: Thu, 13 Nov 2025 19:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57bf763c9fdf56b96abda80c1eb82107a28e79544f1697c4f5c10e89517057b`  
		Last Modified: Thu, 13 Nov 2025 19:16:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c184d7f57e7058688e86fad093b4f63fa671baa0417191603dca9c35136c769`  
		Last Modified: Thu, 13 Nov 2025 19:16:28 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8ca9c6905562a6cb1de62190654202b87c25376a841df82745a5b758f1f70079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20f752b981d0d8b7359ae59f306f7847c7240f4b805bbbd6c3cda40c4c00c94`

```dockerfile
```

-	Layers:
	-	`sha256:be6fbcfc6db556e0e6c963eff3542fd7f0a591dc8e04312ddd9c3c305eb19033`  
		Last Modified: Thu, 13 Nov 2025 22:49:26 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10.2`

```console
$ docker pull clickhouse@sha256:f6c922be45e9839765fa7fe54d8fd07e7586e582846148d4fbd2411cfb225ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:e01ad927d22e7572a36afe57ca4ca6d7bc8db5d5aa457e9ccc55553989467d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231983028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed18c4d38249cc17224a423ebaa194a45a9879a04ffcc3efbfcad4a7e7cb040e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 19:15:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 19:15:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 19:15:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 19:15:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 19:15:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 19:15:42 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 19:15:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 19:16:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 19:16:08 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 19:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 19:16:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 19:16:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 19:16:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88985e9509ea1629450be2ab8c89146c92ea1cf4931088415b9ff8f449d4b8`  
		Last Modified: Thu, 13 Nov 2025 19:16:38 GMT  
		Size: 7.6 MB (7598439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f06b432c622ea0d9e76cf2e1432beb57e8099347beccb92d5901c44394d867`  
		Last Modified: Thu, 13 Nov 2025 19:24:13 GMT  
		Size: 194.0 MB (193977753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e3ebf007834804cf2fd69e7dcfe475383495c90a6ac018d22a04934ae8deca`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7dbe6c3ddb7197a037aa79c13d3413eb7519c78ff807343b057607e5f3ec46`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88056c2b344343d9ddfe0954ca13142dc996db2762a223ea06389161da8ae559`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524cc5ac590815922ccd84509b08c4ce30328d8491bfa9842fef50a3c9983e9`  
		Last Modified: Thu, 13 Nov 2025 19:16:36 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdbac4f40935b5ea01f16ef1fa1f782e492077f9a8dc39433bbd8afc3b56cdd`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e1d1f753653f1599f8d5f1c7b8e7bad43db50d7cfe829492a20b15d56bf81de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66664220cb146f7442a46a9fac3cae55dfb354386f11cb01777a6402b4a63e0`

```dockerfile
```

-	Layers:
	-	`sha256:d08aa577095fcdbfc4e7d98d089ae82582b0ee863182d769ea728dabba82a8c2`  
		Last Modified: Thu, 13 Nov 2025 22:49:23 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b59dd1ce4e937b016f358760aec66484b9d1ea017d0989f18ee2ec1d154326d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216505212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8a3f952674749e2c89d33889035b2a2a77f004233cd8972010c787390fa1c6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 19:15:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 19:15:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 19:15:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 19:15:34 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 19:15:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 19:15:34 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 19:15:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 19:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 19:16:00 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 19:16:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 19:16:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 19:16:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 19:16:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2fa1f30a833b6e9bf8e350076296e47b08ee1ffd285d54dc19ea7c6530dcd7`  
		Last Modified: Thu, 13 Nov 2025 19:16:30 GMT  
		Size: 7.6 MB (7576778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ddd361ee8ed98381de53c1966c215a47da7ee9dde28c8c09f054874d689b7d`  
		Last Modified: Thu, 13 Nov 2025 22:49:54 GMT  
		Size: 180.7 MB (180675306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4fe93b494f11751b7faae52f9c7f5243d91db541eab1a5f002c56abec049eb`  
		Last Modified: Thu, 13 Nov 2025 19:16:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7152fb6c08ae5cf804a0c6e73c0b37c0c0f15aa85e22e99b8e11f3c3958f13`  
		Last Modified: Thu, 13 Nov 2025 19:16:28 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72536613ce3993059c4aae363c7fd6b4b181282386c4fe1c9e27736690b30dd4`  
		Last Modified: Thu, 13 Nov 2025 19:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57bf763c9fdf56b96abda80c1eb82107a28e79544f1697c4f5c10e89517057b`  
		Last Modified: Thu, 13 Nov 2025 19:16:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c184d7f57e7058688e86fad093b4f63fa671baa0417191603dca9c35136c769`  
		Last Modified: Thu, 13 Nov 2025 19:16:28 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8ca9c6905562a6cb1de62190654202b87c25376a841df82745a5b758f1f70079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20f752b981d0d8b7359ae59f306f7847c7240f4b805bbbd6c3cda40c4c00c94`

```dockerfile
```

-	Layers:
	-	`sha256:be6fbcfc6db556e0e6c963eff3542fd7f0a591dc8e04312ddd9c3c305eb19033`  
		Last Modified: Thu, 13 Nov 2025 22:49:26 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10.2-jammy`

```console
$ docker pull clickhouse@sha256:f6c922be45e9839765fa7fe54d8fd07e7586e582846148d4fbd2411cfb225ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e01ad927d22e7572a36afe57ca4ca6d7bc8db5d5aa457e9ccc55553989467d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231983028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed18c4d38249cc17224a423ebaa194a45a9879a04ffcc3efbfcad4a7e7cb040e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 19:15:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 19:15:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 19:15:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 19:15:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 19:15:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 19:15:42 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 19:15:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 19:16:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 19:16:08 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 19:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 19:16:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 19:16:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 19:16:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88985e9509ea1629450be2ab8c89146c92ea1cf4931088415b9ff8f449d4b8`  
		Last Modified: Thu, 13 Nov 2025 19:16:38 GMT  
		Size: 7.6 MB (7598439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f06b432c622ea0d9e76cf2e1432beb57e8099347beccb92d5901c44394d867`  
		Last Modified: Thu, 13 Nov 2025 19:24:13 GMT  
		Size: 194.0 MB (193977753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e3ebf007834804cf2fd69e7dcfe475383495c90a6ac018d22a04934ae8deca`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7dbe6c3ddb7197a037aa79c13d3413eb7519c78ff807343b057607e5f3ec46`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88056c2b344343d9ddfe0954ca13142dc996db2762a223ea06389161da8ae559`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524cc5ac590815922ccd84509b08c4ce30328d8491bfa9842fef50a3c9983e9`  
		Last Modified: Thu, 13 Nov 2025 19:16:36 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdbac4f40935b5ea01f16ef1fa1f782e492077f9a8dc39433bbd8afc3b56cdd`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e1d1f753653f1599f8d5f1c7b8e7bad43db50d7cfe829492a20b15d56bf81de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66664220cb146f7442a46a9fac3cae55dfb354386f11cb01777a6402b4a63e0`

```dockerfile
```

-	Layers:
	-	`sha256:d08aa577095fcdbfc4e7d98d089ae82582b0ee863182d769ea728dabba82a8c2`  
		Last Modified: Thu, 13 Nov 2025 22:49:23 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b59dd1ce4e937b016f358760aec66484b9d1ea017d0989f18ee2ec1d154326d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216505212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8a3f952674749e2c89d33889035b2a2a77f004233cd8972010c787390fa1c6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 19:15:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 19:15:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 19:15:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 19:15:34 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 19:15:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 19:15:34 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 19:15:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 19:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 19:16:00 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 19:16:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 19:16:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 19:16:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 19:16:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2fa1f30a833b6e9bf8e350076296e47b08ee1ffd285d54dc19ea7c6530dcd7`  
		Last Modified: Thu, 13 Nov 2025 19:16:30 GMT  
		Size: 7.6 MB (7576778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ddd361ee8ed98381de53c1966c215a47da7ee9dde28c8c09f054874d689b7d`  
		Last Modified: Thu, 13 Nov 2025 22:49:54 GMT  
		Size: 180.7 MB (180675306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4fe93b494f11751b7faae52f9c7f5243d91db541eab1a5f002c56abec049eb`  
		Last Modified: Thu, 13 Nov 2025 19:16:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7152fb6c08ae5cf804a0c6e73c0b37c0c0f15aa85e22e99b8e11f3c3958f13`  
		Last Modified: Thu, 13 Nov 2025 19:16:28 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72536613ce3993059c4aae363c7fd6b4b181282386c4fe1c9e27736690b30dd4`  
		Last Modified: Thu, 13 Nov 2025 19:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57bf763c9fdf56b96abda80c1eb82107a28e79544f1697c4f5c10e89517057b`  
		Last Modified: Thu, 13 Nov 2025 19:16:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c184d7f57e7058688e86fad093b4f63fa671baa0417191603dca9c35136c769`  
		Last Modified: Thu, 13 Nov 2025 19:16:28 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8ca9c6905562a6cb1de62190654202b87c25376a841df82745a5b758f1f70079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20f752b981d0d8b7359ae59f306f7847c7240f4b805bbbd6c3cda40c4c00c94`

```dockerfile
```

-	Layers:
	-	`sha256:be6fbcfc6db556e0e6c963eff3542fd7f0a591dc8e04312ddd9c3c305eb19033`  
		Last Modified: Thu, 13 Nov 2025 22:49:26 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10.2.65`

```console
$ docker pull clickhouse@sha256:f6c922be45e9839765fa7fe54d8fd07e7586e582846148d4fbd2411cfb225ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10.2.65` - linux; amd64

```console
$ docker pull clickhouse@sha256:e01ad927d22e7572a36afe57ca4ca6d7bc8db5d5aa457e9ccc55553989467d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231983028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed18c4d38249cc17224a423ebaa194a45a9879a04ffcc3efbfcad4a7e7cb040e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 19:15:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 19:15:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 19:15:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 19:15:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 19:15:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 19:15:42 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 19:15:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 19:16:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 19:16:08 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 19:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 19:16:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 19:16:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 19:16:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88985e9509ea1629450be2ab8c89146c92ea1cf4931088415b9ff8f449d4b8`  
		Last Modified: Thu, 13 Nov 2025 19:16:38 GMT  
		Size: 7.6 MB (7598439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f06b432c622ea0d9e76cf2e1432beb57e8099347beccb92d5901c44394d867`  
		Last Modified: Thu, 13 Nov 2025 19:24:13 GMT  
		Size: 194.0 MB (193977753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e3ebf007834804cf2fd69e7dcfe475383495c90a6ac018d22a04934ae8deca`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7dbe6c3ddb7197a037aa79c13d3413eb7519c78ff807343b057607e5f3ec46`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88056c2b344343d9ddfe0954ca13142dc996db2762a223ea06389161da8ae559`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524cc5ac590815922ccd84509b08c4ce30328d8491bfa9842fef50a3c9983e9`  
		Last Modified: Thu, 13 Nov 2025 19:16:36 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdbac4f40935b5ea01f16ef1fa1f782e492077f9a8dc39433bbd8afc3b56cdd`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.2.65` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e1d1f753653f1599f8d5f1c7b8e7bad43db50d7cfe829492a20b15d56bf81de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66664220cb146f7442a46a9fac3cae55dfb354386f11cb01777a6402b4a63e0`

```dockerfile
```

-	Layers:
	-	`sha256:d08aa577095fcdbfc4e7d98d089ae82582b0ee863182d769ea728dabba82a8c2`  
		Last Modified: Thu, 13 Nov 2025 22:49:23 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10.2.65` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b59dd1ce4e937b016f358760aec66484b9d1ea017d0989f18ee2ec1d154326d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216505212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8a3f952674749e2c89d33889035b2a2a77f004233cd8972010c787390fa1c6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 19:15:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 19:15:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 19:15:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 19:15:34 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 19:15:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 19:15:34 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 19:15:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 19:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 19:16:00 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 19:16:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 19:16:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 19:16:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 19:16:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2fa1f30a833b6e9bf8e350076296e47b08ee1ffd285d54dc19ea7c6530dcd7`  
		Last Modified: Thu, 13 Nov 2025 19:16:30 GMT  
		Size: 7.6 MB (7576778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ddd361ee8ed98381de53c1966c215a47da7ee9dde28c8c09f054874d689b7d`  
		Last Modified: Thu, 13 Nov 2025 22:49:54 GMT  
		Size: 180.7 MB (180675306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4fe93b494f11751b7faae52f9c7f5243d91db541eab1a5f002c56abec049eb`  
		Last Modified: Thu, 13 Nov 2025 19:16:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7152fb6c08ae5cf804a0c6e73c0b37c0c0f15aa85e22e99b8e11f3c3958f13`  
		Last Modified: Thu, 13 Nov 2025 19:16:28 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72536613ce3993059c4aae363c7fd6b4b181282386c4fe1c9e27736690b30dd4`  
		Last Modified: Thu, 13 Nov 2025 19:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57bf763c9fdf56b96abda80c1eb82107a28e79544f1697c4f5c10e89517057b`  
		Last Modified: Thu, 13 Nov 2025 19:16:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c184d7f57e7058688e86fad093b4f63fa671baa0417191603dca9c35136c769`  
		Last Modified: Thu, 13 Nov 2025 19:16:28 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.2.65` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8ca9c6905562a6cb1de62190654202b87c25376a841df82745a5b758f1f70079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20f752b981d0d8b7359ae59f306f7847c7240f4b805bbbd6c3cda40c4c00c94`

```dockerfile
```

-	Layers:
	-	`sha256:be6fbcfc6db556e0e6c963eff3542fd7f0a591dc8e04312ddd9c3c305eb19033`  
		Last Modified: Thu, 13 Nov 2025 22:49:26 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10.2.65-jammy`

```console
$ docker pull clickhouse@sha256:f6c922be45e9839765fa7fe54d8fd07e7586e582846148d4fbd2411cfb225ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10.2.65-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e01ad927d22e7572a36afe57ca4ca6d7bc8db5d5aa457e9ccc55553989467d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231983028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed18c4d38249cc17224a423ebaa194a45a9879a04ffcc3efbfcad4a7e7cb040e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 19:15:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 19:15:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 19:15:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 19:15:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 19:15:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 19:15:42 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 19:15:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 19:16:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 19:16:08 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 19:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 19:16:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 19:16:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 19:16:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88985e9509ea1629450be2ab8c89146c92ea1cf4931088415b9ff8f449d4b8`  
		Last Modified: Thu, 13 Nov 2025 19:16:38 GMT  
		Size: 7.6 MB (7598439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f06b432c622ea0d9e76cf2e1432beb57e8099347beccb92d5901c44394d867`  
		Last Modified: Thu, 13 Nov 2025 19:24:13 GMT  
		Size: 194.0 MB (193977753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e3ebf007834804cf2fd69e7dcfe475383495c90a6ac018d22a04934ae8deca`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7dbe6c3ddb7197a037aa79c13d3413eb7519c78ff807343b057607e5f3ec46`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88056c2b344343d9ddfe0954ca13142dc996db2762a223ea06389161da8ae559`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524cc5ac590815922ccd84509b08c4ce30328d8491bfa9842fef50a3c9983e9`  
		Last Modified: Thu, 13 Nov 2025 19:16:36 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdbac4f40935b5ea01f16ef1fa1f782e492077f9a8dc39433bbd8afc3b56cdd`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.2.65-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e1d1f753653f1599f8d5f1c7b8e7bad43db50d7cfe829492a20b15d56bf81de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66664220cb146f7442a46a9fac3cae55dfb354386f11cb01777a6402b4a63e0`

```dockerfile
```

-	Layers:
	-	`sha256:d08aa577095fcdbfc4e7d98d089ae82582b0ee863182d769ea728dabba82a8c2`  
		Last Modified: Thu, 13 Nov 2025 22:49:23 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10.2.65-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b59dd1ce4e937b016f358760aec66484b9d1ea017d0989f18ee2ec1d154326d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216505212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8a3f952674749e2c89d33889035b2a2a77f004233cd8972010c787390fa1c6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 19:15:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 19:15:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 19:15:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 19:15:34 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 19:15:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 19:15:34 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 19:15:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 19:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 19:16:00 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 19:16:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 19:16:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 19:16:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 19:16:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2fa1f30a833b6e9bf8e350076296e47b08ee1ffd285d54dc19ea7c6530dcd7`  
		Last Modified: Thu, 13 Nov 2025 19:16:30 GMT  
		Size: 7.6 MB (7576778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ddd361ee8ed98381de53c1966c215a47da7ee9dde28c8c09f054874d689b7d`  
		Last Modified: Thu, 13 Nov 2025 22:49:54 GMT  
		Size: 180.7 MB (180675306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4fe93b494f11751b7faae52f9c7f5243d91db541eab1a5f002c56abec049eb`  
		Last Modified: Thu, 13 Nov 2025 19:16:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7152fb6c08ae5cf804a0c6e73c0b37c0c0f15aa85e22e99b8e11f3c3958f13`  
		Last Modified: Thu, 13 Nov 2025 19:16:28 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72536613ce3993059c4aae363c7fd6b4b181282386c4fe1c9e27736690b30dd4`  
		Last Modified: Thu, 13 Nov 2025 19:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57bf763c9fdf56b96abda80c1eb82107a28e79544f1697c4f5c10e89517057b`  
		Last Modified: Thu, 13 Nov 2025 19:16:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c184d7f57e7058688e86fad093b4f63fa671baa0417191603dca9c35136c769`  
		Last Modified: Thu, 13 Nov 2025 19:16:28 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10.2.65-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8ca9c6905562a6cb1de62190654202b87c25376a841df82745a5b758f1f70079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20f752b981d0d8b7359ae59f306f7847c7240f4b805bbbd6c3cda40c4c00c94`

```dockerfile
```

-	Layers:
	-	`sha256:be6fbcfc6db556e0e6c963eff3542fd7f0a591dc8e04312ddd9c3c305eb19033`  
		Last Modified: Thu, 13 Nov 2025 22:49:26 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:c5cc010095c4e55fd68d436d265e6f1acad9db83b427956649d30a6172349b76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:31c8de206ef101f9dd11beb0e767115d847fc0cf069e8d5eba607a241721772e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205506762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a460c8827aeb6bcabacc4889fdc06fc0e73de0543c391cb9f7f67584d0662d93`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:53:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:53:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:53:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:53:56 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:53:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:53:56 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 23:53:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:54:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:54:18 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:54:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:54:18 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:54:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:54:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a13d4703704b355c7dd6ab15bd271553dad0c7496ce08ee2c941af8fb865c35`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 7.2 MB (7151576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f90441afda07bd8941850b54829b6f6f38e0bbbc407181dfdee9b2ee70749`  
		Last Modified: Fri, 31 Oct 2025 00:49:47 GMT  
		Size: 167.9 MB (167948122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9504161cb31200125acc034a48877b4c87b8fa8f50a4a5491449b10866d177fc`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d95c7118f545b826eb68e4f581dc725653158afb5e534015fcc52cf9a1e623b`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecd84b0da21b7ac9261d5a7834e43f07293b4627e08e96992b5108f262b3d56`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be103278dbbc68f2584ce11b33141c0f2e095cf4885014f45e11208b6bb10b21`  
		Last Modified: Thu, 30 Oct 2025 23:54:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cc7bd24d0aa86274b9bd038fb37b46eb6e75eb1b0d2d831423eab137e82ea5`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2ee5518f075e453f91fcb34af0861515ee8b59aea56dd0152f079eb9fe4fead5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15158c1ba0b4eb17eac23691fdccfe35bc9d7845537d6da87a77c8a403a07fbb`

```dockerfile
```

-	Layers:
	-	`sha256:3a8e8badc211cc619a524220ae2c9d20a7a33c52a4f4413817a01d27fbad4e64`  
		Last Modified: Fri, 31 Oct 2025 00:49:18 GMT  
		Size: 25.2 KB (25220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4aed478be3bb7097bdc1debd209b178ecf42c37d7210d4e9648631b2579a94b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192983547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d35bbed0c2650693ae9c9d44da2e89dc8b42aba620b35d6de0c43ea3e01810`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:21:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:49 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 21:21:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:16 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3307f657683d186c6205717bfb85eb558ca87cc25b5ec9e9e0f2a3afab8238ae`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.1 MB (7127222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53827a5efe698f075c2a8f84f9e910521f6c849d4e663f8bcda6c1d682998277`  
		Last Modified: Thu, 30 Oct 2025 21:49:52 GMT  
		Size: 157.6 MB (157602973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c75edbbc000a53843b7b15ecb1d209d70d5d24a28598e3ca4b43e07e2115257`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe72d435c20e30ef6acfa667b15604b77c558491fc9f904b620510017cde658`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6a66cb23d300a47ce566678ece81a979d365580649b98d8c909fff1cda80e2`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f337947838d1b535c45aeb37402ed7a290dcfca3e3858494873cc04ab3e63`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314c2d04e787243b12ffabf5f69c468c59cd5a03651b8956fe2db0894f3d63d1`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fa760c382c19e3ad290a49a7f9fcbc3da22211dbfaa1e668571cd3ffdd30a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea58f8008ecdd3d85019881850a1558ac37f38e694fe5712d42af495973d636`

```dockerfile
```

-	Layers:
	-	`sha256:0ae0b038ca2f160b52a976b7eaeccfa1cc67911433863762494a512c80ae316f`  
		Last Modified: Thu, 30 Oct 2025 21:49:22 GMT  
		Size: 25.4 KB (25407 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:c5cc010095c4e55fd68d436d265e6f1acad9db83b427956649d30a6172349b76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:31c8de206ef101f9dd11beb0e767115d847fc0cf069e8d5eba607a241721772e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205506762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a460c8827aeb6bcabacc4889fdc06fc0e73de0543c391cb9f7f67584d0662d93`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:53:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:53:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:53:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:53:56 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:53:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:53:56 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 23:53:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:54:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:54:18 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:54:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:54:18 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:54:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:54:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a13d4703704b355c7dd6ab15bd271553dad0c7496ce08ee2c941af8fb865c35`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 7.2 MB (7151576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f90441afda07bd8941850b54829b6f6f38e0bbbc407181dfdee9b2ee70749`  
		Last Modified: Fri, 31 Oct 2025 00:49:47 GMT  
		Size: 167.9 MB (167948122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9504161cb31200125acc034a48877b4c87b8fa8f50a4a5491449b10866d177fc`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d95c7118f545b826eb68e4f581dc725653158afb5e534015fcc52cf9a1e623b`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecd84b0da21b7ac9261d5a7834e43f07293b4627e08e96992b5108f262b3d56`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be103278dbbc68f2584ce11b33141c0f2e095cf4885014f45e11208b6bb10b21`  
		Last Modified: Thu, 30 Oct 2025 23:54:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cc7bd24d0aa86274b9bd038fb37b46eb6e75eb1b0d2d831423eab137e82ea5`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2ee5518f075e453f91fcb34af0861515ee8b59aea56dd0152f079eb9fe4fead5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15158c1ba0b4eb17eac23691fdccfe35bc9d7845537d6da87a77c8a403a07fbb`

```dockerfile
```

-	Layers:
	-	`sha256:3a8e8badc211cc619a524220ae2c9d20a7a33c52a4f4413817a01d27fbad4e64`  
		Last Modified: Fri, 31 Oct 2025 00:49:18 GMT  
		Size: 25.2 KB (25220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4aed478be3bb7097bdc1debd209b178ecf42c37d7210d4e9648631b2579a94b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192983547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d35bbed0c2650693ae9c9d44da2e89dc8b42aba620b35d6de0c43ea3e01810`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:21:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:49 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 21:21:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:16 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3307f657683d186c6205717bfb85eb558ca87cc25b5ec9e9e0f2a3afab8238ae`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.1 MB (7127222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53827a5efe698f075c2a8f84f9e910521f6c849d4e663f8bcda6c1d682998277`  
		Last Modified: Thu, 30 Oct 2025 21:49:52 GMT  
		Size: 157.6 MB (157602973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c75edbbc000a53843b7b15ecb1d209d70d5d24a28598e3ca4b43e07e2115257`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe72d435c20e30ef6acfa667b15604b77c558491fc9f904b620510017cde658`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6a66cb23d300a47ce566678ece81a979d365580649b98d8c909fff1cda80e2`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f337947838d1b535c45aeb37402ed7a290dcfca3e3858494873cc04ab3e63`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314c2d04e787243b12ffabf5f69c468c59cd5a03651b8956fe2db0894f3d63d1`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fa760c382c19e3ad290a49a7f9fcbc3da22211dbfaa1e668571cd3ffdd30a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea58f8008ecdd3d85019881850a1558ac37f38e694fe5712d42af495973d636`

```dockerfile
```

-	Layers:
	-	`sha256:0ae0b038ca2f160b52a976b7eaeccfa1cc67911433863762494a512c80ae316f`  
		Last Modified: Thu, 30 Oct 2025 21:49:22 GMT  
		Size: 25.4 KB (25407 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.8`

```console
$ docker pull clickhouse@sha256:c5cc010095c4e55fd68d436d265e6f1acad9db83b427956649d30a6172349b76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:31c8de206ef101f9dd11beb0e767115d847fc0cf069e8d5eba607a241721772e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205506762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a460c8827aeb6bcabacc4889fdc06fc0e73de0543c391cb9f7f67584d0662d93`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:53:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:53:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:53:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:53:56 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:53:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:53:56 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 23:53:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:54:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:54:18 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:54:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:54:18 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:54:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:54:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a13d4703704b355c7dd6ab15bd271553dad0c7496ce08ee2c941af8fb865c35`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 7.2 MB (7151576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f90441afda07bd8941850b54829b6f6f38e0bbbc407181dfdee9b2ee70749`  
		Last Modified: Fri, 31 Oct 2025 00:49:47 GMT  
		Size: 167.9 MB (167948122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9504161cb31200125acc034a48877b4c87b8fa8f50a4a5491449b10866d177fc`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d95c7118f545b826eb68e4f581dc725653158afb5e534015fcc52cf9a1e623b`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecd84b0da21b7ac9261d5a7834e43f07293b4627e08e96992b5108f262b3d56`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be103278dbbc68f2584ce11b33141c0f2e095cf4885014f45e11208b6bb10b21`  
		Last Modified: Thu, 30 Oct 2025 23:54:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cc7bd24d0aa86274b9bd038fb37b46eb6e75eb1b0d2d831423eab137e82ea5`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2ee5518f075e453f91fcb34af0861515ee8b59aea56dd0152f079eb9fe4fead5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15158c1ba0b4eb17eac23691fdccfe35bc9d7845537d6da87a77c8a403a07fbb`

```dockerfile
```

-	Layers:
	-	`sha256:3a8e8badc211cc619a524220ae2c9d20a7a33c52a4f4413817a01d27fbad4e64`  
		Last Modified: Fri, 31 Oct 2025 00:49:18 GMT  
		Size: 25.2 KB (25220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4aed478be3bb7097bdc1debd209b178ecf42c37d7210d4e9648631b2579a94b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192983547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d35bbed0c2650693ae9c9d44da2e89dc8b42aba620b35d6de0c43ea3e01810`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:21:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:49 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 21:21:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:16 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3307f657683d186c6205717bfb85eb558ca87cc25b5ec9e9e0f2a3afab8238ae`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.1 MB (7127222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53827a5efe698f075c2a8f84f9e910521f6c849d4e663f8bcda6c1d682998277`  
		Last Modified: Thu, 30 Oct 2025 21:49:52 GMT  
		Size: 157.6 MB (157602973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c75edbbc000a53843b7b15ecb1d209d70d5d24a28598e3ca4b43e07e2115257`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe72d435c20e30ef6acfa667b15604b77c558491fc9f904b620510017cde658`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6a66cb23d300a47ce566678ece81a979d365580649b98d8c909fff1cda80e2`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f337947838d1b535c45aeb37402ed7a290dcfca3e3858494873cc04ab3e63`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314c2d04e787243b12ffabf5f69c468c59cd5a03651b8956fe2db0894f3d63d1`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fa760c382c19e3ad290a49a7f9fcbc3da22211dbfaa1e668571cd3ffdd30a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea58f8008ecdd3d85019881850a1558ac37f38e694fe5712d42af495973d636`

```dockerfile
```

-	Layers:
	-	`sha256:0ae0b038ca2f160b52a976b7eaeccfa1cc67911433863762494a512c80ae316f`  
		Last Modified: Thu, 30 Oct 2025 21:49:22 GMT  
		Size: 25.4 KB (25407 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.8-jammy`

```console
$ docker pull clickhouse@sha256:c5cc010095c4e55fd68d436d265e6f1acad9db83b427956649d30a6172349b76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:31c8de206ef101f9dd11beb0e767115d847fc0cf069e8d5eba607a241721772e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205506762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a460c8827aeb6bcabacc4889fdc06fc0e73de0543c391cb9f7f67584d0662d93`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:53:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:53:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:53:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:53:56 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:53:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:53:56 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 23:53:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:54:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:54:18 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:54:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:54:18 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:54:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:54:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a13d4703704b355c7dd6ab15bd271553dad0c7496ce08ee2c941af8fb865c35`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 7.2 MB (7151576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f90441afda07bd8941850b54829b6f6f38e0bbbc407181dfdee9b2ee70749`  
		Last Modified: Fri, 31 Oct 2025 00:49:47 GMT  
		Size: 167.9 MB (167948122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9504161cb31200125acc034a48877b4c87b8fa8f50a4a5491449b10866d177fc`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d95c7118f545b826eb68e4f581dc725653158afb5e534015fcc52cf9a1e623b`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecd84b0da21b7ac9261d5a7834e43f07293b4627e08e96992b5108f262b3d56`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be103278dbbc68f2584ce11b33141c0f2e095cf4885014f45e11208b6bb10b21`  
		Last Modified: Thu, 30 Oct 2025 23:54:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cc7bd24d0aa86274b9bd038fb37b46eb6e75eb1b0d2d831423eab137e82ea5`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2ee5518f075e453f91fcb34af0861515ee8b59aea56dd0152f079eb9fe4fead5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15158c1ba0b4eb17eac23691fdccfe35bc9d7845537d6da87a77c8a403a07fbb`

```dockerfile
```

-	Layers:
	-	`sha256:3a8e8badc211cc619a524220ae2c9d20a7a33c52a4f4413817a01d27fbad4e64`  
		Last Modified: Fri, 31 Oct 2025 00:49:18 GMT  
		Size: 25.2 KB (25220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4aed478be3bb7097bdc1debd209b178ecf42c37d7210d4e9648631b2579a94b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192983547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d35bbed0c2650693ae9c9d44da2e89dc8b42aba620b35d6de0c43ea3e01810`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:21:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:49 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 21:21:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:16 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3307f657683d186c6205717bfb85eb558ca87cc25b5ec9e9e0f2a3afab8238ae`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.1 MB (7127222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53827a5efe698f075c2a8f84f9e910521f6c849d4e663f8bcda6c1d682998277`  
		Last Modified: Thu, 30 Oct 2025 21:49:52 GMT  
		Size: 157.6 MB (157602973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c75edbbc000a53843b7b15ecb1d209d70d5d24a28598e3ca4b43e07e2115257`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe72d435c20e30ef6acfa667b15604b77c558491fc9f904b620510017cde658`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6a66cb23d300a47ce566678ece81a979d365580649b98d8c909fff1cda80e2`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f337947838d1b535c45aeb37402ed7a290dcfca3e3858494873cc04ab3e63`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314c2d04e787243b12ffabf5f69c468c59cd5a03651b8956fe2db0894f3d63d1`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fa760c382c19e3ad290a49a7f9fcbc3da22211dbfaa1e668571cd3ffdd30a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea58f8008ecdd3d85019881850a1558ac37f38e694fe5712d42af495973d636`

```dockerfile
```

-	Layers:
	-	`sha256:0ae0b038ca2f160b52a976b7eaeccfa1cc67911433863762494a512c80ae316f`  
		Last Modified: Thu, 30 Oct 2025 21:49:22 GMT  
		Size: 25.4 KB (25407 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.8.23`

```console
$ docker pull clickhouse@sha256:c5cc010095c4e55fd68d436d265e6f1acad9db83b427956649d30a6172349b76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.8.23` - linux; amd64

```console
$ docker pull clickhouse@sha256:31c8de206ef101f9dd11beb0e767115d847fc0cf069e8d5eba607a241721772e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205506762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a460c8827aeb6bcabacc4889fdc06fc0e73de0543c391cb9f7f67584d0662d93`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:53:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:53:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:53:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:53:56 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:53:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:53:56 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 23:53:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:54:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:54:18 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:54:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:54:18 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:54:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:54:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a13d4703704b355c7dd6ab15bd271553dad0c7496ce08ee2c941af8fb865c35`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 7.2 MB (7151576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f90441afda07bd8941850b54829b6f6f38e0bbbc407181dfdee9b2ee70749`  
		Last Modified: Fri, 31 Oct 2025 00:49:47 GMT  
		Size: 167.9 MB (167948122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9504161cb31200125acc034a48877b4c87b8fa8f50a4a5491449b10866d177fc`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d95c7118f545b826eb68e4f581dc725653158afb5e534015fcc52cf9a1e623b`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecd84b0da21b7ac9261d5a7834e43f07293b4627e08e96992b5108f262b3d56`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be103278dbbc68f2584ce11b33141c0f2e095cf4885014f45e11208b6bb10b21`  
		Last Modified: Thu, 30 Oct 2025 23:54:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cc7bd24d0aa86274b9bd038fb37b46eb6e75eb1b0d2d831423eab137e82ea5`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.8.23` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2ee5518f075e453f91fcb34af0861515ee8b59aea56dd0152f079eb9fe4fead5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15158c1ba0b4eb17eac23691fdccfe35bc9d7845537d6da87a77c8a403a07fbb`

```dockerfile
```

-	Layers:
	-	`sha256:3a8e8badc211cc619a524220ae2c9d20a7a33c52a4f4413817a01d27fbad4e64`  
		Last Modified: Fri, 31 Oct 2025 00:49:18 GMT  
		Size: 25.2 KB (25220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.8.23` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4aed478be3bb7097bdc1debd209b178ecf42c37d7210d4e9648631b2579a94b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192983547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d35bbed0c2650693ae9c9d44da2e89dc8b42aba620b35d6de0c43ea3e01810`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:21:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:49 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 21:21:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:16 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3307f657683d186c6205717bfb85eb558ca87cc25b5ec9e9e0f2a3afab8238ae`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.1 MB (7127222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53827a5efe698f075c2a8f84f9e910521f6c849d4e663f8bcda6c1d682998277`  
		Last Modified: Thu, 30 Oct 2025 21:49:52 GMT  
		Size: 157.6 MB (157602973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c75edbbc000a53843b7b15ecb1d209d70d5d24a28598e3ca4b43e07e2115257`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe72d435c20e30ef6acfa667b15604b77c558491fc9f904b620510017cde658`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6a66cb23d300a47ce566678ece81a979d365580649b98d8c909fff1cda80e2`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f337947838d1b535c45aeb37402ed7a290dcfca3e3858494873cc04ab3e63`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314c2d04e787243b12ffabf5f69c468c59cd5a03651b8956fe2db0894f3d63d1`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.8.23` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fa760c382c19e3ad290a49a7f9fcbc3da22211dbfaa1e668571cd3ffdd30a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea58f8008ecdd3d85019881850a1558ac37f38e694fe5712d42af495973d636`

```dockerfile
```

-	Layers:
	-	`sha256:0ae0b038ca2f160b52a976b7eaeccfa1cc67911433863762494a512c80ae316f`  
		Last Modified: Thu, 30 Oct 2025 21:49:22 GMT  
		Size: 25.4 KB (25407 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.8.23-jammy`

```console
$ docker pull clickhouse@sha256:c5cc010095c4e55fd68d436d265e6f1acad9db83b427956649d30a6172349b76
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.8.23-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:31c8de206ef101f9dd11beb0e767115d847fc0cf069e8d5eba607a241721772e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205506762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a460c8827aeb6bcabacc4889fdc06fc0e73de0543c391cb9f7f67584d0662d93`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:53:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:53:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:53:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:53:56 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:53:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:53:56 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 23:53:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:54:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:54:18 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:54:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:54:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:54:18 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:54:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:54:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a13d4703704b355c7dd6ab15bd271553dad0c7496ce08ee2c941af8fb865c35`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 7.2 MB (7151576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:328f90441afda07bd8941850b54829b6f6f38e0bbbc407181dfdee9b2ee70749`  
		Last Modified: Fri, 31 Oct 2025 00:49:47 GMT  
		Size: 167.9 MB (167948122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9504161cb31200125acc034a48877b4c87b8fa8f50a4a5491449b10866d177fc`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d95c7118f545b826eb68e4f581dc725653158afb5e534015fcc52cf9a1e623b`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecd84b0da21b7ac9261d5a7834e43f07293b4627e08e96992b5108f262b3d56`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be103278dbbc68f2584ce11b33141c0f2e095cf4885014f45e11208b6bb10b21`  
		Last Modified: Thu, 30 Oct 2025 23:54:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cc7bd24d0aa86274b9bd038fb37b46eb6e75eb1b0d2d831423eab137e82ea5`  
		Last Modified: Thu, 30 Oct 2025 23:54:47 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.8.23-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:2ee5518f075e453f91fcb34af0861515ee8b59aea56dd0152f079eb9fe4fead5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15158c1ba0b4eb17eac23691fdccfe35bc9d7845537d6da87a77c8a403a07fbb`

```dockerfile
```

-	Layers:
	-	`sha256:3a8e8badc211cc619a524220ae2c9d20a7a33c52a4f4413817a01d27fbad4e64`  
		Last Modified: Fri, 31 Oct 2025 00:49:18 GMT  
		Size: 25.2 KB (25220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.8.23-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4aed478be3bb7097bdc1debd209b178ecf42c37d7210d4e9648631b2579a94b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192983547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d35bbed0c2650693ae9c9d44da2e89dc8b42aba620b35d6de0c43ea3e01810`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:21:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:49 GMT
ARG VERSION=25.3.8.23
# Thu, 30 Oct 2025 21:21:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:16 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:16 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3307f657683d186c6205717bfb85eb558ca87cc25b5ec9e9e0f2a3afab8238ae`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.1 MB (7127222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53827a5efe698f075c2a8f84f9e910521f6c849d4e663f8bcda6c1d682998277`  
		Last Modified: Thu, 30 Oct 2025 21:49:52 GMT  
		Size: 157.6 MB (157602973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c75edbbc000a53843b7b15ecb1d209d70d5d24a28598e3ca4b43e07e2115257`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe72d435c20e30ef6acfa667b15604b77c558491fc9f904b620510017cde658`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6a66cb23d300a47ce566678ece81a979d365580649b98d8c909fff1cda80e2`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83f337947838d1b535c45aeb37402ed7a290dcfca3e3858494873cc04ab3e63`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:314c2d04e787243b12ffabf5f69c468c59cd5a03651b8956fe2db0894f3d63d1`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.8.23-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fa760c382c19e3ad290a49a7f9fcbc3da22211dbfaa1e668571cd3ffdd30a3c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ea58f8008ecdd3d85019881850a1558ac37f38e694fe5712d42af495973d636`

```dockerfile
```

-	Layers:
	-	`sha256:0ae0b038ca2f160b52a976b7eaeccfa1cc67911433863762494a512c80ae316f`  
		Last Modified: Thu, 30 Oct 2025 21:49:22 GMT  
		Size: 25.4 KB (25407 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:3f7319c4094584ea1e527d2fe8bc7c0d03356774449fae9d00bfe6b770bc5cc0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:c090f2f5be6364821b31be1fbd278413fb83b2e07122f8ff19e535deeb49f14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227833727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c563c7d8483b10b76dda7c4b0c1da80a4773542b2afa2f2d9cd06ec480369be0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:53:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:53:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:53:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:53:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:53:59 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 23:53:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:54:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:54:25 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:54:25 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:54:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:54:26 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:54:26 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:54:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ddbf1790aac818fc42043394030555dceee7d2402503ea1743acf316968d5d`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 7.6 MB (7598359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b71c2c8a6ff701f53316322e9dd4bab196a266dc009bb2642f9cc4cc6caf9`  
		Last Modified: Fri, 31 Oct 2025 00:50:15 GMT  
		Size: 189.8 MB (189828532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73dc43b82a4c8bf9823bbb7346ac5304f1e7302ea3d97bfb79998562e698782`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad672abd047ac6ffd6ebc6408fb07df6b27bbf64dc47c3c30b54ee8d80b3a5f`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a242d7ec651eceebf026fa9215a574414c4eaf6ed28bb29bbeffb7a50ad8548`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4314f6c48d0c800956cec3e5857ae521dac0be0b82ebded9a9d63e887ed507`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989775034b6f9aeeb688b71bcedc51726f96e3fc855f085ec2fecb490a58374`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e36034a604435695fcb941e3af130db42f3e896ad9dc828774738d39d76754f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb4c979459bf8105d26754d11eaf2bf40538e89af14f65f43fbe10200781337`

```dockerfile
```

-	Layers:
	-	`sha256:51240151cc461d203bfe9dbb7ca87497417d94bc660f5cb1aa4ce6aed96b35db`  
		Last Modified: Fri, 31 Oct 2025 00:49:35 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a5656778631ee59482d9821f008c2f43704a533bb78ce9fabe3f9e735055b882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212645310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cee591520bd679efa5bdfc5ccbbe8955c161e8ce6052107b9f0192bb2d962`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:21:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:43 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 21:21:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:12 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7ce10c9eeca1dd1885578ad8f3f6291f3732bdf5a50a8a6535af67a72e81f`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee964fa2145e136ca73e4c3796c405f427a709e6070f3f4802f8e19f6723677`  
		Last Modified: Thu, 30 Oct 2025 21:50:09 GMT  
		Size: 176.8 MB (176815492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59e47ba03552bfa2a66ef28e55b44868ad4666ae67b5fe3e408e5c5a79ca85`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9616189aee41fb2150e3b2e7df745964d4e966fb63f6a7a431d6d848dfc358`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163c00ab90daa2465b1046a4d0b95388778dc70b143011610dca4fb7590de31`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47157a68ab31f8dfb08a2352278276b514a9773b046ac4dca1504822e01e8856`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda603cdd01780ad677c4f16ef238ba487aa146cd3f5d06542f066c10b93575`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:557ba9743467f6d9ecfb1670d9fb813858720e1ed9612956f837ce4eb5cf0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30079417e65d20ad6f0ad236690d7babc98d5d1128642255422497d2ca46316f`

```dockerfile
```

-	Layers:
	-	`sha256:cdecb34f64c1ba351dec1bcc4a2182fa4b916423bfa5f3853e9f82069f25386a`  
		Last Modified: Thu, 30 Oct 2025 21:49:42 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:3f7319c4094584ea1e527d2fe8bc7c0d03356774449fae9d00bfe6b770bc5cc0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:c090f2f5be6364821b31be1fbd278413fb83b2e07122f8ff19e535deeb49f14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227833727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c563c7d8483b10b76dda7c4b0c1da80a4773542b2afa2f2d9cd06ec480369be0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:53:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:53:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:53:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:53:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:53:59 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 23:53:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:54:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:54:25 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:54:25 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:54:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:54:26 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:54:26 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:54:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ddbf1790aac818fc42043394030555dceee7d2402503ea1743acf316968d5d`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 7.6 MB (7598359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b71c2c8a6ff701f53316322e9dd4bab196a266dc009bb2642f9cc4cc6caf9`  
		Last Modified: Fri, 31 Oct 2025 00:50:15 GMT  
		Size: 189.8 MB (189828532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73dc43b82a4c8bf9823bbb7346ac5304f1e7302ea3d97bfb79998562e698782`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad672abd047ac6ffd6ebc6408fb07df6b27bbf64dc47c3c30b54ee8d80b3a5f`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a242d7ec651eceebf026fa9215a574414c4eaf6ed28bb29bbeffb7a50ad8548`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4314f6c48d0c800956cec3e5857ae521dac0be0b82ebded9a9d63e887ed507`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989775034b6f9aeeb688b71bcedc51726f96e3fc855f085ec2fecb490a58374`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e36034a604435695fcb941e3af130db42f3e896ad9dc828774738d39d76754f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb4c979459bf8105d26754d11eaf2bf40538e89af14f65f43fbe10200781337`

```dockerfile
```

-	Layers:
	-	`sha256:51240151cc461d203bfe9dbb7ca87497417d94bc660f5cb1aa4ce6aed96b35db`  
		Last Modified: Fri, 31 Oct 2025 00:49:35 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a5656778631ee59482d9821f008c2f43704a533bb78ce9fabe3f9e735055b882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212645310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cee591520bd679efa5bdfc5ccbbe8955c161e8ce6052107b9f0192bb2d962`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:21:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:43 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 21:21:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:12 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7ce10c9eeca1dd1885578ad8f3f6291f3732bdf5a50a8a6535af67a72e81f`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee964fa2145e136ca73e4c3796c405f427a709e6070f3f4802f8e19f6723677`  
		Last Modified: Thu, 30 Oct 2025 21:50:09 GMT  
		Size: 176.8 MB (176815492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59e47ba03552bfa2a66ef28e55b44868ad4666ae67b5fe3e408e5c5a79ca85`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9616189aee41fb2150e3b2e7df745964d4e966fb63f6a7a431d6d848dfc358`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163c00ab90daa2465b1046a4d0b95388778dc70b143011610dca4fb7590de31`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47157a68ab31f8dfb08a2352278276b514a9773b046ac4dca1504822e01e8856`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda603cdd01780ad677c4f16ef238ba487aa146cd3f5d06542f066c10b93575`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:557ba9743467f6d9ecfb1670d9fb813858720e1ed9612956f837ce4eb5cf0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30079417e65d20ad6f0ad236690d7babc98d5d1128642255422497d2ca46316f`

```dockerfile
```

-	Layers:
	-	`sha256:cdecb34f64c1ba351dec1bcc4a2182fa4b916423bfa5f3853e9f82069f25386a`  
		Last Modified: Thu, 30 Oct 2025 21:49:42 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.11`

```console
$ docker pull clickhouse@sha256:3f7319c4094584ea1e527d2fe8bc7c0d03356774449fae9d00bfe6b770bc5cc0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:c090f2f5be6364821b31be1fbd278413fb83b2e07122f8ff19e535deeb49f14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227833727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c563c7d8483b10b76dda7c4b0c1da80a4773542b2afa2f2d9cd06ec480369be0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:53:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:53:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:53:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:53:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:53:59 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 23:53:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:54:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:54:25 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:54:25 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:54:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:54:26 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:54:26 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:54:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ddbf1790aac818fc42043394030555dceee7d2402503ea1743acf316968d5d`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 7.6 MB (7598359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b71c2c8a6ff701f53316322e9dd4bab196a266dc009bb2642f9cc4cc6caf9`  
		Last Modified: Fri, 31 Oct 2025 00:50:15 GMT  
		Size: 189.8 MB (189828532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73dc43b82a4c8bf9823bbb7346ac5304f1e7302ea3d97bfb79998562e698782`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad672abd047ac6ffd6ebc6408fb07df6b27bbf64dc47c3c30b54ee8d80b3a5f`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a242d7ec651eceebf026fa9215a574414c4eaf6ed28bb29bbeffb7a50ad8548`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4314f6c48d0c800956cec3e5857ae521dac0be0b82ebded9a9d63e887ed507`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989775034b6f9aeeb688b71bcedc51726f96e3fc855f085ec2fecb490a58374`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e36034a604435695fcb941e3af130db42f3e896ad9dc828774738d39d76754f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb4c979459bf8105d26754d11eaf2bf40538e89af14f65f43fbe10200781337`

```dockerfile
```

-	Layers:
	-	`sha256:51240151cc461d203bfe9dbb7ca87497417d94bc660f5cb1aa4ce6aed96b35db`  
		Last Modified: Fri, 31 Oct 2025 00:49:35 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a5656778631ee59482d9821f008c2f43704a533bb78ce9fabe3f9e735055b882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212645310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cee591520bd679efa5bdfc5ccbbe8955c161e8ce6052107b9f0192bb2d962`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:21:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:43 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 21:21:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:12 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7ce10c9eeca1dd1885578ad8f3f6291f3732bdf5a50a8a6535af67a72e81f`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee964fa2145e136ca73e4c3796c405f427a709e6070f3f4802f8e19f6723677`  
		Last Modified: Thu, 30 Oct 2025 21:50:09 GMT  
		Size: 176.8 MB (176815492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59e47ba03552bfa2a66ef28e55b44868ad4666ae67b5fe3e408e5c5a79ca85`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9616189aee41fb2150e3b2e7df745964d4e966fb63f6a7a431d6d848dfc358`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163c00ab90daa2465b1046a4d0b95388778dc70b143011610dca4fb7590de31`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47157a68ab31f8dfb08a2352278276b514a9773b046ac4dca1504822e01e8856`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda603cdd01780ad677c4f16ef238ba487aa146cd3f5d06542f066c10b93575`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:557ba9743467f6d9ecfb1670d9fb813858720e1ed9612956f837ce4eb5cf0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30079417e65d20ad6f0ad236690d7babc98d5d1128642255422497d2ca46316f`

```dockerfile
```

-	Layers:
	-	`sha256:cdecb34f64c1ba351dec1bcc4a2182fa4b916423bfa5f3853e9f82069f25386a`  
		Last Modified: Thu, 30 Oct 2025 21:49:42 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.11-jammy`

```console
$ docker pull clickhouse@sha256:3f7319c4094584ea1e527d2fe8bc7c0d03356774449fae9d00bfe6b770bc5cc0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:c090f2f5be6364821b31be1fbd278413fb83b2e07122f8ff19e535deeb49f14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227833727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c563c7d8483b10b76dda7c4b0c1da80a4773542b2afa2f2d9cd06ec480369be0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:53:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:53:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:53:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:53:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:53:59 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 23:53:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:54:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:54:25 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:54:25 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:54:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:54:26 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:54:26 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:54:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ddbf1790aac818fc42043394030555dceee7d2402503ea1743acf316968d5d`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 7.6 MB (7598359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b71c2c8a6ff701f53316322e9dd4bab196a266dc009bb2642f9cc4cc6caf9`  
		Last Modified: Fri, 31 Oct 2025 00:50:15 GMT  
		Size: 189.8 MB (189828532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73dc43b82a4c8bf9823bbb7346ac5304f1e7302ea3d97bfb79998562e698782`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad672abd047ac6ffd6ebc6408fb07df6b27bbf64dc47c3c30b54ee8d80b3a5f`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a242d7ec651eceebf026fa9215a574414c4eaf6ed28bb29bbeffb7a50ad8548`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4314f6c48d0c800956cec3e5857ae521dac0be0b82ebded9a9d63e887ed507`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989775034b6f9aeeb688b71bcedc51726f96e3fc855f085ec2fecb490a58374`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e36034a604435695fcb941e3af130db42f3e896ad9dc828774738d39d76754f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb4c979459bf8105d26754d11eaf2bf40538e89af14f65f43fbe10200781337`

```dockerfile
```

-	Layers:
	-	`sha256:51240151cc461d203bfe9dbb7ca87497417d94bc660f5cb1aa4ce6aed96b35db`  
		Last Modified: Fri, 31 Oct 2025 00:49:35 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a5656778631ee59482d9821f008c2f43704a533bb78ce9fabe3f9e735055b882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212645310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cee591520bd679efa5bdfc5ccbbe8955c161e8ce6052107b9f0192bb2d962`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:21:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:43 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 21:21:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:12 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7ce10c9eeca1dd1885578ad8f3f6291f3732bdf5a50a8a6535af67a72e81f`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee964fa2145e136ca73e4c3796c405f427a709e6070f3f4802f8e19f6723677`  
		Last Modified: Thu, 30 Oct 2025 21:50:09 GMT  
		Size: 176.8 MB (176815492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59e47ba03552bfa2a66ef28e55b44868ad4666ae67b5fe3e408e5c5a79ca85`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9616189aee41fb2150e3b2e7df745964d4e966fb63f6a7a431d6d848dfc358`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163c00ab90daa2465b1046a4d0b95388778dc70b143011610dca4fb7590de31`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47157a68ab31f8dfb08a2352278276b514a9773b046ac4dca1504822e01e8856`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda603cdd01780ad677c4f16ef238ba487aa146cd3f5d06542f066c10b93575`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:557ba9743467f6d9ecfb1670d9fb813858720e1ed9612956f837ce4eb5cf0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30079417e65d20ad6f0ad236690d7babc98d5d1128642255422497d2ca46316f`

```dockerfile
```

-	Layers:
	-	`sha256:cdecb34f64c1ba351dec1bcc4a2182fa4b916423bfa5f3853e9f82069f25386a`  
		Last Modified: Thu, 30 Oct 2025 21:49:42 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.11.66`

```console
$ docker pull clickhouse@sha256:3f7319c4094584ea1e527d2fe8bc7c0d03356774449fae9d00bfe6b770bc5cc0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.11.66` - linux; amd64

```console
$ docker pull clickhouse@sha256:c090f2f5be6364821b31be1fbd278413fb83b2e07122f8ff19e535deeb49f14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227833727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c563c7d8483b10b76dda7c4b0c1da80a4773542b2afa2f2d9cd06ec480369be0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:53:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:53:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:53:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:53:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:53:59 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 23:53:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:54:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:54:25 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:54:25 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:54:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:54:26 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:54:26 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:54:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ddbf1790aac818fc42043394030555dceee7d2402503ea1743acf316968d5d`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 7.6 MB (7598359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b71c2c8a6ff701f53316322e9dd4bab196a266dc009bb2642f9cc4cc6caf9`  
		Last Modified: Fri, 31 Oct 2025 00:50:15 GMT  
		Size: 189.8 MB (189828532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73dc43b82a4c8bf9823bbb7346ac5304f1e7302ea3d97bfb79998562e698782`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad672abd047ac6ffd6ebc6408fb07df6b27bbf64dc47c3c30b54ee8d80b3a5f`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a242d7ec651eceebf026fa9215a574414c4eaf6ed28bb29bbeffb7a50ad8548`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4314f6c48d0c800956cec3e5857ae521dac0be0b82ebded9a9d63e887ed507`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989775034b6f9aeeb688b71bcedc51726f96e3fc855f085ec2fecb490a58374`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.11.66` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e36034a604435695fcb941e3af130db42f3e896ad9dc828774738d39d76754f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb4c979459bf8105d26754d11eaf2bf40538e89af14f65f43fbe10200781337`

```dockerfile
```

-	Layers:
	-	`sha256:51240151cc461d203bfe9dbb7ca87497417d94bc660f5cb1aa4ce6aed96b35db`  
		Last Modified: Fri, 31 Oct 2025 00:49:35 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.11.66` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a5656778631ee59482d9821f008c2f43704a533bb78ce9fabe3f9e735055b882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212645310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cee591520bd679efa5bdfc5ccbbe8955c161e8ce6052107b9f0192bb2d962`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:21:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:43 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 21:21:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:12 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7ce10c9eeca1dd1885578ad8f3f6291f3732bdf5a50a8a6535af67a72e81f`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee964fa2145e136ca73e4c3796c405f427a709e6070f3f4802f8e19f6723677`  
		Last Modified: Thu, 30 Oct 2025 21:50:09 GMT  
		Size: 176.8 MB (176815492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59e47ba03552bfa2a66ef28e55b44868ad4666ae67b5fe3e408e5c5a79ca85`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9616189aee41fb2150e3b2e7df745964d4e966fb63f6a7a431d6d848dfc358`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163c00ab90daa2465b1046a4d0b95388778dc70b143011610dca4fb7590de31`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47157a68ab31f8dfb08a2352278276b514a9773b046ac4dca1504822e01e8856`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda603cdd01780ad677c4f16ef238ba487aa146cd3f5d06542f066c10b93575`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.11.66` - unknown; unknown

```console
$ docker pull clickhouse@sha256:557ba9743467f6d9ecfb1670d9fb813858720e1ed9612956f837ce4eb5cf0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30079417e65d20ad6f0ad236690d7babc98d5d1128642255422497d2ca46316f`

```dockerfile
```

-	Layers:
	-	`sha256:cdecb34f64c1ba351dec1bcc4a2182fa4b916423bfa5f3853e9f82069f25386a`  
		Last Modified: Thu, 30 Oct 2025 21:49:42 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.11.66-jammy`

```console
$ docker pull clickhouse@sha256:3f7319c4094584ea1e527d2fe8bc7c0d03356774449fae9d00bfe6b770bc5cc0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.11.66-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:c090f2f5be6364821b31be1fbd278413fb83b2e07122f8ff19e535deeb49f14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227833727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c563c7d8483b10b76dda7c4b0c1da80a4773542b2afa2f2d9cd06ec480369be0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:53:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:53:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:53:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:53:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:53:59 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 23:53:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:54:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:54:25 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:54:25 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:54:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:54:26 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:54:26 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:54:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ddbf1790aac818fc42043394030555dceee7d2402503ea1743acf316968d5d`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 7.6 MB (7598359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b71c2c8a6ff701f53316322e9dd4bab196a266dc009bb2642f9cc4cc6caf9`  
		Last Modified: Fri, 31 Oct 2025 00:50:15 GMT  
		Size: 189.8 MB (189828532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73dc43b82a4c8bf9823bbb7346ac5304f1e7302ea3d97bfb79998562e698782`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad672abd047ac6ffd6ebc6408fb07df6b27bbf64dc47c3c30b54ee8d80b3a5f`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a242d7ec651eceebf026fa9215a574414c4eaf6ed28bb29bbeffb7a50ad8548`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4314f6c48d0c800956cec3e5857ae521dac0be0b82ebded9a9d63e887ed507`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989775034b6f9aeeb688b71bcedc51726f96e3fc855f085ec2fecb490a58374`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.11.66-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e36034a604435695fcb941e3af130db42f3e896ad9dc828774738d39d76754f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb4c979459bf8105d26754d11eaf2bf40538e89af14f65f43fbe10200781337`

```dockerfile
```

-	Layers:
	-	`sha256:51240151cc461d203bfe9dbb7ca87497417d94bc660f5cb1aa4ce6aed96b35db`  
		Last Modified: Fri, 31 Oct 2025 00:49:35 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.11.66-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a5656778631ee59482d9821f008c2f43704a533bb78ce9fabe3f9e735055b882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212645310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cee591520bd679efa5bdfc5ccbbe8955c161e8ce6052107b9f0192bb2d962`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:21:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:43 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 21:21:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:12 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7ce10c9eeca1dd1885578ad8f3f6291f3732bdf5a50a8a6535af67a72e81f`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee964fa2145e136ca73e4c3796c405f427a709e6070f3f4802f8e19f6723677`  
		Last Modified: Thu, 30 Oct 2025 21:50:09 GMT  
		Size: 176.8 MB (176815492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59e47ba03552bfa2a66ef28e55b44868ad4666ae67b5fe3e408e5c5a79ca85`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9616189aee41fb2150e3b2e7df745964d4e966fb63f6a7a431d6d848dfc358`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163c00ab90daa2465b1046a4d0b95388778dc70b143011610dca4fb7590de31`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47157a68ab31f8dfb08a2352278276b514a9773b046ac4dca1504822e01e8856`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda603cdd01780ad677c4f16ef238ba487aa146cd3f5d06542f066c10b93575`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.11.66-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:557ba9743467f6d9ecfb1670d9fb813858720e1ed9612956f837ce4eb5cf0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30079417e65d20ad6f0ad236690d7babc98d5d1128642255422497d2ca46316f`

```dockerfile
```

-	Layers:
	-	`sha256:cdecb34f64c1ba351dec1bcc4a2182fa4b916423bfa5f3853e9f82069f25386a`  
		Last Modified: Thu, 30 Oct 2025 21:49:42 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9`

```console
$ docker pull clickhouse@sha256:ff986122e5bf19e5aef2ecabcd16bbe05c4a25e00bb67ae0b4ff6b7b11ad0488
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9` - linux; amd64

```console
$ docker pull clickhouse@sha256:9d25aa64feac427c42cdf744ef9aa4f231acb86c15f152ddeefd90f6040ae723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228849900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51f737ce505cb0e8ea90024c9e5aa742f2cba374e233f4013ee4817b1711562`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:52:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:52:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:52:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:52:15 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:52:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:52:15 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 23:52:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:52:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:52:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:52:42 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:52:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:52:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:52:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:52:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c05c65c48cae9023d76ef49327f9ff4a44fe42bace02531a518a8e6576377`  
		Last Modified: Thu, 30 Oct 2025 23:53:21 GMT  
		Size: 7.6 MB (7598386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b298cd9e89321c97630540ce9e3389f574c7103c453ef1870ad8d3b6e6c03d`  
		Last Modified: Fri, 31 Oct 2025 00:50:24 GMT  
		Size: 190.8 MB (190844672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7460849a38eecaa02d67a471ffa18f69c5fa51f54a584e792bc89baece46efc`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c43143536b84e144969448d009b8aeba48716cefb394ec2d0549861006f4383`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcd3f3e82c803768cede882c734678a78a3bc587d5baa98aa91654403f20cfb`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0760830e46f553a3c445fa714aaa0bbcce24425ccee151fdfafc4031df31b1d`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e841bceac6aab182cb501d93b256e962fad806ae015dae2640a7f936720c7f19`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b3453230dae41986ec910b9dd820c23d4df56ac68bc8814818aadf053014aad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c016c7e2b79d154a365f0a085fabed20ec181b76a89890ef6d085f393d239b76`

```dockerfile
```

-	Layers:
	-	`sha256:4e6d502db8a447556f4f5558c96aef5270b6b4f517bed0e88ca0e114ce0e1566`  
		Last Modified: Fri, 31 Oct 2025 00:49:53 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4c561844d47154da2cf18bf6fc308a9c1470ebd0b1557577abda7d8663dbd839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214126824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fd8eaba170a8cabde920b8dff74572a18fef475f1da56cf9c2855f6e4dbaf7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:20:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:20:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:20:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:20:39 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 21:20:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:21:07 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:21:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:21:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:21:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f2b54dec56f899e3541e6378d03e8cd182afe4eb4890b954deb8802842f910`  
		Last Modified: Thu, 30 Oct 2025 21:21:52 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3ffe7f678bcd6c880170754623c76b9248b55906cf055baf12b61fd5eef4ed`  
		Last Modified: Thu, 30 Oct 2025 21:50:23 GMT  
		Size: 178.3 MB (178296962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd97dc583a1c5bacf4be0631e5360f470d7b445747bdf2c1e39ab7c59092afb7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ac0b36c361fd8685c0f0c00ac426d3f75d0735f1fd9f3c71b4738dbf41f8d`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b892c789c4c82a60a77df538ce28170f3c71c1c7381ab0c590c490d13f6fef7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6da2b828b97d18e73c18a5c0b0811f1e365e04a58484841e5d282a130d9f34`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9dec9f0e0da6fcc5341e51c7153a7fb55efedbb4ee320a25539daf55c8e011`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:312f09886ff78060a641456578037587fbae0fae26fb8970a86de595d351c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a11d90d516ff1db5e847298e0bfda6cfe9477e57b25a8aaa5279ad2323fec60`

```dockerfile
```

-	Layers:
	-	`sha256:7c0633f1e88444ed45b99f3525f54cbe9baf7c926eb1cf5c8f5abfc8e32886a2`  
		Last Modified: Thu, 30 Oct 2025 21:49:57 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9-jammy`

```console
$ docker pull clickhouse@sha256:ff986122e5bf19e5aef2ecabcd16bbe05c4a25e00bb67ae0b4ff6b7b11ad0488
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:9d25aa64feac427c42cdf744ef9aa4f231acb86c15f152ddeefd90f6040ae723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228849900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51f737ce505cb0e8ea90024c9e5aa742f2cba374e233f4013ee4817b1711562`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:52:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:52:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:52:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:52:15 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:52:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:52:15 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 23:52:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:52:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:52:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:52:42 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:52:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:52:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:52:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:52:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c05c65c48cae9023d76ef49327f9ff4a44fe42bace02531a518a8e6576377`  
		Last Modified: Thu, 30 Oct 2025 23:53:21 GMT  
		Size: 7.6 MB (7598386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b298cd9e89321c97630540ce9e3389f574c7103c453ef1870ad8d3b6e6c03d`  
		Last Modified: Fri, 31 Oct 2025 00:50:24 GMT  
		Size: 190.8 MB (190844672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7460849a38eecaa02d67a471ffa18f69c5fa51f54a584e792bc89baece46efc`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c43143536b84e144969448d009b8aeba48716cefb394ec2d0549861006f4383`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcd3f3e82c803768cede882c734678a78a3bc587d5baa98aa91654403f20cfb`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0760830e46f553a3c445fa714aaa0bbcce24425ccee151fdfafc4031df31b1d`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e841bceac6aab182cb501d93b256e962fad806ae015dae2640a7f936720c7f19`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b3453230dae41986ec910b9dd820c23d4df56ac68bc8814818aadf053014aad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c016c7e2b79d154a365f0a085fabed20ec181b76a89890ef6d085f393d239b76`

```dockerfile
```

-	Layers:
	-	`sha256:4e6d502db8a447556f4f5558c96aef5270b6b4f517bed0e88ca0e114ce0e1566`  
		Last Modified: Fri, 31 Oct 2025 00:49:53 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4c561844d47154da2cf18bf6fc308a9c1470ebd0b1557577abda7d8663dbd839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214126824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fd8eaba170a8cabde920b8dff74572a18fef475f1da56cf9c2855f6e4dbaf7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:20:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:20:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:20:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:20:39 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 21:20:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:21:07 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:21:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:21:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:21:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f2b54dec56f899e3541e6378d03e8cd182afe4eb4890b954deb8802842f910`  
		Last Modified: Thu, 30 Oct 2025 21:21:52 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3ffe7f678bcd6c880170754623c76b9248b55906cf055baf12b61fd5eef4ed`  
		Last Modified: Thu, 30 Oct 2025 21:50:23 GMT  
		Size: 178.3 MB (178296962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd97dc583a1c5bacf4be0631e5360f470d7b445747bdf2c1e39ab7c59092afb7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ac0b36c361fd8685c0f0c00ac426d3f75d0735f1fd9f3c71b4738dbf41f8d`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b892c789c4c82a60a77df538ce28170f3c71c1c7381ab0c590c490d13f6fef7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6da2b828b97d18e73c18a5c0b0811f1e365e04a58484841e5d282a130d9f34`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9dec9f0e0da6fcc5341e51c7153a7fb55efedbb4ee320a25539daf55c8e011`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:312f09886ff78060a641456578037587fbae0fae26fb8970a86de595d351c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a11d90d516ff1db5e847298e0bfda6cfe9477e57b25a8aaa5279ad2323fec60`

```dockerfile
```

-	Layers:
	-	`sha256:7c0633f1e88444ed45b99f3525f54cbe9baf7c926eb1cf5c8f5abfc8e32886a2`  
		Last Modified: Thu, 30 Oct 2025 21:49:57 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.5`

```console
$ docker pull clickhouse@sha256:ff986122e5bf19e5aef2ecabcd16bbe05c4a25e00bb67ae0b4ff6b7b11ad0488
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:9d25aa64feac427c42cdf744ef9aa4f231acb86c15f152ddeefd90f6040ae723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228849900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51f737ce505cb0e8ea90024c9e5aa742f2cba374e233f4013ee4817b1711562`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:52:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:52:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:52:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:52:15 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:52:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:52:15 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 23:52:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:52:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:52:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:52:42 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:52:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:52:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:52:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:52:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c05c65c48cae9023d76ef49327f9ff4a44fe42bace02531a518a8e6576377`  
		Last Modified: Thu, 30 Oct 2025 23:53:21 GMT  
		Size: 7.6 MB (7598386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b298cd9e89321c97630540ce9e3389f574c7103c453ef1870ad8d3b6e6c03d`  
		Last Modified: Fri, 31 Oct 2025 00:50:24 GMT  
		Size: 190.8 MB (190844672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7460849a38eecaa02d67a471ffa18f69c5fa51f54a584e792bc89baece46efc`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c43143536b84e144969448d009b8aeba48716cefb394ec2d0549861006f4383`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcd3f3e82c803768cede882c734678a78a3bc587d5baa98aa91654403f20cfb`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0760830e46f553a3c445fa714aaa0bbcce24425ccee151fdfafc4031df31b1d`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e841bceac6aab182cb501d93b256e962fad806ae015dae2640a7f936720c7f19`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b3453230dae41986ec910b9dd820c23d4df56ac68bc8814818aadf053014aad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c016c7e2b79d154a365f0a085fabed20ec181b76a89890ef6d085f393d239b76`

```dockerfile
```

-	Layers:
	-	`sha256:4e6d502db8a447556f4f5558c96aef5270b6b4f517bed0e88ca0e114ce0e1566`  
		Last Modified: Fri, 31 Oct 2025 00:49:53 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4c561844d47154da2cf18bf6fc308a9c1470ebd0b1557577abda7d8663dbd839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214126824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fd8eaba170a8cabde920b8dff74572a18fef475f1da56cf9c2855f6e4dbaf7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:20:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:20:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:20:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:20:39 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 21:20:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:21:07 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:21:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:21:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:21:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f2b54dec56f899e3541e6378d03e8cd182afe4eb4890b954deb8802842f910`  
		Last Modified: Thu, 30 Oct 2025 21:21:52 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3ffe7f678bcd6c880170754623c76b9248b55906cf055baf12b61fd5eef4ed`  
		Last Modified: Thu, 30 Oct 2025 21:50:23 GMT  
		Size: 178.3 MB (178296962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd97dc583a1c5bacf4be0631e5360f470d7b445747bdf2c1e39ab7c59092afb7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ac0b36c361fd8685c0f0c00ac426d3f75d0735f1fd9f3c71b4738dbf41f8d`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b892c789c4c82a60a77df538ce28170f3c71c1c7381ab0c590c490d13f6fef7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6da2b828b97d18e73c18a5c0b0811f1e365e04a58484841e5d282a130d9f34`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9dec9f0e0da6fcc5341e51c7153a7fb55efedbb4ee320a25539daf55c8e011`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:312f09886ff78060a641456578037587fbae0fae26fb8970a86de595d351c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a11d90d516ff1db5e847298e0bfda6cfe9477e57b25a8aaa5279ad2323fec60`

```dockerfile
```

-	Layers:
	-	`sha256:7c0633f1e88444ed45b99f3525f54cbe9baf7c926eb1cf5c8f5abfc8e32886a2`  
		Last Modified: Thu, 30 Oct 2025 21:49:57 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.5-jammy`

```console
$ docker pull clickhouse@sha256:ff986122e5bf19e5aef2ecabcd16bbe05c4a25e00bb67ae0b4ff6b7b11ad0488
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:9d25aa64feac427c42cdf744ef9aa4f231acb86c15f152ddeefd90f6040ae723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228849900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51f737ce505cb0e8ea90024c9e5aa742f2cba374e233f4013ee4817b1711562`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:52:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:52:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:52:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:52:15 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:52:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:52:15 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 23:52:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:52:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:52:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:52:42 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:52:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:52:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:52:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:52:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c05c65c48cae9023d76ef49327f9ff4a44fe42bace02531a518a8e6576377`  
		Last Modified: Thu, 30 Oct 2025 23:53:21 GMT  
		Size: 7.6 MB (7598386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b298cd9e89321c97630540ce9e3389f574c7103c453ef1870ad8d3b6e6c03d`  
		Last Modified: Fri, 31 Oct 2025 00:50:24 GMT  
		Size: 190.8 MB (190844672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7460849a38eecaa02d67a471ffa18f69c5fa51f54a584e792bc89baece46efc`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c43143536b84e144969448d009b8aeba48716cefb394ec2d0549861006f4383`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcd3f3e82c803768cede882c734678a78a3bc587d5baa98aa91654403f20cfb`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0760830e46f553a3c445fa714aaa0bbcce24425ccee151fdfafc4031df31b1d`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e841bceac6aab182cb501d93b256e962fad806ae015dae2640a7f936720c7f19`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b3453230dae41986ec910b9dd820c23d4df56ac68bc8814818aadf053014aad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c016c7e2b79d154a365f0a085fabed20ec181b76a89890ef6d085f393d239b76`

```dockerfile
```

-	Layers:
	-	`sha256:4e6d502db8a447556f4f5558c96aef5270b6b4f517bed0e88ca0e114ce0e1566`  
		Last Modified: Fri, 31 Oct 2025 00:49:53 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4c561844d47154da2cf18bf6fc308a9c1470ebd0b1557577abda7d8663dbd839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214126824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fd8eaba170a8cabde920b8dff74572a18fef475f1da56cf9c2855f6e4dbaf7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:20:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:20:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:20:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:20:39 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 21:20:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:21:07 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:21:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:21:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:21:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f2b54dec56f899e3541e6378d03e8cd182afe4eb4890b954deb8802842f910`  
		Last Modified: Thu, 30 Oct 2025 21:21:52 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3ffe7f678bcd6c880170754623c76b9248b55906cf055baf12b61fd5eef4ed`  
		Last Modified: Thu, 30 Oct 2025 21:50:23 GMT  
		Size: 178.3 MB (178296962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd97dc583a1c5bacf4be0631e5360f470d7b445747bdf2c1e39ab7c59092afb7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ac0b36c361fd8685c0f0c00ac426d3f75d0735f1fd9f3c71b4738dbf41f8d`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b892c789c4c82a60a77df538ce28170f3c71c1c7381ab0c590c490d13f6fef7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6da2b828b97d18e73c18a5c0b0811f1e365e04a58484841e5d282a130d9f34`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9dec9f0e0da6fcc5341e51c7153a7fb55efedbb4ee320a25539daf55c8e011`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:312f09886ff78060a641456578037587fbae0fae26fb8970a86de595d351c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a11d90d516ff1db5e847298e0bfda6cfe9477e57b25a8aaa5279ad2323fec60`

```dockerfile
```

-	Layers:
	-	`sha256:7c0633f1e88444ed45b99f3525f54cbe9baf7c926eb1cf5c8f5abfc8e32886a2`  
		Last Modified: Thu, 30 Oct 2025 21:49:57 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.5.21`

```console
$ docker pull clickhouse@sha256:ff986122e5bf19e5aef2ecabcd16bbe05c4a25e00bb67ae0b4ff6b7b11ad0488
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.5.21` - linux; amd64

```console
$ docker pull clickhouse@sha256:9d25aa64feac427c42cdf744ef9aa4f231acb86c15f152ddeefd90f6040ae723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228849900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51f737ce505cb0e8ea90024c9e5aa742f2cba374e233f4013ee4817b1711562`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:52:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:52:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:52:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:52:15 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:52:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:52:15 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 23:52:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:52:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:52:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:52:42 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:52:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:52:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:52:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:52:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c05c65c48cae9023d76ef49327f9ff4a44fe42bace02531a518a8e6576377`  
		Last Modified: Thu, 30 Oct 2025 23:53:21 GMT  
		Size: 7.6 MB (7598386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b298cd9e89321c97630540ce9e3389f574c7103c453ef1870ad8d3b6e6c03d`  
		Last Modified: Fri, 31 Oct 2025 00:50:24 GMT  
		Size: 190.8 MB (190844672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7460849a38eecaa02d67a471ffa18f69c5fa51f54a584e792bc89baece46efc`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c43143536b84e144969448d009b8aeba48716cefb394ec2d0549861006f4383`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcd3f3e82c803768cede882c734678a78a3bc587d5baa98aa91654403f20cfb`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0760830e46f553a3c445fa714aaa0bbcce24425ccee151fdfafc4031df31b1d`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e841bceac6aab182cb501d93b256e962fad806ae015dae2640a7f936720c7f19`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.5.21` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b3453230dae41986ec910b9dd820c23d4df56ac68bc8814818aadf053014aad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c016c7e2b79d154a365f0a085fabed20ec181b76a89890ef6d085f393d239b76`

```dockerfile
```

-	Layers:
	-	`sha256:4e6d502db8a447556f4f5558c96aef5270b6b4f517bed0e88ca0e114ce0e1566`  
		Last Modified: Fri, 31 Oct 2025 00:49:53 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9.5.21` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4c561844d47154da2cf18bf6fc308a9c1470ebd0b1557577abda7d8663dbd839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214126824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fd8eaba170a8cabde920b8dff74572a18fef475f1da56cf9c2855f6e4dbaf7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:20:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:20:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:20:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:20:39 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 21:20:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:21:07 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:21:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:21:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:21:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f2b54dec56f899e3541e6378d03e8cd182afe4eb4890b954deb8802842f910`  
		Last Modified: Thu, 30 Oct 2025 21:21:52 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3ffe7f678bcd6c880170754623c76b9248b55906cf055baf12b61fd5eef4ed`  
		Last Modified: Thu, 30 Oct 2025 21:50:23 GMT  
		Size: 178.3 MB (178296962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd97dc583a1c5bacf4be0631e5360f470d7b445747bdf2c1e39ab7c59092afb7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ac0b36c361fd8685c0f0c00ac426d3f75d0735f1fd9f3c71b4738dbf41f8d`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b892c789c4c82a60a77df538ce28170f3c71c1c7381ab0c590c490d13f6fef7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6da2b828b97d18e73c18a5c0b0811f1e365e04a58484841e5d282a130d9f34`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9dec9f0e0da6fcc5341e51c7153a7fb55efedbb4ee320a25539daf55c8e011`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.5.21` - unknown; unknown

```console
$ docker pull clickhouse@sha256:312f09886ff78060a641456578037587fbae0fae26fb8970a86de595d351c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a11d90d516ff1db5e847298e0bfda6cfe9477e57b25a8aaa5279ad2323fec60`

```dockerfile
```

-	Layers:
	-	`sha256:7c0633f1e88444ed45b99f3525f54cbe9baf7c926eb1cf5c8f5abfc8e32886a2`  
		Last Modified: Thu, 30 Oct 2025 21:49:57 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.5.21-jammy`

```console
$ docker pull clickhouse@sha256:ff986122e5bf19e5aef2ecabcd16bbe05c4a25e00bb67ae0b4ff6b7b11ad0488
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9.5.21-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:9d25aa64feac427c42cdf744ef9aa4f231acb86c15f152ddeefd90f6040ae723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228849900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51f737ce505cb0e8ea90024c9e5aa742f2cba374e233f4013ee4817b1711562`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:52:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:52:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:52:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:52:15 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:52:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:52:15 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 23:52:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:52:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:52:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:52:42 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:52:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:52:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:52:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:52:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:52:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2c05c65c48cae9023d76ef49327f9ff4a44fe42bace02531a518a8e6576377`  
		Last Modified: Thu, 30 Oct 2025 23:53:21 GMT  
		Size: 7.6 MB (7598386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b298cd9e89321c97630540ce9e3389f574c7103c453ef1870ad8d3b6e6c03d`  
		Last Modified: Fri, 31 Oct 2025 00:50:24 GMT  
		Size: 190.8 MB (190844672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7460849a38eecaa02d67a471ffa18f69c5fa51f54a584e792bc89baece46efc`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c43143536b84e144969448d009b8aeba48716cefb394ec2d0549861006f4383`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcd3f3e82c803768cede882c734678a78a3bc587d5baa98aa91654403f20cfb`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0760830e46f553a3c445fa714aaa0bbcce24425ccee151fdfafc4031df31b1d`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e841bceac6aab182cb501d93b256e962fad806ae015dae2640a7f936720c7f19`  
		Last Modified: Thu, 30 Oct 2025 23:53:20 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.5.21-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b3453230dae41986ec910b9dd820c23d4df56ac68bc8814818aadf053014aad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c016c7e2b79d154a365f0a085fabed20ec181b76a89890ef6d085f393d239b76`

```dockerfile
```

-	Layers:
	-	`sha256:4e6d502db8a447556f4f5558c96aef5270b6b4f517bed0e88ca0e114ce0e1566`  
		Last Modified: Fri, 31 Oct 2025 00:49:53 GMT  
		Size: 26.0 KB (26027 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9.5.21-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4c561844d47154da2cf18bf6fc308a9c1470ebd0b1557577abda7d8663dbd839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214126824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99fd8eaba170a8cabde920b8dff74572a18fef475f1da56cf9c2855f6e4dbaf7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:20:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:20:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:20:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:20:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:20:39 GMT
ARG VERSION=25.9.5.21
# Thu, 30 Oct 2025 21:20:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:21:07 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:21:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:21:07 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:21:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:21:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:21:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:21:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f2b54dec56f899e3541e6378d03e8cd182afe4eb4890b954deb8802842f910`  
		Last Modified: Thu, 30 Oct 2025 21:21:52 GMT  
		Size: 7.6 MB (7576733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb3ffe7f678bcd6c880170754623c76b9248b55906cf055baf12b61fd5eef4ed`  
		Last Modified: Thu, 30 Oct 2025 21:50:23 GMT  
		Size: 178.3 MB (178296962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd97dc583a1c5bacf4be0631e5360f470d7b445747bdf2c1e39ab7c59092afb7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75ac0b36c361fd8685c0f0c00ac426d3f75d0735f1fd9f3c71b4738dbf41f8d`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b892c789c4c82a60a77df538ce28170f3c71c1c7381ab0c590c490d13f6fef7`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf6da2b828b97d18e73c18a5c0b0811f1e365e04a58484841e5d282a130d9f34`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9dec9f0e0da6fcc5341e51c7153a7fb55efedbb4ee320a25539daf55c8e011`  
		Last Modified: Thu, 30 Oct 2025 21:21:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9.5.21-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:312f09886ff78060a641456578037587fbae0fae26fb8970a86de595d351c709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a11d90d516ff1db5e847298e0bfda6cfe9477e57b25a8aaa5279ad2323fec60`

```dockerfile
```

-	Layers:
	-	`sha256:7c0633f1e88444ed45b99f3525f54cbe9baf7c926eb1cf5c8f5abfc8e32886a2`  
		Last Modified: Thu, 30 Oct 2025 21:49:57 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:f6c922be45e9839765fa7fe54d8fd07e7586e582846148d4fbd2411cfb225ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e01ad927d22e7572a36afe57ca4ca6d7bc8db5d5aa457e9ccc55553989467d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231983028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed18c4d38249cc17224a423ebaa194a45a9879a04ffcc3efbfcad4a7e7cb040e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 19:15:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 19:15:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 19:15:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 19:15:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 19:15:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 19:15:42 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 19:15:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 19:16:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 19:16:08 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 19:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 19:16:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 19:16:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 19:16:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88985e9509ea1629450be2ab8c89146c92ea1cf4931088415b9ff8f449d4b8`  
		Last Modified: Thu, 13 Nov 2025 19:16:38 GMT  
		Size: 7.6 MB (7598439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f06b432c622ea0d9e76cf2e1432beb57e8099347beccb92d5901c44394d867`  
		Last Modified: Thu, 13 Nov 2025 19:24:13 GMT  
		Size: 194.0 MB (193977753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e3ebf007834804cf2fd69e7dcfe475383495c90a6ac018d22a04934ae8deca`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7dbe6c3ddb7197a037aa79c13d3413eb7519c78ff807343b057607e5f3ec46`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88056c2b344343d9ddfe0954ca13142dc996db2762a223ea06389161da8ae559`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524cc5ac590815922ccd84509b08c4ce30328d8491bfa9842fef50a3c9983e9`  
		Last Modified: Thu, 13 Nov 2025 19:16:36 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdbac4f40935b5ea01f16ef1fa1f782e492077f9a8dc39433bbd8afc3b56cdd`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e1d1f753653f1599f8d5f1c7b8e7bad43db50d7cfe829492a20b15d56bf81de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66664220cb146f7442a46a9fac3cae55dfb354386f11cb01777a6402b4a63e0`

```dockerfile
```

-	Layers:
	-	`sha256:d08aa577095fcdbfc4e7d98d089ae82582b0ee863182d769ea728dabba82a8c2`  
		Last Modified: Thu, 13 Nov 2025 22:49:23 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b59dd1ce4e937b016f358760aec66484b9d1ea017d0989f18ee2ec1d154326d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216505212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8a3f952674749e2c89d33889035b2a2a77f004233cd8972010c787390fa1c6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 19:15:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 19:15:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 19:15:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 19:15:34 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 19:15:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 19:15:34 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 19:15:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 19:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 19:16:00 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 19:16:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 19:16:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 19:16:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 19:16:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2fa1f30a833b6e9bf8e350076296e47b08ee1ffd285d54dc19ea7c6530dcd7`  
		Last Modified: Thu, 13 Nov 2025 19:16:30 GMT  
		Size: 7.6 MB (7576778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ddd361ee8ed98381de53c1966c215a47da7ee9dde28c8c09f054874d689b7d`  
		Last Modified: Thu, 13 Nov 2025 22:49:54 GMT  
		Size: 180.7 MB (180675306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4fe93b494f11751b7faae52f9c7f5243d91db541eab1a5f002c56abec049eb`  
		Last Modified: Thu, 13 Nov 2025 19:16:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7152fb6c08ae5cf804a0c6e73c0b37c0c0f15aa85e22e99b8e11f3c3958f13`  
		Last Modified: Thu, 13 Nov 2025 19:16:28 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72536613ce3993059c4aae363c7fd6b4b181282386c4fe1c9e27736690b30dd4`  
		Last Modified: Thu, 13 Nov 2025 19:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57bf763c9fdf56b96abda80c1eb82107a28e79544f1697c4f5c10e89517057b`  
		Last Modified: Thu, 13 Nov 2025 19:16:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c184d7f57e7058688e86fad093b4f63fa671baa0417191603dca9c35136c769`  
		Last Modified: Thu, 13 Nov 2025 19:16:28 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8ca9c6905562a6cb1de62190654202b87c25376a841df82745a5b758f1f70079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20f752b981d0d8b7359ae59f306f7847c7240f4b805bbbd6c3cda40c4c00c94`

```dockerfile
```

-	Layers:
	-	`sha256:be6fbcfc6db556e0e6c963eff3542fd7f0a591dc8e04312ddd9c3c305eb19033`  
		Last Modified: Thu, 13 Nov 2025 22:49:26 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:f6c922be45e9839765fa7fe54d8fd07e7586e582846148d4fbd2411cfb225ca7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:e01ad927d22e7572a36afe57ca4ca6d7bc8db5d5aa457e9ccc55553989467d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231983028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed18c4d38249cc17224a423ebaa194a45a9879a04ffcc3efbfcad4a7e7cb040e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 19:15:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 19:15:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 19:15:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 19:15:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 19:15:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 19:15:42 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 19:15:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 19:16:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 19:16:08 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 19:16:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:16:08 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 19:16:08 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 19:16:08 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 19:16:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e88985e9509ea1629450be2ab8c89146c92ea1cf4931088415b9ff8f449d4b8`  
		Last Modified: Thu, 13 Nov 2025 19:16:38 GMT  
		Size: 7.6 MB (7598439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f06b432c622ea0d9e76cf2e1432beb57e8099347beccb92d5901c44394d867`  
		Last Modified: Thu, 13 Nov 2025 19:24:13 GMT  
		Size: 194.0 MB (193977753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e3ebf007834804cf2fd69e7dcfe475383495c90a6ac018d22a04934ae8deca`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7dbe6c3ddb7197a037aa79c13d3413eb7519c78ff807343b057607e5f3ec46`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88056c2b344343d9ddfe0954ca13142dc996db2762a223ea06389161da8ae559`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a524cc5ac590815922ccd84509b08c4ce30328d8491bfa9842fef50a3c9983e9`  
		Last Modified: Thu, 13 Nov 2025 19:16:36 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdbac4f40935b5ea01f16ef1fa1f782e492077f9a8dc39433bbd8afc3b56cdd`  
		Last Modified: Thu, 13 Nov 2025 19:16:37 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e1d1f753653f1599f8d5f1c7b8e7bad43db50d7cfe829492a20b15d56bf81de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c66664220cb146f7442a46a9fac3cae55dfb354386f11cb01777a6402b4a63e0`

```dockerfile
```

-	Layers:
	-	`sha256:d08aa577095fcdbfc4e7d98d089ae82582b0ee863182d769ea728dabba82a8c2`  
		Last Modified: Thu, 13 Nov 2025 22:49:23 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b59dd1ce4e937b016f358760aec66484b9d1ea017d0989f18ee2ec1d154326d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216505212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf8a3f952674749e2c89d33889035b2a2a77f004233cd8972010c787390fa1c6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 19:15:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 19:15:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 19:15:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 19:15:34 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 19:15:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 19:15:34 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 19:15:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 19:15:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:15:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 19:16:00 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 19:16:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 19:16:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 19:16:00 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 19:16:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 19:16:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2fa1f30a833b6e9bf8e350076296e47b08ee1ffd285d54dc19ea7c6530dcd7`  
		Last Modified: Thu, 13 Nov 2025 19:16:30 GMT  
		Size: 7.6 MB (7576778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ddd361ee8ed98381de53c1966c215a47da7ee9dde28c8c09f054874d689b7d`  
		Last Modified: Thu, 13 Nov 2025 22:49:54 GMT  
		Size: 180.7 MB (180675306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4fe93b494f11751b7faae52f9c7f5243d91db541eab1a5f002c56abec049eb`  
		Last Modified: Thu, 13 Nov 2025 19:16:29 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d7152fb6c08ae5cf804a0c6e73c0b37c0c0f15aa85e22e99b8e11f3c3958f13`  
		Last Modified: Thu, 13 Nov 2025 19:16:28 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72536613ce3993059c4aae363c7fd6b4b181282386c4fe1c9e27736690b30dd4`  
		Last Modified: Thu, 13 Nov 2025 19:16:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57bf763c9fdf56b96abda80c1eb82107a28e79544f1697c4f5c10e89517057b`  
		Last Modified: Thu, 13 Nov 2025 19:16:29 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c184d7f57e7058688e86fad093b4f63fa671baa0417191603dca9c35136c769`  
		Last Modified: Thu, 13 Nov 2025 19:16:28 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:8ca9c6905562a6cb1de62190654202b87c25376a841df82745a5b758f1f70079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c20f752b981d0d8b7359ae59f306f7847c7240f4b805bbbd6c3cda40c4c00c94`

```dockerfile
```

-	Layers:
	-	`sha256:be6fbcfc6db556e0e6c963eff3542fd7f0a591dc8e04312ddd9c3c305eb19033`  
		Last Modified: Thu, 13 Nov 2025 22:49:26 GMT  
		Size: 26.3 KB (26259 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:3f7319c4094584ea1e527d2fe8bc7c0d03356774449fae9d00bfe6b770bc5cc0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:c090f2f5be6364821b31be1fbd278413fb83b2e07122f8ff19e535deeb49f14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227833727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c563c7d8483b10b76dda7c4b0c1da80a4773542b2afa2f2d9cd06ec480369be0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:53:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:53:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:53:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:53:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:53:59 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 23:53:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:54:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:54:25 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:54:25 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:54:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:54:26 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:54:26 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:54:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ddbf1790aac818fc42043394030555dceee7d2402503ea1743acf316968d5d`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 7.6 MB (7598359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b71c2c8a6ff701f53316322e9dd4bab196a266dc009bb2642f9cc4cc6caf9`  
		Last Modified: Fri, 31 Oct 2025 00:50:15 GMT  
		Size: 189.8 MB (189828532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73dc43b82a4c8bf9823bbb7346ac5304f1e7302ea3d97bfb79998562e698782`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad672abd047ac6ffd6ebc6408fb07df6b27bbf64dc47c3c30b54ee8d80b3a5f`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a242d7ec651eceebf026fa9215a574414c4eaf6ed28bb29bbeffb7a50ad8548`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4314f6c48d0c800956cec3e5857ae521dac0be0b82ebded9a9d63e887ed507`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989775034b6f9aeeb688b71bcedc51726f96e3fc855f085ec2fecb490a58374`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e36034a604435695fcb941e3af130db42f3e896ad9dc828774738d39d76754f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb4c979459bf8105d26754d11eaf2bf40538e89af14f65f43fbe10200781337`

```dockerfile
```

-	Layers:
	-	`sha256:51240151cc461d203bfe9dbb7ca87497417d94bc660f5cb1aa4ce6aed96b35db`  
		Last Modified: Fri, 31 Oct 2025 00:49:35 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a5656778631ee59482d9821f008c2f43704a533bb78ce9fabe3f9e735055b882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212645310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cee591520bd679efa5bdfc5ccbbe8955c161e8ce6052107b9f0192bb2d962`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:21:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:43 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 21:21:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:12 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7ce10c9eeca1dd1885578ad8f3f6291f3732bdf5a50a8a6535af67a72e81f`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee964fa2145e136ca73e4c3796c405f427a709e6070f3f4802f8e19f6723677`  
		Last Modified: Thu, 30 Oct 2025 21:50:09 GMT  
		Size: 176.8 MB (176815492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59e47ba03552bfa2a66ef28e55b44868ad4666ae67b5fe3e408e5c5a79ca85`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9616189aee41fb2150e3b2e7df745964d4e966fb63f6a7a431d6d848dfc358`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163c00ab90daa2465b1046a4d0b95388778dc70b143011610dca4fb7590de31`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47157a68ab31f8dfb08a2352278276b514a9773b046ac4dca1504822e01e8856`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda603cdd01780ad677c4f16ef238ba487aa146cd3f5d06542f066c10b93575`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:557ba9743467f6d9ecfb1670d9fb813858720e1ed9612956f837ce4eb5cf0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30079417e65d20ad6f0ad236690d7babc98d5d1128642255422497d2ca46316f`

```dockerfile
```

-	Layers:
	-	`sha256:cdecb34f64c1ba351dec1bcc4a2182fa4b916423bfa5f3853e9f82069f25386a`  
		Last Modified: Thu, 30 Oct 2025 21:49:42 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:3f7319c4094584ea1e527d2fe8bc7c0d03356774449fae9d00bfe6b770bc5cc0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:c090f2f5be6364821b31be1fbd278413fb83b2e07122f8ff19e535deeb49f14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227833727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c563c7d8483b10b76dda7c4b0c1da80a4773542b2afa2f2d9cd06ec480369be0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 23:53:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 23:53:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 23:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 23:53:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 23:53:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 23:53:59 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 23:53:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 23:54:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:24 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 23:54:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 23:54:25 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 23:54:25 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 23:54:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 23:54:26 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 23:54:26 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 23:54:26 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 23:54:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ddbf1790aac818fc42043394030555dceee7d2402503ea1743acf316968d5d`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 7.6 MB (7598359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50b71c2c8a6ff701f53316322e9dd4bab196a266dc009bb2642f9cc4cc6caf9`  
		Last Modified: Fri, 31 Oct 2025 00:50:15 GMT  
		Size: 189.8 MB (189828532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c73dc43b82a4c8bf9823bbb7346ac5304f1e7302ea3d97bfb79998562e698782`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ad672abd047ac6ffd6ebc6408fb07df6b27bbf64dc47c3c30b54ee8d80b3a5f`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a242d7ec651eceebf026fa9215a574414c4eaf6ed28bb29bbeffb7a50ad8548`  
		Last Modified: Thu, 30 Oct 2025 23:54:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4314f6c48d0c800956cec3e5857ae521dac0be0b82ebded9a9d63e887ed507`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0989775034b6f9aeeb688b71bcedc51726f96e3fc855f085ec2fecb490a58374`  
		Last Modified: Thu, 30 Oct 2025 23:54:58 GMT  
		Size: 3.6 KB (3609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e36034a604435695fcb941e3af130db42f3e896ad9dc828774738d39d76754f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb4c979459bf8105d26754d11eaf2bf40538e89af14f65f43fbe10200781337`

```dockerfile
```

-	Layers:
	-	`sha256:51240151cc461d203bfe9dbb7ca87497417d94bc660f5cb1aa4ce6aed96b35db`  
		Last Modified: Fri, 31 Oct 2025 00:49:35 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:a5656778631ee59482d9821f008c2f43704a533bb78ce9fabe3f9e735055b882
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212645310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:636cee591520bd679efa5bdfc5ccbbe8955c161e8ce6052107b9f0192bb2d962`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Thu, 30 Oct 2025 21:21:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 30 Oct 2025 21:21:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 30 Oct 2025 21:21:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPO_CHANNEL=stable
# Thu, 30 Oct 2025 21:21:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 30 Oct 2025 21:21:43 GMT
ARG VERSION=25.8.11.66
# Thu, 30 Oct 2025 21:21:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
ENV LANG=en_US.UTF-8
# Thu, 30 Oct 2025 21:22:12 GMT
ENV TZ=UTC
# Thu, 30 Oct 2025 21:22:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 30 Oct 2025 21:22:12 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 30 Oct 2025 21:22:12 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 30 Oct 2025 21:22:12 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 30 Oct 2025 21:22:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce7ce10c9eeca1dd1885578ad8f3f6291f3732bdf5a50a8a6535af67a72e81f`  
		Last Modified: Thu, 30 Oct 2025 21:22:52 GMT  
		Size: 7.6 MB (7576689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee964fa2145e136ca73e4c3796c405f427a709e6070f3f4802f8e19f6723677`  
		Last Modified: Thu, 30 Oct 2025 21:50:09 GMT  
		Size: 176.8 MB (176815492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd59e47ba03552bfa2a66ef28e55b44868ad4666ae67b5fe3e408e5c5a79ca85`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d9616189aee41fb2150e3b2e7df745964d4e966fb63f6a7a431d6d848dfc358`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e163c00ab90daa2465b1046a4d0b95388778dc70b143011610dca4fb7590de31`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47157a68ab31f8dfb08a2352278276b514a9773b046ac4dca1504822e01e8856`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dda603cdd01780ad677c4f16ef238ba487aa146cd3f5d06542f066c10b93575`  
		Last Modified: Thu, 30 Oct 2025 21:22:51 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:557ba9743467f6d9ecfb1670d9fb813858720e1ed9612956f837ce4eb5cf0dee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30079417e65d20ad6f0ad236690d7babc98d5d1128642255422497d2ca46316f`

```dockerfile
```

-	Layers:
	-	`sha256:cdecb34f64c1ba351dec1bcc4a2182fa4b916423bfa5f3853e9f82069f25386a`  
		Last Modified: Thu, 30 Oct 2025 21:49:42 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json
