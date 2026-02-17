<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.11`](#clickhouse2511)
-	[`clickhouse:25.11-jammy`](#clickhouse2511-jammy)
-	[`clickhouse:25.11.8`](#clickhouse25118)
-	[`clickhouse:25.11.8-jammy`](#clickhouse25118-jammy)
-	[`clickhouse:25.11.8.25`](#clickhouse2511825)
-	[`clickhouse:25.11.8.25-jammy`](#clickhouse2511825-jammy)
-	[`clickhouse:25.12`](#clickhouse2512)
-	[`clickhouse:25.12-jammy`](#clickhouse2512-jammy)
-	[`clickhouse:25.12.5`](#clickhouse25125)
-	[`clickhouse:25.12.5-jammy`](#clickhouse25125-jammy)
-	[`clickhouse:25.12.5.44`](#clickhouse2512544)
-	[`clickhouse:25.12.5.44-jammy`](#clickhouse2512544-jammy)
-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.14`](#clickhouse25314)
-	[`clickhouse:25.3.14-jammy`](#clickhouse25314-jammy)
-	[`clickhouse:25.3.14.14`](#clickhouse2531414)
-	[`clickhouse:25.3.14.14-jammy`](#clickhouse2531414-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.16`](#clickhouse25816)
-	[`clickhouse:25.8.16-jammy`](#clickhouse25816-jammy)
-	[`clickhouse:25.8.16.34`](#clickhouse2581634)
-	[`clickhouse:25.8.16.34-jammy`](#clickhouse2581634-jammy)
-	[`clickhouse:26.1`](#clickhouse261)
-	[`clickhouse:26.1-jammy`](#clickhouse261-jammy)
-	[`clickhouse:26.1.2`](#clickhouse2612)
-	[`clickhouse:26.1.2-jammy`](#clickhouse2612-jammy)
-	[`clickhouse:26.1.2.11`](#clickhouse261211)
-	[`clickhouse:26.1.2.11-jammy`](#clickhouse261211-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.11`

```console
$ docker pull clickhouse@sha256:ccd16b8ac297dca4114beed3e3f190e9d5e7ea9364a594eceb122ff1853bda1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:f32d20068e28f7661fe2c42ea2d0716016674a6d17b4bfdb0e9691a061cc3839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aa2c176b01d0cf3e17502bd7abb990041c97b33db244f6674977601a0f77c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:14 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:14 GMT
ARG VERSION=25.11.8.25
# Tue, 17 Feb 2026 20:12:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:39 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:39 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9d150c9ff99086b807e3678935d4da99d9683aa3608527a0e77a9cf4d88a84`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 7.6 MB (7598371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742b48bbb0cf1130fee35ea6b4b3add878b06f846c4e213453fa127086257a4f`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 195.9 MB (195939044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2f8a6da401457e599ee0b58e94fe29bf58fd2d405bc4f8265e277f6fee196`  
		Last Modified: Tue, 17 Feb 2026 20:12:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3832510b4a5eb5a416a1b42ffa703a98f6c79a7faff2d8f197f9600eb6a17c08`  
		Last Modified: Tue, 17 Feb 2026 20:12:59 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76573b3557c2f10baafa409931c333bb0c026bf0aeca634bdc066533ccf6f2b4`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531a11fbbc5c4871abd9085604715ded8c2213b49ec9b80a2343998c4094bb52`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d06fb32286e4fc75405da033b2427f8692a4b69909d8b7bb96ea78509e13d8`  
		Last Modified: Tue, 17 Feb 2026 20:13:01 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d41187c1e9fcad326efa6fecc3bf52c3148765ae739d548e2a8fc442be606dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0345d53d0a13bbfcfe4125bfa2c7807e48b941459fc3e291ebda048178d73c7a`

```dockerfile
```

-	Layers:
	-	`sha256:f1237f1f75186fb0ba0b3b0a65791fa7687e11b9a77f81935680620d5805b0bc`  
		Last Modified: Tue, 17 Feb 2026 20:12:58 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1fbb24394e790a78b52d188e945afbeaef347b6fbbfe84f1a19894422727c53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218829691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b6d85f978a032d669893e6ae13ea2220a320a91aee140d1777279c9d4f09d9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:15 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:15 GMT
ARG VERSION=25.11.8.25
# Tue, 17 Feb 2026 20:11:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:11:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:11:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:11:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:11:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:11:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5278748135bd2b865b7028139a87207921524fbf46221ff518a864f03aeec0`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 7.6 MB (7577440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd56c430974029f0b1b77b5b6b6819e81a1920e0cdb1edf3a187b8a0f7c90531`  
		Last Modified: Tue, 17 Feb 2026 20:12:06 GMT  
		Size: 183.0 MB (182997267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b72a3c23b7348f096e0ddd699099502f22884613c0b137ceb02c23ecf9e4e7`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226cd2b473689d2f66d11e6b74f5369c2450290b5202c09b2d414a1ef7a99f7b`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37fa23e4bd88270ca3ac242525911615e56ccb1cdb5948e5537a0086380a747`  
		Last Modified: Tue, 17 Feb 2026 20:12:04 GMT  
		Size: 112.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da6a058db9a898b5102faf464e981c3ae60874a9464d4ff95a02afba612f530`  
		Last Modified: Tue, 17 Feb 2026 20:12:04 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb636331124ecda26ce5d3fa2184529b15898a482600824889f3ace84008b538`  
		Last Modified: Tue, 17 Feb 2026 20:12:05 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6e428607ff260f225db0780567c96218726d71633bd5c5d908ae3e09c7d5409f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdbf047c774478b3e820861a565542b04dca1960b2901a30d489c313d08a2f6`

```dockerfile
```

-	Layers:
	-	`sha256:be6b45e80bf7bec77c9220ba27cfb49cfb3b0e88c26b90151540c9b881139bce`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11-jammy`

```console
$ docker pull clickhouse@sha256:ccd16b8ac297dca4114beed3e3f190e9d5e7ea9364a594eceb122ff1853bda1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f32d20068e28f7661fe2c42ea2d0716016674a6d17b4bfdb0e9691a061cc3839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aa2c176b01d0cf3e17502bd7abb990041c97b33db244f6674977601a0f77c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:14 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:14 GMT
ARG VERSION=25.11.8.25
# Tue, 17 Feb 2026 20:12:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:39 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:39 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9d150c9ff99086b807e3678935d4da99d9683aa3608527a0e77a9cf4d88a84`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 7.6 MB (7598371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742b48bbb0cf1130fee35ea6b4b3add878b06f846c4e213453fa127086257a4f`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 195.9 MB (195939044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2f8a6da401457e599ee0b58e94fe29bf58fd2d405bc4f8265e277f6fee196`  
		Last Modified: Tue, 17 Feb 2026 20:12:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3832510b4a5eb5a416a1b42ffa703a98f6c79a7faff2d8f197f9600eb6a17c08`  
		Last Modified: Tue, 17 Feb 2026 20:12:59 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76573b3557c2f10baafa409931c333bb0c026bf0aeca634bdc066533ccf6f2b4`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531a11fbbc5c4871abd9085604715ded8c2213b49ec9b80a2343998c4094bb52`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d06fb32286e4fc75405da033b2427f8692a4b69909d8b7bb96ea78509e13d8`  
		Last Modified: Tue, 17 Feb 2026 20:13:01 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d41187c1e9fcad326efa6fecc3bf52c3148765ae739d548e2a8fc442be606dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0345d53d0a13bbfcfe4125bfa2c7807e48b941459fc3e291ebda048178d73c7a`

```dockerfile
```

-	Layers:
	-	`sha256:f1237f1f75186fb0ba0b3b0a65791fa7687e11b9a77f81935680620d5805b0bc`  
		Last Modified: Tue, 17 Feb 2026 20:12:58 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1fbb24394e790a78b52d188e945afbeaef347b6fbbfe84f1a19894422727c53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218829691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b6d85f978a032d669893e6ae13ea2220a320a91aee140d1777279c9d4f09d9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:15 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:15 GMT
ARG VERSION=25.11.8.25
# Tue, 17 Feb 2026 20:11:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:11:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:11:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:11:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:11:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:11:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5278748135bd2b865b7028139a87207921524fbf46221ff518a864f03aeec0`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 7.6 MB (7577440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd56c430974029f0b1b77b5b6b6819e81a1920e0cdb1edf3a187b8a0f7c90531`  
		Last Modified: Tue, 17 Feb 2026 20:12:06 GMT  
		Size: 183.0 MB (182997267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b72a3c23b7348f096e0ddd699099502f22884613c0b137ceb02c23ecf9e4e7`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226cd2b473689d2f66d11e6b74f5369c2450290b5202c09b2d414a1ef7a99f7b`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37fa23e4bd88270ca3ac242525911615e56ccb1cdb5948e5537a0086380a747`  
		Last Modified: Tue, 17 Feb 2026 20:12:04 GMT  
		Size: 112.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da6a058db9a898b5102faf464e981c3ae60874a9464d4ff95a02afba612f530`  
		Last Modified: Tue, 17 Feb 2026 20:12:04 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb636331124ecda26ce5d3fa2184529b15898a482600824889f3ace84008b538`  
		Last Modified: Tue, 17 Feb 2026 20:12:05 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6e428607ff260f225db0780567c96218726d71633bd5c5d908ae3e09c7d5409f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdbf047c774478b3e820861a565542b04dca1960b2901a30d489c313d08a2f6`

```dockerfile
```

-	Layers:
	-	`sha256:be6b45e80bf7bec77c9220ba27cfb49cfb3b0e88c26b90151540c9b881139bce`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.8`

```console
$ docker pull clickhouse@sha256:ccd16b8ac297dca4114beed3e3f190e9d5e7ea9364a594eceb122ff1853bda1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:f32d20068e28f7661fe2c42ea2d0716016674a6d17b4bfdb0e9691a061cc3839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aa2c176b01d0cf3e17502bd7abb990041c97b33db244f6674977601a0f77c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:14 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:14 GMT
ARG VERSION=25.11.8.25
# Tue, 17 Feb 2026 20:12:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:39 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:39 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9d150c9ff99086b807e3678935d4da99d9683aa3608527a0e77a9cf4d88a84`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 7.6 MB (7598371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742b48bbb0cf1130fee35ea6b4b3add878b06f846c4e213453fa127086257a4f`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 195.9 MB (195939044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2f8a6da401457e599ee0b58e94fe29bf58fd2d405bc4f8265e277f6fee196`  
		Last Modified: Tue, 17 Feb 2026 20:12:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3832510b4a5eb5a416a1b42ffa703a98f6c79a7faff2d8f197f9600eb6a17c08`  
		Last Modified: Tue, 17 Feb 2026 20:12:59 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76573b3557c2f10baafa409931c333bb0c026bf0aeca634bdc066533ccf6f2b4`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531a11fbbc5c4871abd9085604715ded8c2213b49ec9b80a2343998c4094bb52`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d06fb32286e4fc75405da033b2427f8692a4b69909d8b7bb96ea78509e13d8`  
		Last Modified: Tue, 17 Feb 2026 20:13:01 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d41187c1e9fcad326efa6fecc3bf52c3148765ae739d548e2a8fc442be606dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0345d53d0a13bbfcfe4125bfa2c7807e48b941459fc3e291ebda048178d73c7a`

```dockerfile
```

-	Layers:
	-	`sha256:f1237f1f75186fb0ba0b3b0a65791fa7687e11b9a77f81935680620d5805b0bc`  
		Last Modified: Tue, 17 Feb 2026 20:12:58 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1fbb24394e790a78b52d188e945afbeaef347b6fbbfe84f1a19894422727c53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218829691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b6d85f978a032d669893e6ae13ea2220a320a91aee140d1777279c9d4f09d9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:15 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:15 GMT
ARG VERSION=25.11.8.25
# Tue, 17 Feb 2026 20:11:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:11:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:11:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:11:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:11:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:11:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5278748135bd2b865b7028139a87207921524fbf46221ff518a864f03aeec0`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 7.6 MB (7577440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd56c430974029f0b1b77b5b6b6819e81a1920e0cdb1edf3a187b8a0f7c90531`  
		Last Modified: Tue, 17 Feb 2026 20:12:06 GMT  
		Size: 183.0 MB (182997267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b72a3c23b7348f096e0ddd699099502f22884613c0b137ceb02c23ecf9e4e7`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226cd2b473689d2f66d11e6b74f5369c2450290b5202c09b2d414a1ef7a99f7b`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37fa23e4bd88270ca3ac242525911615e56ccb1cdb5948e5537a0086380a747`  
		Last Modified: Tue, 17 Feb 2026 20:12:04 GMT  
		Size: 112.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da6a058db9a898b5102faf464e981c3ae60874a9464d4ff95a02afba612f530`  
		Last Modified: Tue, 17 Feb 2026 20:12:04 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb636331124ecda26ce5d3fa2184529b15898a482600824889f3ace84008b538`  
		Last Modified: Tue, 17 Feb 2026 20:12:05 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6e428607ff260f225db0780567c96218726d71633bd5c5d908ae3e09c7d5409f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdbf047c774478b3e820861a565542b04dca1960b2901a30d489c313d08a2f6`

```dockerfile
```

-	Layers:
	-	`sha256:be6b45e80bf7bec77c9220ba27cfb49cfb3b0e88c26b90151540c9b881139bce`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.8-jammy`

```console
$ docker pull clickhouse@sha256:ccd16b8ac297dca4114beed3e3f190e9d5e7ea9364a594eceb122ff1853bda1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f32d20068e28f7661fe2c42ea2d0716016674a6d17b4bfdb0e9691a061cc3839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aa2c176b01d0cf3e17502bd7abb990041c97b33db244f6674977601a0f77c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:14 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:14 GMT
ARG VERSION=25.11.8.25
# Tue, 17 Feb 2026 20:12:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:39 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:39 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9d150c9ff99086b807e3678935d4da99d9683aa3608527a0e77a9cf4d88a84`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 7.6 MB (7598371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742b48bbb0cf1130fee35ea6b4b3add878b06f846c4e213453fa127086257a4f`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 195.9 MB (195939044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2f8a6da401457e599ee0b58e94fe29bf58fd2d405bc4f8265e277f6fee196`  
		Last Modified: Tue, 17 Feb 2026 20:12:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3832510b4a5eb5a416a1b42ffa703a98f6c79a7faff2d8f197f9600eb6a17c08`  
		Last Modified: Tue, 17 Feb 2026 20:12:59 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76573b3557c2f10baafa409931c333bb0c026bf0aeca634bdc066533ccf6f2b4`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531a11fbbc5c4871abd9085604715ded8c2213b49ec9b80a2343998c4094bb52`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d06fb32286e4fc75405da033b2427f8692a4b69909d8b7bb96ea78509e13d8`  
		Last Modified: Tue, 17 Feb 2026 20:13:01 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d41187c1e9fcad326efa6fecc3bf52c3148765ae739d548e2a8fc442be606dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0345d53d0a13bbfcfe4125bfa2c7807e48b941459fc3e291ebda048178d73c7a`

```dockerfile
```

-	Layers:
	-	`sha256:f1237f1f75186fb0ba0b3b0a65791fa7687e11b9a77f81935680620d5805b0bc`  
		Last Modified: Tue, 17 Feb 2026 20:12:58 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1fbb24394e790a78b52d188e945afbeaef347b6fbbfe84f1a19894422727c53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218829691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b6d85f978a032d669893e6ae13ea2220a320a91aee140d1777279c9d4f09d9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:15 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:15 GMT
ARG VERSION=25.11.8.25
# Tue, 17 Feb 2026 20:11:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:11:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:11:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:11:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:11:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:11:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5278748135bd2b865b7028139a87207921524fbf46221ff518a864f03aeec0`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 7.6 MB (7577440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd56c430974029f0b1b77b5b6b6819e81a1920e0cdb1edf3a187b8a0f7c90531`  
		Last Modified: Tue, 17 Feb 2026 20:12:06 GMT  
		Size: 183.0 MB (182997267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b72a3c23b7348f096e0ddd699099502f22884613c0b137ceb02c23ecf9e4e7`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226cd2b473689d2f66d11e6b74f5369c2450290b5202c09b2d414a1ef7a99f7b`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37fa23e4bd88270ca3ac242525911615e56ccb1cdb5948e5537a0086380a747`  
		Last Modified: Tue, 17 Feb 2026 20:12:04 GMT  
		Size: 112.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da6a058db9a898b5102faf464e981c3ae60874a9464d4ff95a02afba612f530`  
		Last Modified: Tue, 17 Feb 2026 20:12:04 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb636331124ecda26ce5d3fa2184529b15898a482600824889f3ace84008b538`  
		Last Modified: Tue, 17 Feb 2026 20:12:05 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6e428607ff260f225db0780567c96218726d71633bd5c5d908ae3e09c7d5409f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdbf047c774478b3e820861a565542b04dca1960b2901a30d489c313d08a2f6`

```dockerfile
```

-	Layers:
	-	`sha256:be6b45e80bf7bec77c9220ba27cfb49cfb3b0e88c26b90151540c9b881139bce`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.8.25`

```console
$ docker pull clickhouse@sha256:ccd16b8ac297dca4114beed3e3f190e9d5e7ea9364a594eceb122ff1853bda1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.8.25` - linux; amd64

```console
$ docker pull clickhouse@sha256:f32d20068e28f7661fe2c42ea2d0716016674a6d17b4bfdb0e9691a061cc3839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aa2c176b01d0cf3e17502bd7abb990041c97b33db244f6674977601a0f77c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:14 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:14 GMT
ARG VERSION=25.11.8.25
# Tue, 17 Feb 2026 20:12:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:39 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:39 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9d150c9ff99086b807e3678935d4da99d9683aa3608527a0e77a9cf4d88a84`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 7.6 MB (7598371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742b48bbb0cf1130fee35ea6b4b3add878b06f846c4e213453fa127086257a4f`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 195.9 MB (195939044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2f8a6da401457e599ee0b58e94fe29bf58fd2d405bc4f8265e277f6fee196`  
		Last Modified: Tue, 17 Feb 2026 20:12:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3832510b4a5eb5a416a1b42ffa703a98f6c79a7faff2d8f197f9600eb6a17c08`  
		Last Modified: Tue, 17 Feb 2026 20:12:59 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76573b3557c2f10baafa409931c333bb0c026bf0aeca634bdc066533ccf6f2b4`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531a11fbbc5c4871abd9085604715ded8c2213b49ec9b80a2343998c4094bb52`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d06fb32286e4fc75405da033b2427f8692a4b69909d8b7bb96ea78509e13d8`  
		Last Modified: Tue, 17 Feb 2026 20:13:01 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8.25` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d41187c1e9fcad326efa6fecc3bf52c3148765ae739d548e2a8fc442be606dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0345d53d0a13bbfcfe4125bfa2c7807e48b941459fc3e291ebda048178d73c7a`

```dockerfile
```

-	Layers:
	-	`sha256:f1237f1f75186fb0ba0b3b0a65791fa7687e11b9a77f81935680620d5805b0bc`  
		Last Modified: Tue, 17 Feb 2026 20:12:58 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.8.25` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1fbb24394e790a78b52d188e945afbeaef347b6fbbfe84f1a19894422727c53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218829691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b6d85f978a032d669893e6ae13ea2220a320a91aee140d1777279c9d4f09d9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:15 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:15 GMT
ARG VERSION=25.11.8.25
# Tue, 17 Feb 2026 20:11:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:11:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:11:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:11:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:11:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:11:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5278748135bd2b865b7028139a87207921524fbf46221ff518a864f03aeec0`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 7.6 MB (7577440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd56c430974029f0b1b77b5b6b6819e81a1920e0cdb1edf3a187b8a0f7c90531`  
		Last Modified: Tue, 17 Feb 2026 20:12:06 GMT  
		Size: 183.0 MB (182997267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b72a3c23b7348f096e0ddd699099502f22884613c0b137ceb02c23ecf9e4e7`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226cd2b473689d2f66d11e6b74f5369c2450290b5202c09b2d414a1ef7a99f7b`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37fa23e4bd88270ca3ac242525911615e56ccb1cdb5948e5537a0086380a747`  
		Last Modified: Tue, 17 Feb 2026 20:12:04 GMT  
		Size: 112.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da6a058db9a898b5102faf464e981c3ae60874a9464d4ff95a02afba612f530`  
		Last Modified: Tue, 17 Feb 2026 20:12:04 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb636331124ecda26ce5d3fa2184529b15898a482600824889f3ace84008b538`  
		Last Modified: Tue, 17 Feb 2026 20:12:05 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8.25` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6e428607ff260f225db0780567c96218726d71633bd5c5d908ae3e09c7d5409f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdbf047c774478b3e820861a565542b04dca1960b2901a30d489c313d08a2f6`

```dockerfile
```

-	Layers:
	-	`sha256:be6b45e80bf7bec77c9220ba27cfb49cfb3b0e88c26b90151540c9b881139bce`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.8.25-jammy`

```console
$ docker pull clickhouse@sha256:ccd16b8ac297dca4114beed3e3f190e9d5e7ea9364a594eceb122ff1853bda1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.8.25-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f32d20068e28f7661fe2c42ea2d0716016674a6d17b4bfdb0e9691a061cc3839
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe2aa2c176b01d0cf3e17502bd7abb990041c97b33db244f6674977601a0f77c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:14 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:14 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:14 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:14 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:14 GMT
ARG VERSION=25.11.8.25
# Tue, 17 Feb 2026 20:12:14 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:39 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:39 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc9d150c9ff99086b807e3678935d4da99d9683aa3608527a0e77a9cf4d88a84`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 7.6 MB (7598371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742b48bbb0cf1130fee35ea6b4b3add878b06f846c4e213453fa127086257a4f`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 195.9 MB (195939044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96a2f8a6da401457e599ee0b58e94fe29bf58fd2d405bc4f8265e277f6fee196`  
		Last Modified: Tue, 17 Feb 2026 20:12:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3832510b4a5eb5a416a1b42ffa703a98f6c79a7faff2d8f197f9600eb6a17c08`  
		Last Modified: Tue, 17 Feb 2026 20:12:59 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76573b3557c2f10baafa409931c333bb0c026bf0aeca634bdc066533ccf6f2b4`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531a11fbbc5c4871abd9085604715ded8c2213b49ec9b80a2343998c4094bb52`  
		Last Modified: Tue, 17 Feb 2026 20:13:00 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d06fb32286e4fc75405da033b2427f8692a4b69909d8b7bb96ea78509e13d8`  
		Last Modified: Tue, 17 Feb 2026 20:13:01 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8.25-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d41187c1e9fcad326efa6fecc3bf52c3148765ae739d548e2a8fc442be606dc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0345d53d0a13bbfcfe4125bfa2c7807e48b941459fc3e291ebda048178d73c7a`

```dockerfile
```

-	Layers:
	-	`sha256:f1237f1f75186fb0ba0b3b0a65791fa7687e11b9a77f81935680620d5805b0bc`  
		Last Modified: Tue, 17 Feb 2026 20:12:58 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.8.25-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:1fbb24394e790a78b52d188e945afbeaef347b6fbbfe84f1a19894422727c53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218829691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2b6d85f978a032d669893e6ae13ea2220a320a91aee140d1777279c9d4f09d9`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:15 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:15 GMT
ARG VERSION=25.11.8.25
# Tue, 17 Feb 2026 20:11:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:11:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:11:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:11:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:11:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:11:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:11:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb5278748135bd2b865b7028139a87207921524fbf46221ff518a864f03aeec0`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 7.6 MB (7577440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd56c430974029f0b1b77b5b6b6819e81a1920e0cdb1edf3a187b8a0f7c90531`  
		Last Modified: Tue, 17 Feb 2026 20:12:06 GMT  
		Size: 183.0 MB (182997267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b72a3c23b7348f096e0ddd699099502f22884613c0b137ceb02c23ecf9e4e7`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226cd2b473689d2f66d11e6b74f5369c2450290b5202c09b2d414a1ef7a99f7b`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 865.7 KB (865748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37fa23e4bd88270ca3ac242525911615e56ccb1cdb5948e5537a0086380a747`  
		Last Modified: Tue, 17 Feb 2026 20:12:04 GMT  
		Size: 112.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da6a058db9a898b5102faf464e981c3ae60874a9464d4ff95a02afba612f530`  
		Last Modified: Tue, 17 Feb 2026 20:12:04 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb636331124ecda26ce5d3fa2184529b15898a482600824889f3ace84008b538`  
		Last Modified: Tue, 17 Feb 2026 20:12:05 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8.25-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6e428607ff260f225db0780567c96218726d71633bd5c5d908ae3e09c7d5409f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdbf047c774478b3e820861a565542b04dca1960b2901a30d489c313d08a2f6`

```dockerfile
```

-	Layers:
	-	`sha256:be6b45e80bf7bec77c9220ba27cfb49cfb3b0e88c26b90151540c9b881139bce`  
		Last Modified: Tue, 17 Feb 2026 20:12:03 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12`

```console
$ docker pull clickhouse@sha256:2321bd600611139f9bb7265d170ab0bdfad5790b6d5fa0db3ce1476a5c96ec51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12` - linux; amd64

```console
$ docker pull clickhouse@sha256:0234c146e2ada07696d3b78214b3aa6d7be283ab70e5eb77f4cd3d566b0e6cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246337052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73140c89608e3bbffe181bbfb5e990dd53f526897d3496c0da3758a311a8883a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:53 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:53 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:53 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:53 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:53 GMT
ARG VERSION=25.12.5.44
# Tue, 17 Feb 2026 20:11:53 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:22 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:22 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0265759b2c9568c995905af6c4660fc2821ffbb20f8b491129324ac758b862b7`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 7.6 MB (7598343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feab4d6a05aead20c3dc14e61f73b3e296b703c9765a71e7722494886e4bfe36`  
		Last Modified: Tue, 17 Feb 2026 20:12:54 GMT  
		Size: 208.3 MB (208331298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8b29bd28eec82baaccdb71d33cfbf8ce51b815bfa91f0e50d0f7b58cdee994`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2f47d985a3157d7b6f7f3651533c3da6d9140452099cf3c3fc35051d592b7f`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e96360c2d10134667e54c02a3436bef43841556cd299b11f3694aa7735f7bb`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ef6e8e2d68cd939dd47891dcae496113d2098b78600955e039121f651308a`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a21da2e50caf1756948c84ef75b8e826739b607c64dbf128fbdead8f3b389`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:624ca399136baac93922dd527aca4d8bb02ddde80cf3723fb94f207198686f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c6627c353a22d7bd470c2689c11efce04a7a697ed4c2f30bf769fd14060758`

```dockerfile
```

-	Layers:
	-	`sha256:23ca4ec631b96fa89d3ae9ae56dcf08b8074cb4d5199c96d7187a60246f702c3`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f967a788d5f14f6295a4e8e5d83167c7753b2b88023516a992963f33e3730aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228264216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4334e77e616d2395ef8dea81829afc9ef088d8e0488345d6d8c95ff0951292a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:34 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:34 GMT
ARG VERSION=25.12.5.44
# Tue, 17 Feb 2026 20:11:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:03 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:03 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0410a9069e273bb1927901a15bed0cd84781c8b1faa429362db58007eff67f7`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 7.6 MB (7577479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef87aa69603aeaf6806246c274efa79a7b2d47e95439fa1c3df51b392079b1e3`  
		Last Modified: Tue, 17 Feb 2026 20:12:29 GMT  
		Size: 192.4 MB (192431747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9456d54f9a468d2c5b0da72265dfc1700133424a8da87f04cfc20c0ff2bde9d`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad56a8ad46d57e27336b3630afca3cdc6c2872740d43fafbec92015e28519ef`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fb05a1b115ae9167abf8f810742ec51e0ed85efb38d76c80cc76d73b69420b`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eb12c5a4be3e160b1065c9d843fa7bae8deb9ad509de5234a79cc0487e70bc`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e0fc2c2ecc3164944d1a8a97927858425fee2332643b38b1f6ed591a279032`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:43d7abd45abcac286785db9eaaf8996018b890f7f219c6924b10d50d4bc0db45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d28c03cbf285560d96fb640e98022681325cb392470f117ec4787700d91375`

```dockerfile
```

-	Layers:
	-	`sha256:82a818fbed76d98d30db30c165ccb9de457b47aebdb9ae7c2f79e825059df586`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12-jammy`

```console
$ docker pull clickhouse@sha256:2321bd600611139f9bb7265d170ab0bdfad5790b6d5fa0db3ce1476a5c96ec51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0234c146e2ada07696d3b78214b3aa6d7be283ab70e5eb77f4cd3d566b0e6cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246337052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73140c89608e3bbffe181bbfb5e990dd53f526897d3496c0da3758a311a8883a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:53 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:53 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:53 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:53 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:53 GMT
ARG VERSION=25.12.5.44
# Tue, 17 Feb 2026 20:11:53 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:22 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:22 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0265759b2c9568c995905af6c4660fc2821ffbb20f8b491129324ac758b862b7`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 7.6 MB (7598343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feab4d6a05aead20c3dc14e61f73b3e296b703c9765a71e7722494886e4bfe36`  
		Last Modified: Tue, 17 Feb 2026 20:12:54 GMT  
		Size: 208.3 MB (208331298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8b29bd28eec82baaccdb71d33cfbf8ce51b815bfa91f0e50d0f7b58cdee994`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2f47d985a3157d7b6f7f3651533c3da6d9140452099cf3c3fc35051d592b7f`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e96360c2d10134667e54c02a3436bef43841556cd299b11f3694aa7735f7bb`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ef6e8e2d68cd939dd47891dcae496113d2098b78600955e039121f651308a`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a21da2e50caf1756948c84ef75b8e826739b607c64dbf128fbdead8f3b389`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:624ca399136baac93922dd527aca4d8bb02ddde80cf3723fb94f207198686f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c6627c353a22d7bd470c2689c11efce04a7a697ed4c2f30bf769fd14060758`

```dockerfile
```

-	Layers:
	-	`sha256:23ca4ec631b96fa89d3ae9ae56dcf08b8074cb4d5199c96d7187a60246f702c3`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f967a788d5f14f6295a4e8e5d83167c7753b2b88023516a992963f33e3730aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228264216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4334e77e616d2395ef8dea81829afc9ef088d8e0488345d6d8c95ff0951292a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:34 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:34 GMT
ARG VERSION=25.12.5.44
# Tue, 17 Feb 2026 20:11:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:03 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:03 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0410a9069e273bb1927901a15bed0cd84781c8b1faa429362db58007eff67f7`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 7.6 MB (7577479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef87aa69603aeaf6806246c274efa79a7b2d47e95439fa1c3df51b392079b1e3`  
		Last Modified: Tue, 17 Feb 2026 20:12:29 GMT  
		Size: 192.4 MB (192431747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9456d54f9a468d2c5b0da72265dfc1700133424a8da87f04cfc20c0ff2bde9d`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad56a8ad46d57e27336b3630afca3cdc6c2872740d43fafbec92015e28519ef`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fb05a1b115ae9167abf8f810742ec51e0ed85efb38d76c80cc76d73b69420b`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eb12c5a4be3e160b1065c9d843fa7bae8deb9ad509de5234a79cc0487e70bc`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e0fc2c2ecc3164944d1a8a97927858425fee2332643b38b1f6ed591a279032`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:43d7abd45abcac286785db9eaaf8996018b890f7f219c6924b10d50d4bc0db45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d28c03cbf285560d96fb640e98022681325cb392470f117ec4787700d91375`

```dockerfile
```

-	Layers:
	-	`sha256:82a818fbed76d98d30db30c165ccb9de457b47aebdb9ae7c2f79e825059df586`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.5`

```console
$ docker pull clickhouse@sha256:2321bd600611139f9bb7265d170ab0bdfad5790b6d5fa0db3ce1476a5c96ec51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:0234c146e2ada07696d3b78214b3aa6d7be283ab70e5eb77f4cd3d566b0e6cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246337052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73140c89608e3bbffe181bbfb5e990dd53f526897d3496c0da3758a311a8883a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:53 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:53 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:53 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:53 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:53 GMT
ARG VERSION=25.12.5.44
# Tue, 17 Feb 2026 20:11:53 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:22 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:22 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0265759b2c9568c995905af6c4660fc2821ffbb20f8b491129324ac758b862b7`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 7.6 MB (7598343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feab4d6a05aead20c3dc14e61f73b3e296b703c9765a71e7722494886e4bfe36`  
		Last Modified: Tue, 17 Feb 2026 20:12:54 GMT  
		Size: 208.3 MB (208331298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8b29bd28eec82baaccdb71d33cfbf8ce51b815bfa91f0e50d0f7b58cdee994`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2f47d985a3157d7b6f7f3651533c3da6d9140452099cf3c3fc35051d592b7f`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e96360c2d10134667e54c02a3436bef43841556cd299b11f3694aa7735f7bb`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ef6e8e2d68cd939dd47891dcae496113d2098b78600955e039121f651308a`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a21da2e50caf1756948c84ef75b8e826739b607c64dbf128fbdead8f3b389`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:624ca399136baac93922dd527aca4d8bb02ddde80cf3723fb94f207198686f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c6627c353a22d7bd470c2689c11efce04a7a697ed4c2f30bf769fd14060758`

```dockerfile
```

-	Layers:
	-	`sha256:23ca4ec631b96fa89d3ae9ae56dcf08b8074cb4d5199c96d7187a60246f702c3`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f967a788d5f14f6295a4e8e5d83167c7753b2b88023516a992963f33e3730aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228264216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4334e77e616d2395ef8dea81829afc9ef088d8e0488345d6d8c95ff0951292a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:34 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:34 GMT
ARG VERSION=25.12.5.44
# Tue, 17 Feb 2026 20:11:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:03 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:03 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0410a9069e273bb1927901a15bed0cd84781c8b1faa429362db58007eff67f7`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 7.6 MB (7577479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef87aa69603aeaf6806246c274efa79a7b2d47e95439fa1c3df51b392079b1e3`  
		Last Modified: Tue, 17 Feb 2026 20:12:29 GMT  
		Size: 192.4 MB (192431747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9456d54f9a468d2c5b0da72265dfc1700133424a8da87f04cfc20c0ff2bde9d`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad56a8ad46d57e27336b3630afca3cdc6c2872740d43fafbec92015e28519ef`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fb05a1b115ae9167abf8f810742ec51e0ed85efb38d76c80cc76d73b69420b`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eb12c5a4be3e160b1065c9d843fa7bae8deb9ad509de5234a79cc0487e70bc`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e0fc2c2ecc3164944d1a8a97927858425fee2332643b38b1f6ed591a279032`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:43d7abd45abcac286785db9eaaf8996018b890f7f219c6924b10d50d4bc0db45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d28c03cbf285560d96fb640e98022681325cb392470f117ec4787700d91375`

```dockerfile
```

-	Layers:
	-	`sha256:82a818fbed76d98d30db30c165ccb9de457b47aebdb9ae7c2f79e825059df586`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.5-jammy`

```console
$ docker pull clickhouse@sha256:2321bd600611139f9bb7265d170ab0bdfad5790b6d5fa0db3ce1476a5c96ec51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0234c146e2ada07696d3b78214b3aa6d7be283ab70e5eb77f4cd3d566b0e6cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246337052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73140c89608e3bbffe181bbfb5e990dd53f526897d3496c0da3758a311a8883a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:53 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:53 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:53 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:53 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:53 GMT
ARG VERSION=25.12.5.44
# Tue, 17 Feb 2026 20:11:53 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:22 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:22 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0265759b2c9568c995905af6c4660fc2821ffbb20f8b491129324ac758b862b7`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 7.6 MB (7598343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feab4d6a05aead20c3dc14e61f73b3e296b703c9765a71e7722494886e4bfe36`  
		Last Modified: Tue, 17 Feb 2026 20:12:54 GMT  
		Size: 208.3 MB (208331298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8b29bd28eec82baaccdb71d33cfbf8ce51b815bfa91f0e50d0f7b58cdee994`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2f47d985a3157d7b6f7f3651533c3da6d9140452099cf3c3fc35051d592b7f`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e96360c2d10134667e54c02a3436bef43841556cd299b11f3694aa7735f7bb`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ef6e8e2d68cd939dd47891dcae496113d2098b78600955e039121f651308a`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a21da2e50caf1756948c84ef75b8e826739b607c64dbf128fbdead8f3b389`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:624ca399136baac93922dd527aca4d8bb02ddde80cf3723fb94f207198686f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c6627c353a22d7bd470c2689c11efce04a7a697ed4c2f30bf769fd14060758`

```dockerfile
```

-	Layers:
	-	`sha256:23ca4ec631b96fa89d3ae9ae56dcf08b8074cb4d5199c96d7187a60246f702c3`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f967a788d5f14f6295a4e8e5d83167c7753b2b88023516a992963f33e3730aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228264216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4334e77e616d2395ef8dea81829afc9ef088d8e0488345d6d8c95ff0951292a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:34 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:34 GMT
ARG VERSION=25.12.5.44
# Tue, 17 Feb 2026 20:11:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:03 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:03 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0410a9069e273bb1927901a15bed0cd84781c8b1faa429362db58007eff67f7`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 7.6 MB (7577479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef87aa69603aeaf6806246c274efa79a7b2d47e95439fa1c3df51b392079b1e3`  
		Last Modified: Tue, 17 Feb 2026 20:12:29 GMT  
		Size: 192.4 MB (192431747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9456d54f9a468d2c5b0da72265dfc1700133424a8da87f04cfc20c0ff2bde9d`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad56a8ad46d57e27336b3630afca3cdc6c2872740d43fafbec92015e28519ef`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fb05a1b115ae9167abf8f810742ec51e0ed85efb38d76c80cc76d73b69420b`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eb12c5a4be3e160b1065c9d843fa7bae8deb9ad509de5234a79cc0487e70bc`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e0fc2c2ecc3164944d1a8a97927858425fee2332643b38b1f6ed591a279032`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:43d7abd45abcac286785db9eaaf8996018b890f7f219c6924b10d50d4bc0db45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d28c03cbf285560d96fb640e98022681325cb392470f117ec4787700d91375`

```dockerfile
```

-	Layers:
	-	`sha256:82a818fbed76d98d30db30c165ccb9de457b47aebdb9ae7c2f79e825059df586`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.5.44`

```console
$ docker pull clickhouse@sha256:2321bd600611139f9bb7265d170ab0bdfad5790b6d5fa0db3ce1476a5c96ec51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.5.44` - linux; amd64

```console
$ docker pull clickhouse@sha256:0234c146e2ada07696d3b78214b3aa6d7be283ab70e5eb77f4cd3d566b0e6cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246337052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73140c89608e3bbffe181bbfb5e990dd53f526897d3496c0da3758a311a8883a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:53 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:53 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:53 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:53 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:53 GMT
ARG VERSION=25.12.5.44
# Tue, 17 Feb 2026 20:11:53 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:22 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:22 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0265759b2c9568c995905af6c4660fc2821ffbb20f8b491129324ac758b862b7`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 7.6 MB (7598343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feab4d6a05aead20c3dc14e61f73b3e296b703c9765a71e7722494886e4bfe36`  
		Last Modified: Tue, 17 Feb 2026 20:12:54 GMT  
		Size: 208.3 MB (208331298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8b29bd28eec82baaccdb71d33cfbf8ce51b815bfa91f0e50d0f7b58cdee994`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2f47d985a3157d7b6f7f3651533c3da6d9140452099cf3c3fc35051d592b7f`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e96360c2d10134667e54c02a3436bef43841556cd299b11f3694aa7735f7bb`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ef6e8e2d68cd939dd47891dcae496113d2098b78600955e039121f651308a`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a21da2e50caf1756948c84ef75b8e826739b607c64dbf128fbdead8f3b389`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.5.44` - unknown; unknown

```console
$ docker pull clickhouse@sha256:624ca399136baac93922dd527aca4d8bb02ddde80cf3723fb94f207198686f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c6627c353a22d7bd470c2689c11efce04a7a697ed4c2f30bf769fd14060758`

```dockerfile
```

-	Layers:
	-	`sha256:23ca4ec631b96fa89d3ae9ae56dcf08b8074cb4d5199c96d7187a60246f702c3`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.5.44` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f967a788d5f14f6295a4e8e5d83167c7753b2b88023516a992963f33e3730aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228264216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4334e77e616d2395ef8dea81829afc9ef088d8e0488345d6d8c95ff0951292a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:34 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:34 GMT
ARG VERSION=25.12.5.44
# Tue, 17 Feb 2026 20:11:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:03 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:03 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0410a9069e273bb1927901a15bed0cd84781c8b1faa429362db58007eff67f7`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 7.6 MB (7577479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef87aa69603aeaf6806246c274efa79a7b2d47e95439fa1c3df51b392079b1e3`  
		Last Modified: Tue, 17 Feb 2026 20:12:29 GMT  
		Size: 192.4 MB (192431747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9456d54f9a468d2c5b0da72265dfc1700133424a8da87f04cfc20c0ff2bde9d`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad56a8ad46d57e27336b3630afca3cdc6c2872740d43fafbec92015e28519ef`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fb05a1b115ae9167abf8f810742ec51e0ed85efb38d76c80cc76d73b69420b`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eb12c5a4be3e160b1065c9d843fa7bae8deb9ad509de5234a79cc0487e70bc`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e0fc2c2ecc3164944d1a8a97927858425fee2332643b38b1f6ed591a279032`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.5.44` - unknown; unknown

```console
$ docker pull clickhouse@sha256:43d7abd45abcac286785db9eaaf8996018b890f7f219c6924b10d50d4bc0db45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d28c03cbf285560d96fb640e98022681325cb392470f117ec4787700d91375`

```dockerfile
```

-	Layers:
	-	`sha256:82a818fbed76d98d30db30c165ccb9de457b47aebdb9ae7c2f79e825059df586`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.5.44-jammy`

```console
$ docker pull clickhouse@sha256:2321bd600611139f9bb7265d170ab0bdfad5790b6d5fa0db3ce1476a5c96ec51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.5.44-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0234c146e2ada07696d3b78214b3aa6d7be283ab70e5eb77f4cd3d566b0e6cd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246337052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73140c89608e3bbffe181bbfb5e990dd53f526897d3496c0da3758a311a8883a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:53 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:53 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:53 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:53 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:53 GMT
ARG VERSION=25.12.5.44
# Tue, 17 Feb 2026 20:11:53 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:22 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:22 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0265759b2c9568c995905af6c4660fc2821ffbb20f8b491129324ac758b862b7`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 7.6 MB (7598343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feab4d6a05aead20c3dc14e61f73b3e296b703c9765a71e7722494886e4bfe36`  
		Last Modified: Tue, 17 Feb 2026 20:12:54 GMT  
		Size: 208.3 MB (208331298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8b29bd28eec82baaccdb71d33cfbf8ce51b815bfa91f0e50d0f7b58cdee994`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2f47d985a3157d7b6f7f3651533c3da6d9140452099cf3c3fc35051d592b7f`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e96360c2d10134667e54c02a3436bef43841556cd299b11f3694aa7735f7bb`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d89ef6e8e2d68cd939dd47891dcae496113d2098b78600955e039121f651308a`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529a21da2e50caf1756948c84ef75b8e826739b607c64dbf128fbdead8f3b389`  
		Last Modified: Tue, 17 Feb 2026 20:12:50 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.5.44-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:624ca399136baac93922dd527aca4d8bb02ddde80cf3723fb94f207198686f69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21c6627c353a22d7bd470c2689c11efce04a7a697ed4c2f30bf769fd14060758`

```dockerfile
```

-	Layers:
	-	`sha256:23ca4ec631b96fa89d3ae9ae56dcf08b8074cb4d5199c96d7187a60246f702c3`  
		Last Modified: Tue, 17 Feb 2026 20:12:49 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.5.44-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f967a788d5f14f6295a4e8e5d83167c7753b2b88023516a992963f33e3730aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228264216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4334e77e616d2395ef8dea81829afc9ef088d8e0488345d6d8c95ff0951292a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:34 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:34 GMT
ARG VERSION=25.12.5.44
# Tue, 17 Feb 2026 20:11:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:03 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:03 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0410a9069e273bb1927901a15bed0cd84781c8b1faa429362db58007eff67f7`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 7.6 MB (7577479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef87aa69603aeaf6806246c274efa79a7b2d47e95439fa1c3df51b392079b1e3`  
		Last Modified: Tue, 17 Feb 2026 20:12:29 GMT  
		Size: 192.4 MB (192431747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9456d54f9a468d2c5b0da72265dfc1700133424a8da87f04cfc20c0ff2bde9d`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad56a8ad46d57e27336b3630afca3cdc6c2872740d43fafbec92015e28519ef`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fb05a1b115ae9167abf8f810742ec51e0ed85efb38d76c80cc76d73b69420b`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07eb12c5a4be3e160b1065c9d843fa7bae8deb9ad509de5234a79cc0487e70bc`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e0fc2c2ecc3164944d1a8a97927858425fee2332643b38b1f6ed591a279032`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.5.44-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:43d7abd45abcac286785db9eaaf8996018b890f7f219c6924b10d50d4bc0db45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d28c03cbf285560d96fb640e98022681325cb392470f117ec4787700d91375`

```dockerfile
```

-	Layers:
	-	`sha256:82a818fbed76d98d30db30c165ccb9de457b47aebdb9ae7c2f79e825059df586`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 25.6 KB (25624 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.14` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.14` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14-jammy`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.14-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.14-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14.14`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.14.14` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.14.14` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14.14-jammy`

```console
$ docker pull clickhouse@sha256:a161d2462162002de37ef285f97ee473ff6508e71ed81731086b45058f7971a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.14.14-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:68b993f2d07340a659657c85dbec8c0e6664c4763ed2e16677805ac01eba6c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddae4d17c8b5b9c19686e4b059d576168ca5cfa47e7ac610e39ce0056dfd1005`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:18 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:18 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:18 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:18 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:12:18 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:44 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:44 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:44 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:44 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea5956e9ce06105113f91334938df5dcf525a8bc3df1c2a16f57e7f2b6a425e`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 7.2 MB (7151509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd687d6ec6fb5e767ac2ca0cf6d3411821c2963f0640e0e7316bbb579e892f9c`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 168.8 MB (168777561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbfc1879e0b9308f93961875da0ed4a1eeea8e8338923e92c8fd29dec9372c8`  
		Last Modified: Tue, 17 Feb 2026 20:13:02 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560b24731cae82462de66b7d68ab1508e053d735ee7d2bac36fff6a9289b78f0`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dbbc20ed2fff54fd78c0590eaf506bffd7a5c803469fe9ac05e04dbdb7860d`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8413cb2badc60c87392ed27852cbeb3e4c2f9813d852f8ae754ee0a8ba0426bd`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2059c77eb3baaca966ebdda21ee54d6da774ddde0eb1e45ed10c5ea89e3542`  
		Last Modified: Tue, 17 Feb 2026 20:13:04 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:190da4274705d84510bc8104aaae91dbf618e9cf2060d8d588b9b1df7a1991bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafc7844525af3653222389e37e92e42b166fd754a24836b758e384ab815546d`

```dockerfile
```

-	Layers:
	-	`sha256:efc0464d0f6bea6c6a6592de9a192f7ea548342e2624f968db4bf76d272f23ff`  
		Last Modified: Tue, 17 Feb 2026 20:13:03 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.14.14-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:485453bc6aa4103654609fcce1b5a83f178933e16b3b172b1e12d734a5cbda45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193806497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616e0f6b5e42d7886179a3dfb40e0fd3da2b1eb6b6f1a113cb70ef9ea73ebd66`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:33 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:33 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:33 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:33 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:33 GMT
ARG VERSION=25.3.14.14
# Tue, 17 Feb 2026 20:11:33 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:11:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:00 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:00 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59885813d2f331b43b4d1b4a603417ed9d9a5cbc416424ae6b095157475d29b8`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 7.1 MB (7128067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9daf47d8683bb463fc285f6fa2c0389a2631e55679b3ae463e2ab577942d4883`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 158.4 MB (158423249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a7d7c1ac561fd5f9a2a2d52cd577d5a4947992fe513cb6eb9eb94786fd16de`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac72554f2c42ff26b6ee6b1bb296f8ad25875544d0f7f6a53d3e6c33c2574089`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 865.7 KB (865743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471715e89c512d9a8ae44d90031fe06f801f3aa194634227cdd295803c805172`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88a679bec67c5fc1629125025793f282530a3fbfe4632cc065265a71a0490b2`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3610c5656cde1e3bdb996350e08bcaf439884c976546b048f90e380470c279f1`  
		Last Modified: Tue, 17 Feb 2026 20:12:23 GMT  
		Size: 3.8 KB (3833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c7570325bce91d940a46b84cefce0ee0dcfef171bbdb74f61141cb965f42e73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:907a078740daa561978d8bd3f2180da51d1a7d0ee6e73d20bc77d43d00114e07`

```dockerfile
```

-	Layers:
	-	`sha256:29e9f9a0d1bd0b8f9de203da15c5c54b93f793c82362c853130c14729f32fb1c`  
		Last Modified: Tue, 17 Feb 2026 20:12:22 GMT  
		Size: 25.4 KB (25422 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:cb8ea3c339aa84c1d75e0c9fc08f372e0398576caa3d787e7f27b9bbca483d3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:0ec0e053c41857406923f72d00580eac2b61fe11aff754672a9ed03f172c02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228945044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5381324c8bcc3410608a9c899346d8806971bcef1a1a5fad7b59b6418415de5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:26 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:53 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:53 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dee958d69ceaceb4ea57bc08fb7179f6c7e0987acf3a83c3fb4d05fecc5f2`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 7.6 MB (7598324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258567d60460abdf8fc0d705b07cfb5c2cf9c109302d7d2c766667ce48775f4c`  
		Last Modified: Tue, 17 Feb 2026 20:13:16 GMT  
		Size: 190.9 MB (190939334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88afd8fd9b9d7dc8563b7db8a2a6351683c3b3e457879c7f4c041b98bff53e`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53900b96e71ca59796a1577140c2aea52ebe99495fc78ab718f66f89ce11fda`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306d071c1343d8dc0c6d88a9a96ca5aa60bd057563577ae76fd30fbf89e8a3f`  
		Last Modified: Tue, 17 Feb 2026 20:13:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6fbf6e82586a7efc880a4aa52b6e2c210259ad18c01db546ba7da838bd3af`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9009d2f669d7bd059ba402b69f6770efd463c0a1f88b6c0a81fce2aa343e61b`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f00e22ef556b57f9002953ccb230258a724d206ddecc96ddef872a1715c4cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864971555410cf3c7ecd8e15f929470ad3e6751db3fb535b698bb37a50e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:b03ea5c9cfa2f868003976091441edbc705a684639b36b3607bd13f9e0fa5a85`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2bc2d567de72e07f96d39d437aa8ad8c85de7d62d947633c5197d97d05e3603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a020363e23f68ae53ea85f8d5889d92a049d464d3eac58db615f3903fd82d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:49 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:11:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:18 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:18 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e105b5258b6287684da632f28c009bead56d72476c38c18b71037e43e8e9b7c`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 7.6 MB (7577435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d420eedbfb97f76c475c4139188424ad202fa0e076dcced2c2495768b59ac`  
		Last Modified: Tue, 17 Feb 2026 20:12:41 GMT  
		Size: 178.0 MB (178016046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477e7fcc96d3a9fe18cfd60a3109816b4a377d41bfdb46d3e0a3438fd193976`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a0a0e8730d6ac8153fd30fc3f7dc73e6e5160fa253c8ffa137dbdb06914b4`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55e4b063f018d389136b40b857059bb4e1bb4f5af6046376bb9edfcad0241ff`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac4fd6f889704ea3b167cbbc7b274f8178ae69d00df70debe3e214aa936b13`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96f921752d4141c565ccca7e44ec7c882d09ac1601be61a0997273ce77657c`  
		Last Modified: Tue, 17 Feb 2026 20:12:40 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e40bf21f69748ff21ecb45294a3d5abada6026f07908ff61c72014db1bb06598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a041960efb6f4644dde88a255c026fc5cac64f703efced83f24300b69ce680`

```dockerfile
```

-	Layers:
	-	`sha256:d61611774bdc1996895d1e9b295614f62dae75e1c939a7fb15d6abaa66d5a746`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:cb8ea3c339aa84c1d75e0c9fc08f372e0398576caa3d787e7f27b9bbca483d3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0ec0e053c41857406923f72d00580eac2b61fe11aff754672a9ed03f172c02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228945044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5381324c8bcc3410608a9c899346d8806971bcef1a1a5fad7b59b6418415de5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:26 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:53 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:53 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dee958d69ceaceb4ea57bc08fb7179f6c7e0987acf3a83c3fb4d05fecc5f2`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 7.6 MB (7598324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258567d60460abdf8fc0d705b07cfb5c2cf9c109302d7d2c766667ce48775f4c`  
		Last Modified: Tue, 17 Feb 2026 20:13:16 GMT  
		Size: 190.9 MB (190939334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88afd8fd9b9d7dc8563b7db8a2a6351683c3b3e457879c7f4c041b98bff53e`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53900b96e71ca59796a1577140c2aea52ebe99495fc78ab718f66f89ce11fda`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306d071c1343d8dc0c6d88a9a96ca5aa60bd057563577ae76fd30fbf89e8a3f`  
		Last Modified: Tue, 17 Feb 2026 20:13:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6fbf6e82586a7efc880a4aa52b6e2c210259ad18c01db546ba7da838bd3af`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9009d2f669d7bd059ba402b69f6770efd463c0a1f88b6c0a81fce2aa343e61b`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f00e22ef556b57f9002953ccb230258a724d206ddecc96ddef872a1715c4cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864971555410cf3c7ecd8e15f929470ad3e6751db3fb535b698bb37a50e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:b03ea5c9cfa2f868003976091441edbc705a684639b36b3607bd13f9e0fa5a85`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2bc2d567de72e07f96d39d437aa8ad8c85de7d62d947633c5197d97d05e3603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a020363e23f68ae53ea85f8d5889d92a049d464d3eac58db615f3903fd82d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:49 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:11:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:18 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:18 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e105b5258b6287684da632f28c009bead56d72476c38c18b71037e43e8e9b7c`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 7.6 MB (7577435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d420eedbfb97f76c475c4139188424ad202fa0e076dcced2c2495768b59ac`  
		Last Modified: Tue, 17 Feb 2026 20:12:41 GMT  
		Size: 178.0 MB (178016046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477e7fcc96d3a9fe18cfd60a3109816b4a377d41bfdb46d3e0a3438fd193976`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a0a0e8730d6ac8153fd30fc3f7dc73e6e5160fa253c8ffa137dbdb06914b4`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55e4b063f018d389136b40b857059bb4e1bb4f5af6046376bb9edfcad0241ff`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac4fd6f889704ea3b167cbbc7b274f8178ae69d00df70debe3e214aa936b13`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96f921752d4141c565ccca7e44ec7c882d09ac1601be61a0997273ce77657c`  
		Last Modified: Tue, 17 Feb 2026 20:12:40 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e40bf21f69748ff21ecb45294a3d5abada6026f07908ff61c72014db1bb06598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a041960efb6f4644dde88a255c026fc5cac64f703efced83f24300b69ce680`

```dockerfile
```

-	Layers:
	-	`sha256:d61611774bdc1996895d1e9b295614f62dae75e1c939a7fb15d6abaa66d5a746`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.16`

```console
$ docker pull clickhouse@sha256:cb8ea3c339aa84c1d75e0c9fc08f372e0398576caa3d787e7f27b9bbca483d3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.16` - linux; amd64

```console
$ docker pull clickhouse@sha256:0ec0e053c41857406923f72d00580eac2b61fe11aff754672a9ed03f172c02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228945044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5381324c8bcc3410608a9c899346d8806971bcef1a1a5fad7b59b6418415de5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:26 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:53 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:53 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dee958d69ceaceb4ea57bc08fb7179f6c7e0987acf3a83c3fb4d05fecc5f2`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 7.6 MB (7598324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258567d60460abdf8fc0d705b07cfb5c2cf9c109302d7d2c766667ce48775f4c`  
		Last Modified: Tue, 17 Feb 2026 20:13:16 GMT  
		Size: 190.9 MB (190939334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88afd8fd9b9d7dc8563b7db8a2a6351683c3b3e457879c7f4c041b98bff53e`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53900b96e71ca59796a1577140c2aea52ebe99495fc78ab718f66f89ce11fda`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306d071c1343d8dc0c6d88a9a96ca5aa60bd057563577ae76fd30fbf89e8a3f`  
		Last Modified: Tue, 17 Feb 2026 20:13:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6fbf6e82586a7efc880a4aa52b6e2c210259ad18c01db546ba7da838bd3af`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9009d2f669d7bd059ba402b69f6770efd463c0a1f88b6c0a81fce2aa343e61b`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f00e22ef556b57f9002953ccb230258a724d206ddecc96ddef872a1715c4cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864971555410cf3c7ecd8e15f929470ad3e6751db3fb535b698bb37a50e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:b03ea5c9cfa2f868003976091441edbc705a684639b36b3607bd13f9e0fa5a85`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.16` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2bc2d567de72e07f96d39d437aa8ad8c85de7d62d947633c5197d97d05e3603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a020363e23f68ae53ea85f8d5889d92a049d464d3eac58db615f3903fd82d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:49 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:11:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:18 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:18 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e105b5258b6287684da632f28c009bead56d72476c38c18b71037e43e8e9b7c`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 7.6 MB (7577435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d420eedbfb97f76c475c4139188424ad202fa0e076dcced2c2495768b59ac`  
		Last Modified: Tue, 17 Feb 2026 20:12:41 GMT  
		Size: 178.0 MB (178016046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477e7fcc96d3a9fe18cfd60a3109816b4a377d41bfdb46d3e0a3438fd193976`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a0a0e8730d6ac8153fd30fc3f7dc73e6e5160fa253c8ffa137dbdb06914b4`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55e4b063f018d389136b40b857059bb4e1bb4f5af6046376bb9edfcad0241ff`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac4fd6f889704ea3b167cbbc7b274f8178ae69d00df70debe3e214aa936b13`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96f921752d4141c565ccca7e44ec7c882d09ac1601be61a0997273ce77657c`  
		Last Modified: Tue, 17 Feb 2026 20:12:40 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e40bf21f69748ff21ecb45294a3d5abada6026f07908ff61c72014db1bb06598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a041960efb6f4644dde88a255c026fc5cac64f703efced83f24300b69ce680`

```dockerfile
```

-	Layers:
	-	`sha256:d61611774bdc1996895d1e9b295614f62dae75e1c939a7fb15d6abaa66d5a746`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.16-jammy`

```console
$ docker pull clickhouse@sha256:cb8ea3c339aa84c1d75e0c9fc08f372e0398576caa3d787e7f27b9bbca483d3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.16-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0ec0e053c41857406923f72d00580eac2b61fe11aff754672a9ed03f172c02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228945044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5381324c8bcc3410608a9c899346d8806971bcef1a1a5fad7b59b6418415de5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:26 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:53 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:53 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dee958d69ceaceb4ea57bc08fb7179f6c7e0987acf3a83c3fb4d05fecc5f2`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 7.6 MB (7598324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258567d60460abdf8fc0d705b07cfb5c2cf9c109302d7d2c766667ce48775f4c`  
		Last Modified: Tue, 17 Feb 2026 20:13:16 GMT  
		Size: 190.9 MB (190939334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88afd8fd9b9d7dc8563b7db8a2a6351683c3b3e457879c7f4c041b98bff53e`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53900b96e71ca59796a1577140c2aea52ebe99495fc78ab718f66f89ce11fda`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306d071c1343d8dc0c6d88a9a96ca5aa60bd057563577ae76fd30fbf89e8a3f`  
		Last Modified: Tue, 17 Feb 2026 20:13:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6fbf6e82586a7efc880a4aa52b6e2c210259ad18c01db546ba7da838bd3af`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9009d2f669d7bd059ba402b69f6770efd463c0a1f88b6c0a81fce2aa343e61b`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f00e22ef556b57f9002953ccb230258a724d206ddecc96ddef872a1715c4cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864971555410cf3c7ecd8e15f929470ad3e6751db3fb535b698bb37a50e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:b03ea5c9cfa2f868003976091441edbc705a684639b36b3607bd13f9e0fa5a85`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.16-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2bc2d567de72e07f96d39d437aa8ad8c85de7d62d947633c5197d97d05e3603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a020363e23f68ae53ea85f8d5889d92a049d464d3eac58db615f3903fd82d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:49 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:11:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:18 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:18 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e105b5258b6287684da632f28c009bead56d72476c38c18b71037e43e8e9b7c`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 7.6 MB (7577435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d420eedbfb97f76c475c4139188424ad202fa0e076dcced2c2495768b59ac`  
		Last Modified: Tue, 17 Feb 2026 20:12:41 GMT  
		Size: 178.0 MB (178016046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477e7fcc96d3a9fe18cfd60a3109816b4a377d41bfdb46d3e0a3438fd193976`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a0a0e8730d6ac8153fd30fc3f7dc73e6e5160fa253c8ffa137dbdb06914b4`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55e4b063f018d389136b40b857059bb4e1bb4f5af6046376bb9edfcad0241ff`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac4fd6f889704ea3b167cbbc7b274f8178ae69d00df70debe3e214aa936b13`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96f921752d4141c565ccca7e44ec7c882d09ac1601be61a0997273ce77657c`  
		Last Modified: Tue, 17 Feb 2026 20:12:40 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e40bf21f69748ff21ecb45294a3d5abada6026f07908ff61c72014db1bb06598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a041960efb6f4644dde88a255c026fc5cac64f703efced83f24300b69ce680`

```dockerfile
```

-	Layers:
	-	`sha256:d61611774bdc1996895d1e9b295614f62dae75e1c939a7fb15d6abaa66d5a746`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.16.34`

```console
$ docker pull clickhouse@sha256:cb8ea3c339aa84c1d75e0c9fc08f372e0398576caa3d787e7f27b9bbca483d3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.16.34` - linux; amd64

```console
$ docker pull clickhouse@sha256:0ec0e053c41857406923f72d00580eac2b61fe11aff754672a9ed03f172c02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228945044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5381324c8bcc3410608a9c899346d8806971bcef1a1a5fad7b59b6418415de5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:26 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:53 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:53 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dee958d69ceaceb4ea57bc08fb7179f6c7e0987acf3a83c3fb4d05fecc5f2`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 7.6 MB (7598324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258567d60460abdf8fc0d705b07cfb5c2cf9c109302d7d2c766667ce48775f4c`  
		Last Modified: Tue, 17 Feb 2026 20:13:16 GMT  
		Size: 190.9 MB (190939334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88afd8fd9b9d7dc8563b7db8a2a6351683c3b3e457879c7f4c041b98bff53e`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53900b96e71ca59796a1577140c2aea52ebe99495fc78ab718f66f89ce11fda`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306d071c1343d8dc0c6d88a9a96ca5aa60bd057563577ae76fd30fbf89e8a3f`  
		Last Modified: Tue, 17 Feb 2026 20:13:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6fbf6e82586a7efc880a4aa52b6e2c210259ad18c01db546ba7da838bd3af`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9009d2f669d7bd059ba402b69f6770efd463c0a1f88b6c0a81fce2aa343e61b`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16.34` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f00e22ef556b57f9002953ccb230258a724d206ddecc96ddef872a1715c4cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864971555410cf3c7ecd8e15f929470ad3e6751db3fb535b698bb37a50e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:b03ea5c9cfa2f868003976091441edbc705a684639b36b3607bd13f9e0fa5a85`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.16.34` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2bc2d567de72e07f96d39d437aa8ad8c85de7d62d947633c5197d97d05e3603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a020363e23f68ae53ea85f8d5889d92a049d464d3eac58db615f3903fd82d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:49 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:11:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:18 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:18 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e105b5258b6287684da632f28c009bead56d72476c38c18b71037e43e8e9b7c`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 7.6 MB (7577435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d420eedbfb97f76c475c4139188424ad202fa0e076dcced2c2495768b59ac`  
		Last Modified: Tue, 17 Feb 2026 20:12:41 GMT  
		Size: 178.0 MB (178016046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477e7fcc96d3a9fe18cfd60a3109816b4a377d41bfdb46d3e0a3438fd193976`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a0a0e8730d6ac8153fd30fc3f7dc73e6e5160fa253c8ffa137dbdb06914b4`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55e4b063f018d389136b40b857059bb4e1bb4f5af6046376bb9edfcad0241ff`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac4fd6f889704ea3b167cbbc7b274f8178ae69d00df70debe3e214aa936b13`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96f921752d4141c565ccca7e44ec7c882d09ac1601be61a0997273ce77657c`  
		Last Modified: Tue, 17 Feb 2026 20:12:40 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16.34` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e40bf21f69748ff21ecb45294a3d5abada6026f07908ff61c72014db1bb06598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a041960efb6f4644dde88a255c026fc5cac64f703efced83f24300b69ce680`

```dockerfile
```

-	Layers:
	-	`sha256:d61611774bdc1996895d1e9b295614f62dae75e1c939a7fb15d6abaa66d5a746`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.16.34-jammy`

```console
$ docker pull clickhouse@sha256:cb8ea3c339aa84c1d75e0c9fc08f372e0398576caa3d787e7f27b9bbca483d3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.16.34-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0ec0e053c41857406923f72d00580eac2b61fe11aff754672a9ed03f172c02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228945044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5381324c8bcc3410608a9c899346d8806971bcef1a1a5fad7b59b6418415de5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:26 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:53 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:53 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dee958d69ceaceb4ea57bc08fb7179f6c7e0987acf3a83c3fb4d05fecc5f2`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 7.6 MB (7598324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258567d60460abdf8fc0d705b07cfb5c2cf9c109302d7d2c766667ce48775f4c`  
		Last Modified: Tue, 17 Feb 2026 20:13:16 GMT  
		Size: 190.9 MB (190939334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88afd8fd9b9d7dc8563b7db8a2a6351683c3b3e457879c7f4c041b98bff53e`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53900b96e71ca59796a1577140c2aea52ebe99495fc78ab718f66f89ce11fda`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306d071c1343d8dc0c6d88a9a96ca5aa60bd057563577ae76fd30fbf89e8a3f`  
		Last Modified: Tue, 17 Feb 2026 20:13:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6fbf6e82586a7efc880a4aa52b6e2c210259ad18c01db546ba7da838bd3af`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9009d2f669d7bd059ba402b69f6770efd463c0a1f88b6c0a81fce2aa343e61b`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16.34-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f00e22ef556b57f9002953ccb230258a724d206ddecc96ddef872a1715c4cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864971555410cf3c7ecd8e15f929470ad3e6751db3fb535b698bb37a50e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:b03ea5c9cfa2f868003976091441edbc705a684639b36b3607bd13f9e0fa5a85`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.16.34-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2bc2d567de72e07f96d39d437aa8ad8c85de7d62d947633c5197d97d05e3603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a020363e23f68ae53ea85f8d5889d92a049d464d3eac58db615f3903fd82d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:49 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:11:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:18 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:18 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e105b5258b6287684da632f28c009bead56d72476c38c18b71037e43e8e9b7c`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 7.6 MB (7577435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d420eedbfb97f76c475c4139188424ad202fa0e076dcced2c2495768b59ac`  
		Last Modified: Tue, 17 Feb 2026 20:12:41 GMT  
		Size: 178.0 MB (178016046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477e7fcc96d3a9fe18cfd60a3109816b4a377d41bfdb46d3e0a3438fd193976`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a0a0e8730d6ac8153fd30fc3f7dc73e6e5160fa253c8ffa137dbdb06914b4`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55e4b063f018d389136b40b857059bb4e1bb4f5af6046376bb9edfcad0241ff`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac4fd6f889704ea3b167cbbc7b274f8178ae69d00df70debe3e214aa936b13`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96f921752d4141c565ccca7e44ec7c882d09ac1601be61a0997273ce77657c`  
		Last Modified: Tue, 17 Feb 2026 20:12:40 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16.34-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e40bf21f69748ff21ecb45294a3d5abada6026f07908ff61c72014db1bb06598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a041960efb6f4644dde88a255c026fc5cac64f703efced83f24300b69ce680`

```dockerfile
```

-	Layers:
	-	`sha256:d61611774bdc1996895d1e9b295614f62dae75e1c939a7fb15d6abaa66d5a746`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1`

```console
$ docker pull clickhouse@sha256:33b3d506101eacd5c956aa2a9ca699142b4e416b2a323b8e08b6e7ff4baf5ee4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:9ccf2f724082e15005463983b21ce300e6a37e42d2f9247160a8ea311121245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246000376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e71b825ab5bf4b21f792087ba4c659d068b9241e7e6df43f6ae34221e7ba315`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:51 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:51 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:51 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:51 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:51 GMT
ARG VERSION=26.1.2.11
# Tue, 17 Feb 2026 20:11:51 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:43 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:43 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:43 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358aea4f7c076ba368df1282f1f04f07c8f663f737f5709a4542bdb92ab78545`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 7.6 MB (7598370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853ad1574df53d6e1debfe0cdd5b1884da948333a4ee32afacdca15a83802c94`  
		Last Modified: Tue, 17 Feb 2026 20:13:09 GMT  
		Size: 208.0 MB (207994605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72fb4592f19d88bdfb886f8987bf22d20fabc42f5b15fc46a8037623150c48b`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f0ee55081f6d58efcf2c52f7819024f89c529ead6333e84b8ca4e1f7fe50f6`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abc4fa545535bc3ebf24fa18a9f566b2b58666110279d7868198317cbba2413`  
		Last Modified: Tue, 17 Feb 2026 20:13:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e04a537211258d7fdbf4b41a0631019dfc16446fbb924dcba78ab1edc47f12`  
		Last Modified: Tue, 17 Feb 2026 20:13:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620b9b548b40539a30fdfcbb5abb283fa2243b1c67b3044c0da351d9980fd2c4`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:691c518013c16f60737305161ee387f1e0ddf7190ff55138e2fb8ce6eb3dc1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8069f56463c7727c5f72ca9901b0bde49672b701050b69fd98a80b4ae6a10e49`

```dockerfile
```

-	Layers:
	-	`sha256:57de74d915f05b81ede453b0a141e47216675a9e6aecb68e83eb64dc181063dd`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:021c8b9d467466063b9d08ca416183864bbd008eea83b5f9109200217c56be0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228204383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd534b39c71930ad029134007379854cd9bb4a3e70f9e6b08542d3bf14fa4b51`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:35 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:35 GMT
ARG VERSION=26.1.2.11
# Tue, 17 Feb 2026 20:11:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:02 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:03 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e437fc694ccf6b344853b723b3019089894d4f5302a098744f989b425e77ea`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 7.6 MB (7577401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a28268f9e3b3b43fe763fd13b19e423f9bedc3d7bb23f576b3b1609a33bbcfe`  
		Last Modified: Tue, 17 Feb 2026 20:12:30 GMT  
		Size: 192.4 MB (192371994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9456d54f9a468d2c5b0da72265dfc1700133424a8da87f04cfc20c0ff2bde9d`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94f07ea74de42bad18cfe1050a598e10af6c3c700bd16d614bb4e7cfc0a36c3`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff6e3401174e3e4d32e98be9dea020d8cf66ab1dde840a7fbd6d00ae9ff47b`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c664f3d09f0a4e9932acbce930b07fbcad9c594a0b01381e0e1863caea9198a9`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a2fe54066d9fe1a6def590773e9783ecf5015f072e1acd73d6077b89bfc62f`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d5da5276f34eba3d43021bce1ec8da657af3db13069ff368fe7d9554a607db65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207156ff3a9f6bfca6a94cc3c9d9d0664f9ede755b5f126f040d67dc48414ea6`

```dockerfile
```

-	Layers:
	-	`sha256:ab55c6ddecb392ca89035cd2a8f67faad7bf8c562cf6783a36bfb51b3202c7f7`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1-jammy`

```console
$ docker pull clickhouse@sha256:33b3d506101eacd5c956aa2a9ca699142b4e416b2a323b8e08b6e7ff4baf5ee4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:9ccf2f724082e15005463983b21ce300e6a37e42d2f9247160a8ea311121245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246000376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e71b825ab5bf4b21f792087ba4c659d068b9241e7e6df43f6ae34221e7ba315`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:51 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:51 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:51 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:51 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:51 GMT
ARG VERSION=26.1.2.11
# Tue, 17 Feb 2026 20:11:51 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:43 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:43 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:43 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358aea4f7c076ba368df1282f1f04f07c8f663f737f5709a4542bdb92ab78545`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 7.6 MB (7598370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853ad1574df53d6e1debfe0cdd5b1884da948333a4ee32afacdca15a83802c94`  
		Last Modified: Tue, 17 Feb 2026 20:13:09 GMT  
		Size: 208.0 MB (207994605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72fb4592f19d88bdfb886f8987bf22d20fabc42f5b15fc46a8037623150c48b`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f0ee55081f6d58efcf2c52f7819024f89c529ead6333e84b8ca4e1f7fe50f6`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abc4fa545535bc3ebf24fa18a9f566b2b58666110279d7868198317cbba2413`  
		Last Modified: Tue, 17 Feb 2026 20:13:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e04a537211258d7fdbf4b41a0631019dfc16446fbb924dcba78ab1edc47f12`  
		Last Modified: Tue, 17 Feb 2026 20:13:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620b9b548b40539a30fdfcbb5abb283fa2243b1c67b3044c0da351d9980fd2c4`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:691c518013c16f60737305161ee387f1e0ddf7190ff55138e2fb8ce6eb3dc1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8069f56463c7727c5f72ca9901b0bde49672b701050b69fd98a80b4ae6a10e49`

```dockerfile
```

-	Layers:
	-	`sha256:57de74d915f05b81ede453b0a141e47216675a9e6aecb68e83eb64dc181063dd`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:021c8b9d467466063b9d08ca416183864bbd008eea83b5f9109200217c56be0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228204383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd534b39c71930ad029134007379854cd9bb4a3e70f9e6b08542d3bf14fa4b51`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:35 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:35 GMT
ARG VERSION=26.1.2.11
# Tue, 17 Feb 2026 20:11:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:02 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:03 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e437fc694ccf6b344853b723b3019089894d4f5302a098744f989b425e77ea`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 7.6 MB (7577401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a28268f9e3b3b43fe763fd13b19e423f9bedc3d7bb23f576b3b1609a33bbcfe`  
		Last Modified: Tue, 17 Feb 2026 20:12:30 GMT  
		Size: 192.4 MB (192371994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9456d54f9a468d2c5b0da72265dfc1700133424a8da87f04cfc20c0ff2bde9d`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94f07ea74de42bad18cfe1050a598e10af6c3c700bd16d614bb4e7cfc0a36c3`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff6e3401174e3e4d32e98be9dea020d8cf66ab1dde840a7fbd6d00ae9ff47b`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c664f3d09f0a4e9932acbce930b07fbcad9c594a0b01381e0e1863caea9198a9`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a2fe54066d9fe1a6def590773e9783ecf5015f072e1acd73d6077b89bfc62f`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d5da5276f34eba3d43021bce1ec8da657af3db13069ff368fe7d9554a607db65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207156ff3a9f6bfca6a94cc3c9d9d0664f9ede755b5f126f040d67dc48414ea6`

```dockerfile
```

-	Layers:
	-	`sha256:ab55c6ddecb392ca89035cd2a8f67faad7bf8c562cf6783a36bfb51b3202c7f7`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.2`

```console
$ docker pull clickhouse@sha256:33b3d506101eacd5c956aa2a9ca699142b4e416b2a323b8e08b6e7ff4baf5ee4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:9ccf2f724082e15005463983b21ce300e6a37e42d2f9247160a8ea311121245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246000376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e71b825ab5bf4b21f792087ba4c659d068b9241e7e6df43f6ae34221e7ba315`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:51 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:51 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:51 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:51 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:51 GMT
ARG VERSION=26.1.2.11
# Tue, 17 Feb 2026 20:11:51 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:43 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:43 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:43 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358aea4f7c076ba368df1282f1f04f07c8f663f737f5709a4542bdb92ab78545`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 7.6 MB (7598370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853ad1574df53d6e1debfe0cdd5b1884da948333a4ee32afacdca15a83802c94`  
		Last Modified: Tue, 17 Feb 2026 20:13:09 GMT  
		Size: 208.0 MB (207994605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72fb4592f19d88bdfb886f8987bf22d20fabc42f5b15fc46a8037623150c48b`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f0ee55081f6d58efcf2c52f7819024f89c529ead6333e84b8ca4e1f7fe50f6`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abc4fa545535bc3ebf24fa18a9f566b2b58666110279d7868198317cbba2413`  
		Last Modified: Tue, 17 Feb 2026 20:13:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e04a537211258d7fdbf4b41a0631019dfc16446fbb924dcba78ab1edc47f12`  
		Last Modified: Tue, 17 Feb 2026 20:13:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620b9b548b40539a30fdfcbb5abb283fa2243b1c67b3044c0da351d9980fd2c4`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:691c518013c16f60737305161ee387f1e0ddf7190ff55138e2fb8ce6eb3dc1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8069f56463c7727c5f72ca9901b0bde49672b701050b69fd98a80b4ae6a10e49`

```dockerfile
```

-	Layers:
	-	`sha256:57de74d915f05b81ede453b0a141e47216675a9e6aecb68e83eb64dc181063dd`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:021c8b9d467466063b9d08ca416183864bbd008eea83b5f9109200217c56be0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228204383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd534b39c71930ad029134007379854cd9bb4a3e70f9e6b08542d3bf14fa4b51`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:35 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:35 GMT
ARG VERSION=26.1.2.11
# Tue, 17 Feb 2026 20:11:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:02 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:03 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e437fc694ccf6b344853b723b3019089894d4f5302a098744f989b425e77ea`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 7.6 MB (7577401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a28268f9e3b3b43fe763fd13b19e423f9bedc3d7bb23f576b3b1609a33bbcfe`  
		Last Modified: Tue, 17 Feb 2026 20:12:30 GMT  
		Size: 192.4 MB (192371994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9456d54f9a468d2c5b0da72265dfc1700133424a8da87f04cfc20c0ff2bde9d`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94f07ea74de42bad18cfe1050a598e10af6c3c700bd16d614bb4e7cfc0a36c3`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff6e3401174e3e4d32e98be9dea020d8cf66ab1dde840a7fbd6d00ae9ff47b`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c664f3d09f0a4e9932acbce930b07fbcad9c594a0b01381e0e1863caea9198a9`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a2fe54066d9fe1a6def590773e9783ecf5015f072e1acd73d6077b89bfc62f`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d5da5276f34eba3d43021bce1ec8da657af3db13069ff368fe7d9554a607db65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207156ff3a9f6bfca6a94cc3c9d9d0664f9ede755b5f126f040d67dc48414ea6`

```dockerfile
```

-	Layers:
	-	`sha256:ab55c6ddecb392ca89035cd2a8f67faad7bf8c562cf6783a36bfb51b3202c7f7`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.2-jammy`

```console
$ docker pull clickhouse@sha256:33b3d506101eacd5c956aa2a9ca699142b4e416b2a323b8e08b6e7ff4baf5ee4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:9ccf2f724082e15005463983b21ce300e6a37e42d2f9247160a8ea311121245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246000376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e71b825ab5bf4b21f792087ba4c659d068b9241e7e6df43f6ae34221e7ba315`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:51 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:51 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:51 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:51 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:51 GMT
ARG VERSION=26.1.2.11
# Tue, 17 Feb 2026 20:11:51 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:43 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:43 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:43 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358aea4f7c076ba368df1282f1f04f07c8f663f737f5709a4542bdb92ab78545`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 7.6 MB (7598370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853ad1574df53d6e1debfe0cdd5b1884da948333a4ee32afacdca15a83802c94`  
		Last Modified: Tue, 17 Feb 2026 20:13:09 GMT  
		Size: 208.0 MB (207994605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72fb4592f19d88bdfb886f8987bf22d20fabc42f5b15fc46a8037623150c48b`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f0ee55081f6d58efcf2c52f7819024f89c529ead6333e84b8ca4e1f7fe50f6`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abc4fa545535bc3ebf24fa18a9f566b2b58666110279d7868198317cbba2413`  
		Last Modified: Tue, 17 Feb 2026 20:13:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e04a537211258d7fdbf4b41a0631019dfc16446fbb924dcba78ab1edc47f12`  
		Last Modified: Tue, 17 Feb 2026 20:13:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620b9b548b40539a30fdfcbb5abb283fa2243b1c67b3044c0da351d9980fd2c4`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:691c518013c16f60737305161ee387f1e0ddf7190ff55138e2fb8ce6eb3dc1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8069f56463c7727c5f72ca9901b0bde49672b701050b69fd98a80b4ae6a10e49`

```dockerfile
```

-	Layers:
	-	`sha256:57de74d915f05b81ede453b0a141e47216675a9e6aecb68e83eb64dc181063dd`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:021c8b9d467466063b9d08ca416183864bbd008eea83b5f9109200217c56be0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228204383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd534b39c71930ad029134007379854cd9bb4a3e70f9e6b08542d3bf14fa4b51`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:35 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:35 GMT
ARG VERSION=26.1.2.11
# Tue, 17 Feb 2026 20:11:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:02 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:03 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e437fc694ccf6b344853b723b3019089894d4f5302a098744f989b425e77ea`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 7.6 MB (7577401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a28268f9e3b3b43fe763fd13b19e423f9bedc3d7bb23f576b3b1609a33bbcfe`  
		Last Modified: Tue, 17 Feb 2026 20:12:30 GMT  
		Size: 192.4 MB (192371994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9456d54f9a468d2c5b0da72265dfc1700133424a8da87f04cfc20c0ff2bde9d`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94f07ea74de42bad18cfe1050a598e10af6c3c700bd16d614bb4e7cfc0a36c3`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff6e3401174e3e4d32e98be9dea020d8cf66ab1dde840a7fbd6d00ae9ff47b`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c664f3d09f0a4e9932acbce930b07fbcad9c594a0b01381e0e1863caea9198a9`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a2fe54066d9fe1a6def590773e9783ecf5015f072e1acd73d6077b89bfc62f`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d5da5276f34eba3d43021bce1ec8da657af3db13069ff368fe7d9554a607db65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207156ff3a9f6bfca6a94cc3c9d9d0664f9ede755b5f126f040d67dc48414ea6`

```dockerfile
```

-	Layers:
	-	`sha256:ab55c6ddecb392ca89035cd2a8f67faad7bf8c562cf6783a36bfb51b3202c7f7`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.2.11`

```console
$ docker pull clickhouse@sha256:33b3d506101eacd5c956aa2a9ca699142b4e416b2a323b8e08b6e7ff4baf5ee4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.2.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:9ccf2f724082e15005463983b21ce300e6a37e42d2f9247160a8ea311121245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246000376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e71b825ab5bf4b21f792087ba4c659d068b9241e7e6df43f6ae34221e7ba315`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:51 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:51 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:51 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:51 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:51 GMT
ARG VERSION=26.1.2.11
# Tue, 17 Feb 2026 20:11:51 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:43 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:43 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:43 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358aea4f7c076ba368df1282f1f04f07c8f663f737f5709a4542bdb92ab78545`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 7.6 MB (7598370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853ad1574df53d6e1debfe0cdd5b1884da948333a4ee32afacdca15a83802c94`  
		Last Modified: Tue, 17 Feb 2026 20:13:09 GMT  
		Size: 208.0 MB (207994605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72fb4592f19d88bdfb886f8987bf22d20fabc42f5b15fc46a8037623150c48b`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f0ee55081f6d58efcf2c52f7819024f89c529ead6333e84b8ca4e1f7fe50f6`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abc4fa545535bc3ebf24fa18a9f566b2b58666110279d7868198317cbba2413`  
		Last Modified: Tue, 17 Feb 2026 20:13:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e04a537211258d7fdbf4b41a0631019dfc16446fbb924dcba78ab1edc47f12`  
		Last Modified: Tue, 17 Feb 2026 20:13:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620b9b548b40539a30fdfcbb5abb283fa2243b1c67b3044c0da351d9980fd2c4`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.2.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:691c518013c16f60737305161ee387f1e0ddf7190ff55138e2fb8ce6eb3dc1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8069f56463c7727c5f72ca9901b0bde49672b701050b69fd98a80b4ae6a10e49`

```dockerfile
```

-	Layers:
	-	`sha256:57de74d915f05b81ede453b0a141e47216675a9e6aecb68e83eb64dc181063dd`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.2.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:021c8b9d467466063b9d08ca416183864bbd008eea83b5f9109200217c56be0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228204383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd534b39c71930ad029134007379854cd9bb4a3e70f9e6b08542d3bf14fa4b51`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:35 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:35 GMT
ARG VERSION=26.1.2.11
# Tue, 17 Feb 2026 20:11:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:02 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:03 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e437fc694ccf6b344853b723b3019089894d4f5302a098744f989b425e77ea`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 7.6 MB (7577401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a28268f9e3b3b43fe763fd13b19e423f9bedc3d7bb23f576b3b1609a33bbcfe`  
		Last Modified: Tue, 17 Feb 2026 20:12:30 GMT  
		Size: 192.4 MB (192371994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9456d54f9a468d2c5b0da72265dfc1700133424a8da87f04cfc20c0ff2bde9d`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94f07ea74de42bad18cfe1050a598e10af6c3c700bd16d614bb4e7cfc0a36c3`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff6e3401174e3e4d32e98be9dea020d8cf66ab1dde840a7fbd6d00ae9ff47b`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c664f3d09f0a4e9932acbce930b07fbcad9c594a0b01381e0e1863caea9198a9`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a2fe54066d9fe1a6def590773e9783ecf5015f072e1acd73d6077b89bfc62f`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.2.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d5da5276f34eba3d43021bce1ec8da657af3db13069ff368fe7d9554a607db65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207156ff3a9f6bfca6a94cc3c9d9d0664f9ede755b5f126f040d67dc48414ea6`

```dockerfile
```

-	Layers:
	-	`sha256:ab55c6ddecb392ca89035cd2a8f67faad7bf8c562cf6783a36bfb51b3202c7f7`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.2.11-jammy`

```console
$ docker pull clickhouse@sha256:33b3d506101eacd5c956aa2a9ca699142b4e416b2a323b8e08b6e7ff4baf5ee4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.2.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:9ccf2f724082e15005463983b21ce300e6a37e42d2f9247160a8ea311121245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246000376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e71b825ab5bf4b21f792087ba4c659d068b9241e7e6df43f6ae34221e7ba315`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:51 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:51 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:51 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:51 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:51 GMT
ARG VERSION=26.1.2.11
# Tue, 17 Feb 2026 20:11:51 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:43 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:43 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:43 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358aea4f7c076ba368df1282f1f04f07c8f663f737f5709a4542bdb92ab78545`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 7.6 MB (7598370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853ad1574df53d6e1debfe0cdd5b1884da948333a4ee32afacdca15a83802c94`  
		Last Modified: Tue, 17 Feb 2026 20:13:09 GMT  
		Size: 208.0 MB (207994605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72fb4592f19d88bdfb886f8987bf22d20fabc42f5b15fc46a8037623150c48b`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f0ee55081f6d58efcf2c52f7819024f89c529ead6333e84b8ca4e1f7fe50f6`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abc4fa545535bc3ebf24fa18a9f566b2b58666110279d7868198317cbba2413`  
		Last Modified: Tue, 17 Feb 2026 20:13:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e04a537211258d7fdbf4b41a0631019dfc16446fbb924dcba78ab1edc47f12`  
		Last Modified: Tue, 17 Feb 2026 20:13:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620b9b548b40539a30fdfcbb5abb283fa2243b1c67b3044c0da351d9980fd2c4`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.2.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:691c518013c16f60737305161ee387f1e0ddf7190ff55138e2fb8ce6eb3dc1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8069f56463c7727c5f72ca9901b0bde49672b701050b69fd98a80b4ae6a10e49`

```dockerfile
```

-	Layers:
	-	`sha256:57de74d915f05b81ede453b0a141e47216675a9e6aecb68e83eb64dc181063dd`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.2.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:021c8b9d467466063b9d08ca416183864bbd008eea83b5f9109200217c56be0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228204383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd534b39c71930ad029134007379854cd9bb4a3e70f9e6b08542d3bf14fa4b51`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:35 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:35 GMT
ARG VERSION=26.1.2.11
# Tue, 17 Feb 2026 20:11:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:02 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:03 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e437fc694ccf6b344853b723b3019089894d4f5302a098744f989b425e77ea`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 7.6 MB (7577401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a28268f9e3b3b43fe763fd13b19e423f9bedc3d7bb23f576b3b1609a33bbcfe`  
		Last Modified: Tue, 17 Feb 2026 20:12:30 GMT  
		Size: 192.4 MB (192371994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9456d54f9a468d2c5b0da72265dfc1700133424a8da87f04cfc20c0ff2bde9d`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94f07ea74de42bad18cfe1050a598e10af6c3c700bd16d614bb4e7cfc0a36c3`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff6e3401174e3e4d32e98be9dea020d8cf66ab1dde840a7fbd6d00ae9ff47b`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c664f3d09f0a4e9932acbce930b07fbcad9c594a0b01381e0e1863caea9198a9`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a2fe54066d9fe1a6def590773e9783ecf5015f072e1acd73d6077b89bfc62f`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.2.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d5da5276f34eba3d43021bce1ec8da657af3db13069ff368fe7d9554a607db65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207156ff3a9f6bfca6a94cc3c9d9d0664f9ede755b5f126f040d67dc48414ea6`

```dockerfile
```

-	Layers:
	-	`sha256:ab55c6ddecb392ca89035cd2a8f67faad7bf8c562cf6783a36bfb51b3202c7f7`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:33b3d506101eacd5c956aa2a9ca699142b4e416b2a323b8e08b6e7ff4baf5ee4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:9ccf2f724082e15005463983b21ce300e6a37e42d2f9247160a8ea311121245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246000376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e71b825ab5bf4b21f792087ba4c659d068b9241e7e6df43f6ae34221e7ba315`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:51 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:51 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:51 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:51 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:51 GMT
ARG VERSION=26.1.2.11
# Tue, 17 Feb 2026 20:11:51 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:43 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:43 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:43 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358aea4f7c076ba368df1282f1f04f07c8f663f737f5709a4542bdb92ab78545`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 7.6 MB (7598370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853ad1574df53d6e1debfe0cdd5b1884da948333a4ee32afacdca15a83802c94`  
		Last Modified: Tue, 17 Feb 2026 20:13:09 GMT  
		Size: 208.0 MB (207994605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72fb4592f19d88bdfb886f8987bf22d20fabc42f5b15fc46a8037623150c48b`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f0ee55081f6d58efcf2c52f7819024f89c529ead6333e84b8ca4e1f7fe50f6`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abc4fa545535bc3ebf24fa18a9f566b2b58666110279d7868198317cbba2413`  
		Last Modified: Tue, 17 Feb 2026 20:13:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e04a537211258d7fdbf4b41a0631019dfc16446fbb924dcba78ab1edc47f12`  
		Last Modified: Tue, 17 Feb 2026 20:13:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620b9b548b40539a30fdfcbb5abb283fa2243b1c67b3044c0da351d9980fd2c4`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:691c518013c16f60737305161ee387f1e0ddf7190ff55138e2fb8ce6eb3dc1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8069f56463c7727c5f72ca9901b0bde49672b701050b69fd98a80b4ae6a10e49`

```dockerfile
```

-	Layers:
	-	`sha256:57de74d915f05b81ede453b0a141e47216675a9e6aecb68e83eb64dc181063dd`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:021c8b9d467466063b9d08ca416183864bbd008eea83b5f9109200217c56be0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228204383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd534b39c71930ad029134007379854cd9bb4a3e70f9e6b08542d3bf14fa4b51`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:35 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:35 GMT
ARG VERSION=26.1.2.11
# Tue, 17 Feb 2026 20:11:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:02 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:03 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e437fc694ccf6b344853b723b3019089894d4f5302a098744f989b425e77ea`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 7.6 MB (7577401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a28268f9e3b3b43fe763fd13b19e423f9bedc3d7bb23f576b3b1609a33bbcfe`  
		Last Modified: Tue, 17 Feb 2026 20:12:30 GMT  
		Size: 192.4 MB (192371994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9456d54f9a468d2c5b0da72265dfc1700133424a8da87f04cfc20c0ff2bde9d`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94f07ea74de42bad18cfe1050a598e10af6c3c700bd16d614bb4e7cfc0a36c3`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff6e3401174e3e4d32e98be9dea020d8cf66ab1dde840a7fbd6d00ae9ff47b`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c664f3d09f0a4e9932acbce930b07fbcad9c594a0b01381e0e1863caea9198a9`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a2fe54066d9fe1a6def590773e9783ecf5015f072e1acd73d6077b89bfc62f`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d5da5276f34eba3d43021bce1ec8da657af3db13069ff368fe7d9554a607db65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207156ff3a9f6bfca6a94cc3c9d9d0664f9ede755b5f126f040d67dc48414ea6`

```dockerfile
```

-	Layers:
	-	`sha256:ab55c6ddecb392ca89035cd2a8f67faad7bf8c562cf6783a36bfb51b3202c7f7`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:33b3d506101eacd5c956aa2a9ca699142b4e416b2a323b8e08b6e7ff4baf5ee4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:9ccf2f724082e15005463983b21ce300e6a37e42d2f9247160a8ea311121245d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (246000376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e71b825ab5bf4b21f792087ba4c659d068b9241e7e6df43f6ae34221e7ba315`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:51 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:51 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:51 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:51 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:51 GMT
ARG VERSION=26.1.2.11
# Tue, 17 Feb 2026 20:11:51 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:43 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:43 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:43 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:43 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358aea4f7c076ba368df1282f1f04f07c8f663f737f5709a4542bdb92ab78545`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 7.6 MB (7598370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853ad1574df53d6e1debfe0cdd5b1884da948333a4ee32afacdca15a83802c94`  
		Last Modified: Tue, 17 Feb 2026 20:13:09 GMT  
		Size: 208.0 MB (207994605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72fb4592f19d88bdfb886f8987bf22d20fabc42f5b15fc46a8037623150c48b`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f0ee55081f6d58efcf2c52f7819024f89c529ead6333e84b8ca4e1f7fe50f6`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 865.7 KB (865741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abc4fa545535bc3ebf24fa18a9f566b2b58666110279d7868198317cbba2413`  
		Last Modified: Tue, 17 Feb 2026 20:13:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e04a537211258d7fdbf4b41a0631019dfc16446fbb924dcba78ab1edc47f12`  
		Last Modified: Tue, 17 Feb 2026 20:13:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:620b9b548b40539a30fdfcbb5abb283fa2243b1c67b3044c0da351d9980fd2c4`  
		Last Modified: Tue, 17 Feb 2026 20:13:07 GMT  
		Size: 3.6 KB (3635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:691c518013c16f60737305161ee387f1e0ddf7190ff55138e2fb8ce6eb3dc1ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8069f56463c7727c5f72ca9901b0bde49672b701050b69fd98a80b4ae6a10e49`

```dockerfile
```

-	Layers:
	-	`sha256:57de74d915f05b81ede453b0a141e47216675a9e6aecb68e83eb64dc181063dd`  
		Last Modified: Tue, 17 Feb 2026 20:13:05 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:021c8b9d467466063b9d08ca416183864bbd008eea83b5f9109200217c56be0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228204383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd534b39c71930ad029134007379854cd9bb4a3e70f9e6b08542d3bf14fa4b51`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:35 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:35 GMT
ARG VERSION=26.1.2.11
# Tue, 17 Feb 2026 20:11:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:02 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:03 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07e437fc694ccf6b344853b723b3019089894d4f5302a098744f989b425e77ea`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 7.6 MB (7577401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a28268f9e3b3b43fe763fd13b19e423f9bedc3d7bb23f576b3b1609a33bbcfe`  
		Last Modified: Tue, 17 Feb 2026 20:12:30 GMT  
		Size: 192.4 MB (192371994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9456d54f9a468d2c5b0da72265dfc1700133424a8da87f04cfc20c0ff2bde9d`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e94f07ea74de42bad18cfe1050a598e10af6c3c700bd16d614bb4e7cfc0a36c3`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecff6e3401174e3e4d32e98be9dea020d8cf66ab1dde840a7fbd6d00ae9ff47b`  
		Last Modified: Tue, 17 Feb 2026 20:12:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c664f3d09f0a4e9932acbce930b07fbcad9c594a0b01381e0e1863caea9198a9`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a2fe54066d9fe1a6def590773e9783ecf5015f072e1acd73d6077b89bfc62f`  
		Last Modified: Tue, 17 Feb 2026 20:12:27 GMT  
		Size: 3.6 KB (3634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d5da5276f34eba3d43021bce1ec8da657af3db13069ff368fe7d9554a607db65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:207156ff3a9f6bfca6a94cc3c9d9d0664f9ede755b5f126f040d67dc48414ea6`

```dockerfile
```

-	Layers:
	-	`sha256:ab55c6ddecb392ca89035cd2a8f67faad7bf8c562cf6783a36bfb51b3202c7f7`  
		Last Modified: Tue, 17 Feb 2026 20:12:25 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:cb8ea3c339aa84c1d75e0c9fc08f372e0398576caa3d787e7f27b9bbca483d3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:0ec0e053c41857406923f72d00580eac2b61fe11aff754672a9ed03f172c02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228945044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5381324c8bcc3410608a9c899346d8806971bcef1a1a5fad7b59b6418415de5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:26 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:53 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:53 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dee958d69ceaceb4ea57bc08fb7179f6c7e0987acf3a83c3fb4d05fecc5f2`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 7.6 MB (7598324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258567d60460abdf8fc0d705b07cfb5c2cf9c109302d7d2c766667ce48775f4c`  
		Last Modified: Tue, 17 Feb 2026 20:13:16 GMT  
		Size: 190.9 MB (190939334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88afd8fd9b9d7dc8563b7db8a2a6351683c3b3e457879c7f4c041b98bff53e`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53900b96e71ca59796a1577140c2aea52ebe99495fc78ab718f66f89ce11fda`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306d071c1343d8dc0c6d88a9a96ca5aa60bd057563577ae76fd30fbf89e8a3f`  
		Last Modified: Tue, 17 Feb 2026 20:13:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6fbf6e82586a7efc880a4aa52b6e2c210259ad18c01db546ba7da838bd3af`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9009d2f669d7bd059ba402b69f6770efd463c0a1f88b6c0a81fce2aa343e61b`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f00e22ef556b57f9002953ccb230258a724d206ddecc96ddef872a1715c4cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864971555410cf3c7ecd8e15f929470ad3e6751db3fb535b698bb37a50e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:b03ea5c9cfa2f868003976091441edbc705a684639b36b3607bd13f9e0fa5a85`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2bc2d567de72e07f96d39d437aa8ad8c85de7d62d947633c5197d97d05e3603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a020363e23f68ae53ea85f8d5889d92a049d464d3eac58db615f3903fd82d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:49 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:11:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:18 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:18 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e105b5258b6287684da632f28c009bead56d72476c38c18b71037e43e8e9b7c`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 7.6 MB (7577435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d420eedbfb97f76c475c4139188424ad202fa0e076dcced2c2495768b59ac`  
		Last Modified: Tue, 17 Feb 2026 20:12:41 GMT  
		Size: 178.0 MB (178016046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477e7fcc96d3a9fe18cfd60a3109816b4a377d41bfdb46d3e0a3438fd193976`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a0a0e8730d6ac8153fd30fc3f7dc73e6e5160fa253c8ffa137dbdb06914b4`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55e4b063f018d389136b40b857059bb4e1bb4f5af6046376bb9edfcad0241ff`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac4fd6f889704ea3b167cbbc7b274f8178ae69d00df70debe3e214aa936b13`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96f921752d4141c565ccca7e44ec7c882d09ac1601be61a0997273ce77657c`  
		Last Modified: Tue, 17 Feb 2026 20:12:40 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e40bf21f69748ff21ecb45294a3d5abada6026f07908ff61c72014db1bb06598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a041960efb6f4644dde88a255c026fc5cac64f703efced83f24300b69ce680`

```dockerfile
```

-	Layers:
	-	`sha256:d61611774bdc1996895d1e9b295614f62dae75e1c939a7fb15d6abaa66d5a746`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:cb8ea3c339aa84c1d75e0c9fc08f372e0398576caa3d787e7f27b9bbca483d3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:0ec0e053c41857406923f72d00580eac2b61fe11aff754672a9ed03f172c02c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228945044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5381324c8bcc3410608a9c899346d8806971bcef1a1a5fad7b59b6418415de5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:40:06 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:40:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:40:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:40:09 GMT
ADD file:52c0e467fa2e92f101018df01a0ff56580c752b7553fbe6df88e16b02af6d4ee in / 
# Tue, 10 Feb 2026 17:40:09 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:12:26 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:12:26 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:12:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:12:26 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:12:26 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:12:26 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:53 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:53 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b1cba2e842ca52b95817f958faf99734080c78e92e43ce609cde9244867b49ed`  
		Last Modified: Tue, 10 Feb 2026 18:13:31 GMT  
		Size: 29.5 MB (29537366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820dee958d69ceaceb4ea57bc08fb7179f6c7e0987acf3a83c3fb4d05fecc5f2`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 7.6 MB (7598324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258567d60460abdf8fc0d705b07cfb5c2cf9c109302d7d2c766667ce48775f4c`  
		Last Modified: Tue, 17 Feb 2026 20:13:16 GMT  
		Size: 190.9 MB (190939334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e88afd8fd9b9d7dc8563b7db8a2a6351683c3b3e457879c7f4c041b98bff53e`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53900b96e71ca59796a1577140c2aea52ebe99495fc78ab718f66f89ce11fda`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b306d071c1343d8dc0c6d88a9a96ca5aa60bd057563577ae76fd30fbf89e8a3f`  
		Last Modified: Tue, 17 Feb 2026 20:13:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c6fbf6e82586a7efc880a4aa52b6e2c210259ad18c01db546ba7da838bd3af`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9009d2f669d7bd059ba402b69f6770efd463c0a1f88b6c0a81fce2aa343e61b`  
		Last Modified: Tue, 17 Feb 2026 20:13:14 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0f00e22ef556b57f9002953ccb230258a724d206ddecc96ddef872a1715c4cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b864971555410cf3c7ecd8e15f929470ad3e6751db3fb535b698bb37a50e09a9`

```dockerfile
```

-	Layers:
	-	`sha256:b03ea5c9cfa2f868003976091441edbc705a684639b36b3607bd13f9e0fa5a85`  
		Last Modified: Tue, 17 Feb 2026 20:13:12 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:2bc2d567de72e07f96d39d437aa8ad8c85de7d62d947633c5197d97d05e3603b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213848446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6a020363e23f68ae53ea85f8d5889d92a049d464d3eac58db615f3903fd82d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 10 Feb 2026 17:42:29 GMT
ARG RELEASE
# Tue, 10 Feb 2026 17:42:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 10 Feb 2026 17:42:29 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 10 Feb 2026 17:42:31 GMT
ADD file:a85469998596adb526225bc2a2ce3f2cd899fb87a09539f6f84d359c6b935769 in / 
# Tue, 10 Feb 2026 17:42:31 GMT
CMD ["/bin/bash"]
# Tue, 17 Feb 2026 20:11:49 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Tue, 17 Feb 2026 20:11:49 GMT
ARG apt_archive=http://archive.ubuntu.com
# Tue, 17 Feb 2026 20:11:49 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPO_CHANNEL=stable
# Tue, 17 Feb 2026 20:11:49 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Tue, 17 Feb 2026 20:11:49 GMT
ARG VERSION=25.8.16.34
# Tue, 17 Feb 2026 20:11:49 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
ENV LANG=en_US.UTF-8
# Tue, 17 Feb 2026 20:12:18 GMT
ENV TZ=UTC
# Tue, 17 Feb 2026 20:12:18 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Feb 2026 20:12:18 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Tue, 17 Feb 2026 20:12:18 GMT
VOLUME [/var/lib/clickhouse]
# Tue, 17 Feb 2026 20:12:18 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Tue, 17 Feb 2026 20:12:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:c36472b3458398be28ecbfebbaac44143c040eae73411baded48a22060d3055b`  
		Last Modified: Tue, 10 Feb 2026 18:13:38 GMT  
		Size: 27.4 MB (27384944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e105b5258b6287684da632f28c009bead56d72476c38c18b71037e43e8e9b7c`  
		Last Modified: Tue, 17 Feb 2026 20:12:39 GMT  
		Size: 7.6 MB (7577435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494d420eedbfb97f76c475c4139188424ad202fa0e076dcced2c2495768b59ac`  
		Last Modified: Tue, 17 Feb 2026 20:12:41 GMT  
		Size: 178.0 MB (178016046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c477e7fcc96d3a9fe18cfd60a3109816b4a377d41bfdb46d3e0a3438fd193976`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56a0a0e8730d6ac8153fd30fc3f7dc73e6e5160fa253c8ffa137dbdb06914b4`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55e4b063f018d389136b40b857059bb4e1bb4f5af6046376bb9edfcad0241ff`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ac4fd6f889704ea3b167cbbc7b274f8178ae69d00df70debe3e214aa936b13`  
		Last Modified: Tue, 17 Feb 2026 20:12:38 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff96f921752d4141c565ccca7e44ec7c882d09ac1601be61a0997273ce77657c`  
		Last Modified: Tue, 17 Feb 2026 20:12:40 GMT  
		Size: 3.6 KB (3608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:e40bf21f69748ff21ecb45294a3d5abada6026f07908ff61c72014db1bb06598
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8a041960efb6f4644dde88a255c026fc5cac64f703efced83f24300b69ce680`

```dockerfile
```

-	Layers:
	-	`sha256:d61611774bdc1996895d1e9b295614f62dae75e1c939a7fb15d6abaa66d5a746`  
		Last Modified: Tue, 17 Feb 2026 20:12:37 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json
