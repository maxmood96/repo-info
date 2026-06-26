<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.24`](#clickhouse25824)
-	[`clickhouse:25.8.24-jammy`](#clickhouse25824-jammy)
-	[`clickhouse:25.8.24.21`](#clickhouse2582421)
-	[`clickhouse:25.8.24.21-jammy`](#clickhouse2582421-jammy)
-	[`clickhouse:26.3`](#clickhouse263)
-	[`clickhouse:26.3-jammy`](#clickhouse263-jammy)
-	[`clickhouse:26.3.15`](#clickhouse26315)
-	[`clickhouse:26.3.15-jammy`](#clickhouse26315-jammy)
-	[`clickhouse:26.3.15.4`](#clickhouse263154)
-	[`clickhouse:26.3.15.4-jammy`](#clickhouse263154-jammy)
-	[`clickhouse:26.4`](#clickhouse264)
-	[`clickhouse:26.4-jammy`](#clickhouse264-jammy)
-	[`clickhouse:26.4.4`](#clickhouse2644)
-	[`clickhouse:26.4.4-jammy`](#clickhouse2644-jammy)
-	[`clickhouse:26.4.4.38`](#clickhouse264438)
-	[`clickhouse:26.4.4.38-jammy`](#clickhouse264438-jammy)
-	[`clickhouse:26.5`](#clickhouse265)
-	[`clickhouse:26.5-jammy`](#clickhouse265-jammy)
-	[`clickhouse:26.5.3`](#clickhouse2653)
-	[`clickhouse:26.5.3-jammy`](#clickhouse2653-jammy)
-	[`clickhouse:26.5.3.52`](#clickhouse265352)
-	[`clickhouse:26.5.3.52-jammy`](#clickhouse265352-jammy)
-	[`clickhouse:26.6`](#clickhouse266)
-	[`clickhouse:26.6-jammy`](#clickhouse266-jammy)
-	[`clickhouse:26.6.1`](#clickhouse2661)
-	[`clickhouse:26.6.1-jammy`](#clickhouse2661-jammy)
-	[`clickhouse:26.6.1.1193`](#clickhouse26611193)
-	[`clickhouse:26.6.1.1193-jammy`](#clickhouse26611193-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:18bf639a964a6ec2f73961b64ee741c9df937a0d7f3c88044af890e36aa01602
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:58bfef34cb332f1a648d4b81384c7738d586cc1138c8a418efc53eda87bb1a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229742631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0393b6b82a0974311360423dc34ee7458f7b26a5d42c4dc13b7a0aaf4ec7ea7d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 20:13:52 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:13:52 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:13:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:13:52 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:13:52 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:13:52 GMT
ARG VERSION=25.8.24.21
# Fri, 22 May 2026 20:13:52 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:16 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:16 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:16 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c0282c550652100f28e2da62108bbc623017749bbe71b18ceed33443f6dca7`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 7.6 MB (7599313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de18a01773d2ca6e805635a191ef8028857524798956f388c84d8d729cd777e9`  
		Last Modified: Fri, 22 May 2026 20:14:42 GMT  
		Size: 191.5 MB (191536614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639ff7803e6996c30df508f76b8c465b314ff831e581d5b0d02e537b212d0d0c`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710ba67d0e879220e450304d634ca9b7b15596de2fc8d005d514472a526d6ee`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9131807896f9276949683ba8ef23858cde62f8411b3dda83086dbe22f4e9312`  
		Last Modified: Fri, 22 May 2026 20:14:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e0d51b44dc15ef33221555f31fa9bbcc54f772815d462cf7d3f006323d956b`  
		Last Modified: Fri, 22 May 2026 20:14:39 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739128bc428a8fb7fd804f52eebc6d032fb0c6e957f8affb75a0860a630bcc0e`  
		Last Modified: Fri, 22 May 2026 20:14:40 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f072909f3378c3cc2f19ca644f6dd9883a1b08407d49ef7184aacf0fd2b70edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1b66315f609e8da306d637cdae3a64861bbd0dec81cf9651ef8d0ec697b453`

```dockerfile
```

-	Layers:
	-	`sha256:8f9a0766d415c439caca1a36b8646543e0e00fe3750281efd3a6f04fb9e41fc6`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:07aaeee0079c154e2f553132a44663f68f79807ffb7071d98cbcaf87e449b277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214762200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa7e71f6e177009a33b95ff3d378b8628a8f03d89e13ee84cd29d26a31ef11e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 20:14:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:15 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:15 GMT
ARG VERSION=25.8.24.21
# Fri, 22 May 2026 20:14:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:43 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:43 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:43 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:43 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:43 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe324c3e425059558f6841667b6fdeef96748949b777b74f036ffad5699d483`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 7.6 MB (7578944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc4217bd1ce03a48e06768a3445f22cd7c0aa27a375891ee1d650a43ec72b6`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 178.7 MB (178706607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecae983caf8ebdae2d5ff5c251c9e8d12058a947fffa05f736089c06d6661c2`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df70b86b1fb877d6e9ca88035405b4611d54af75ce40dd7c1b2167d248dc91`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d166ff932a7464238d955c4d69a40ecc6c55e500a3fdc19cebe57a0982f4e81d`  
		Last Modified: Fri, 22 May 2026 20:15:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00ec4e11070cc3aba308e1e6f30c3240691c138889156e56c0bf9629d7c5951`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe88076300a4de524dc2224fa04ac1ea0009ef631c14779f09f7cae96ffe6e3`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fb26df47139f46b43de4845b7fca3f09c957b99050150c8cc37d08b1b117cd1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75508d39e8f9d467b113f529ecc496dbb6e37e17d171e493b89331b6b8a1e459`

```dockerfile
```

-	Layers:
	-	`sha256:5ca3b6c1f220620f13df3362507b6ff8738149fc9418671509d14c9d5991d967`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 26.4 KB (26423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:18bf639a964a6ec2f73961b64ee741c9df937a0d7f3c88044af890e36aa01602
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:58bfef34cb332f1a648d4b81384c7738d586cc1138c8a418efc53eda87bb1a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229742631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0393b6b82a0974311360423dc34ee7458f7b26a5d42c4dc13b7a0aaf4ec7ea7d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 20:13:52 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:13:52 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:13:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:13:52 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:13:52 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:13:52 GMT
ARG VERSION=25.8.24.21
# Fri, 22 May 2026 20:13:52 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:16 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:16 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:16 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c0282c550652100f28e2da62108bbc623017749bbe71b18ceed33443f6dca7`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 7.6 MB (7599313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de18a01773d2ca6e805635a191ef8028857524798956f388c84d8d729cd777e9`  
		Last Modified: Fri, 22 May 2026 20:14:42 GMT  
		Size: 191.5 MB (191536614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639ff7803e6996c30df508f76b8c465b314ff831e581d5b0d02e537b212d0d0c`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710ba67d0e879220e450304d634ca9b7b15596de2fc8d005d514472a526d6ee`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9131807896f9276949683ba8ef23858cde62f8411b3dda83086dbe22f4e9312`  
		Last Modified: Fri, 22 May 2026 20:14:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e0d51b44dc15ef33221555f31fa9bbcc54f772815d462cf7d3f006323d956b`  
		Last Modified: Fri, 22 May 2026 20:14:39 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739128bc428a8fb7fd804f52eebc6d032fb0c6e957f8affb75a0860a630bcc0e`  
		Last Modified: Fri, 22 May 2026 20:14:40 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f072909f3378c3cc2f19ca644f6dd9883a1b08407d49ef7184aacf0fd2b70edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1b66315f609e8da306d637cdae3a64861bbd0dec81cf9651ef8d0ec697b453`

```dockerfile
```

-	Layers:
	-	`sha256:8f9a0766d415c439caca1a36b8646543e0e00fe3750281efd3a6f04fb9e41fc6`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:07aaeee0079c154e2f553132a44663f68f79807ffb7071d98cbcaf87e449b277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214762200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa7e71f6e177009a33b95ff3d378b8628a8f03d89e13ee84cd29d26a31ef11e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 20:14:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:15 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:15 GMT
ARG VERSION=25.8.24.21
# Fri, 22 May 2026 20:14:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:43 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:43 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:43 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:43 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:43 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe324c3e425059558f6841667b6fdeef96748949b777b74f036ffad5699d483`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 7.6 MB (7578944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc4217bd1ce03a48e06768a3445f22cd7c0aa27a375891ee1d650a43ec72b6`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 178.7 MB (178706607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecae983caf8ebdae2d5ff5c251c9e8d12058a947fffa05f736089c06d6661c2`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df70b86b1fb877d6e9ca88035405b4611d54af75ce40dd7c1b2167d248dc91`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d166ff932a7464238d955c4d69a40ecc6c55e500a3fdc19cebe57a0982f4e81d`  
		Last Modified: Fri, 22 May 2026 20:15:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00ec4e11070cc3aba308e1e6f30c3240691c138889156e56c0bf9629d7c5951`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe88076300a4de524dc2224fa04ac1ea0009ef631c14779f09f7cae96ffe6e3`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fb26df47139f46b43de4845b7fca3f09c957b99050150c8cc37d08b1b117cd1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75508d39e8f9d467b113f529ecc496dbb6e37e17d171e493b89331b6b8a1e459`

```dockerfile
```

-	Layers:
	-	`sha256:5ca3b6c1f220620f13df3362507b6ff8738149fc9418671509d14c9d5991d967`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 26.4 KB (26423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.24`

```console
$ docker pull clickhouse@sha256:18bf639a964a6ec2f73961b64ee741c9df937a0d7f3c88044af890e36aa01602
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.24` - linux; amd64

```console
$ docker pull clickhouse@sha256:58bfef34cb332f1a648d4b81384c7738d586cc1138c8a418efc53eda87bb1a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229742631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0393b6b82a0974311360423dc34ee7458f7b26a5d42c4dc13b7a0aaf4ec7ea7d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 20:13:52 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:13:52 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:13:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:13:52 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:13:52 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:13:52 GMT
ARG VERSION=25.8.24.21
# Fri, 22 May 2026 20:13:52 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:16 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:16 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:16 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c0282c550652100f28e2da62108bbc623017749bbe71b18ceed33443f6dca7`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 7.6 MB (7599313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de18a01773d2ca6e805635a191ef8028857524798956f388c84d8d729cd777e9`  
		Last Modified: Fri, 22 May 2026 20:14:42 GMT  
		Size: 191.5 MB (191536614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639ff7803e6996c30df508f76b8c465b314ff831e581d5b0d02e537b212d0d0c`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710ba67d0e879220e450304d634ca9b7b15596de2fc8d005d514472a526d6ee`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9131807896f9276949683ba8ef23858cde62f8411b3dda83086dbe22f4e9312`  
		Last Modified: Fri, 22 May 2026 20:14:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e0d51b44dc15ef33221555f31fa9bbcc54f772815d462cf7d3f006323d956b`  
		Last Modified: Fri, 22 May 2026 20:14:39 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739128bc428a8fb7fd804f52eebc6d032fb0c6e957f8affb75a0860a630bcc0e`  
		Last Modified: Fri, 22 May 2026 20:14:40 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.24` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f072909f3378c3cc2f19ca644f6dd9883a1b08407d49ef7184aacf0fd2b70edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1b66315f609e8da306d637cdae3a64861bbd0dec81cf9651ef8d0ec697b453`

```dockerfile
```

-	Layers:
	-	`sha256:8f9a0766d415c439caca1a36b8646543e0e00fe3750281efd3a6f04fb9e41fc6`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.24` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:07aaeee0079c154e2f553132a44663f68f79807ffb7071d98cbcaf87e449b277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214762200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa7e71f6e177009a33b95ff3d378b8628a8f03d89e13ee84cd29d26a31ef11e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 20:14:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:15 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:15 GMT
ARG VERSION=25.8.24.21
# Fri, 22 May 2026 20:14:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:43 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:43 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:43 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:43 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:43 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe324c3e425059558f6841667b6fdeef96748949b777b74f036ffad5699d483`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 7.6 MB (7578944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc4217bd1ce03a48e06768a3445f22cd7c0aa27a375891ee1d650a43ec72b6`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 178.7 MB (178706607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecae983caf8ebdae2d5ff5c251c9e8d12058a947fffa05f736089c06d6661c2`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df70b86b1fb877d6e9ca88035405b4611d54af75ce40dd7c1b2167d248dc91`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d166ff932a7464238d955c4d69a40ecc6c55e500a3fdc19cebe57a0982f4e81d`  
		Last Modified: Fri, 22 May 2026 20:15:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00ec4e11070cc3aba308e1e6f30c3240691c138889156e56c0bf9629d7c5951`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe88076300a4de524dc2224fa04ac1ea0009ef631c14779f09f7cae96ffe6e3`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.24` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fb26df47139f46b43de4845b7fca3f09c957b99050150c8cc37d08b1b117cd1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75508d39e8f9d467b113f529ecc496dbb6e37e17d171e493b89331b6b8a1e459`

```dockerfile
```

-	Layers:
	-	`sha256:5ca3b6c1f220620f13df3362507b6ff8738149fc9418671509d14c9d5991d967`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 26.4 KB (26423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.24-jammy`

```console
$ docker pull clickhouse@sha256:18bf639a964a6ec2f73961b64ee741c9df937a0d7f3c88044af890e36aa01602
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.24-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:58bfef34cb332f1a648d4b81384c7738d586cc1138c8a418efc53eda87bb1a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229742631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0393b6b82a0974311360423dc34ee7458f7b26a5d42c4dc13b7a0aaf4ec7ea7d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 20:13:52 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:13:52 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:13:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:13:52 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:13:52 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:13:52 GMT
ARG VERSION=25.8.24.21
# Fri, 22 May 2026 20:13:52 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:16 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:16 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:16 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c0282c550652100f28e2da62108bbc623017749bbe71b18ceed33443f6dca7`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 7.6 MB (7599313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de18a01773d2ca6e805635a191ef8028857524798956f388c84d8d729cd777e9`  
		Last Modified: Fri, 22 May 2026 20:14:42 GMT  
		Size: 191.5 MB (191536614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639ff7803e6996c30df508f76b8c465b314ff831e581d5b0d02e537b212d0d0c`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710ba67d0e879220e450304d634ca9b7b15596de2fc8d005d514472a526d6ee`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9131807896f9276949683ba8ef23858cde62f8411b3dda83086dbe22f4e9312`  
		Last Modified: Fri, 22 May 2026 20:14:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e0d51b44dc15ef33221555f31fa9bbcc54f772815d462cf7d3f006323d956b`  
		Last Modified: Fri, 22 May 2026 20:14:39 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739128bc428a8fb7fd804f52eebc6d032fb0c6e957f8affb75a0860a630bcc0e`  
		Last Modified: Fri, 22 May 2026 20:14:40 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.24-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f072909f3378c3cc2f19ca644f6dd9883a1b08407d49ef7184aacf0fd2b70edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1b66315f609e8da306d637cdae3a64861bbd0dec81cf9651ef8d0ec697b453`

```dockerfile
```

-	Layers:
	-	`sha256:8f9a0766d415c439caca1a36b8646543e0e00fe3750281efd3a6f04fb9e41fc6`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.24-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:07aaeee0079c154e2f553132a44663f68f79807ffb7071d98cbcaf87e449b277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214762200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa7e71f6e177009a33b95ff3d378b8628a8f03d89e13ee84cd29d26a31ef11e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 20:14:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:15 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:15 GMT
ARG VERSION=25.8.24.21
# Fri, 22 May 2026 20:14:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:43 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:43 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:43 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:43 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:43 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe324c3e425059558f6841667b6fdeef96748949b777b74f036ffad5699d483`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 7.6 MB (7578944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc4217bd1ce03a48e06768a3445f22cd7c0aa27a375891ee1d650a43ec72b6`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 178.7 MB (178706607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecae983caf8ebdae2d5ff5c251c9e8d12058a947fffa05f736089c06d6661c2`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df70b86b1fb877d6e9ca88035405b4611d54af75ce40dd7c1b2167d248dc91`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d166ff932a7464238d955c4d69a40ecc6c55e500a3fdc19cebe57a0982f4e81d`  
		Last Modified: Fri, 22 May 2026 20:15:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00ec4e11070cc3aba308e1e6f30c3240691c138889156e56c0bf9629d7c5951`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe88076300a4de524dc2224fa04ac1ea0009ef631c14779f09f7cae96ffe6e3`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.24-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fb26df47139f46b43de4845b7fca3f09c957b99050150c8cc37d08b1b117cd1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75508d39e8f9d467b113f529ecc496dbb6e37e17d171e493b89331b6b8a1e459`

```dockerfile
```

-	Layers:
	-	`sha256:5ca3b6c1f220620f13df3362507b6ff8738149fc9418671509d14c9d5991d967`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 26.4 KB (26423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.24.21`

```console
$ docker pull clickhouse@sha256:18bf639a964a6ec2f73961b64ee741c9df937a0d7f3c88044af890e36aa01602
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.24.21` - linux; amd64

```console
$ docker pull clickhouse@sha256:58bfef34cb332f1a648d4b81384c7738d586cc1138c8a418efc53eda87bb1a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229742631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0393b6b82a0974311360423dc34ee7458f7b26a5d42c4dc13b7a0aaf4ec7ea7d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 20:13:52 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:13:52 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:13:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:13:52 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:13:52 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:13:52 GMT
ARG VERSION=25.8.24.21
# Fri, 22 May 2026 20:13:52 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:16 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:16 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:16 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c0282c550652100f28e2da62108bbc623017749bbe71b18ceed33443f6dca7`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 7.6 MB (7599313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de18a01773d2ca6e805635a191ef8028857524798956f388c84d8d729cd777e9`  
		Last Modified: Fri, 22 May 2026 20:14:42 GMT  
		Size: 191.5 MB (191536614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639ff7803e6996c30df508f76b8c465b314ff831e581d5b0d02e537b212d0d0c`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710ba67d0e879220e450304d634ca9b7b15596de2fc8d005d514472a526d6ee`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9131807896f9276949683ba8ef23858cde62f8411b3dda83086dbe22f4e9312`  
		Last Modified: Fri, 22 May 2026 20:14:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e0d51b44dc15ef33221555f31fa9bbcc54f772815d462cf7d3f006323d956b`  
		Last Modified: Fri, 22 May 2026 20:14:39 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739128bc428a8fb7fd804f52eebc6d032fb0c6e957f8affb75a0860a630bcc0e`  
		Last Modified: Fri, 22 May 2026 20:14:40 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.24.21` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f072909f3378c3cc2f19ca644f6dd9883a1b08407d49ef7184aacf0fd2b70edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1b66315f609e8da306d637cdae3a64861bbd0dec81cf9651ef8d0ec697b453`

```dockerfile
```

-	Layers:
	-	`sha256:8f9a0766d415c439caca1a36b8646543e0e00fe3750281efd3a6f04fb9e41fc6`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.24.21` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:07aaeee0079c154e2f553132a44663f68f79807ffb7071d98cbcaf87e449b277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214762200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa7e71f6e177009a33b95ff3d378b8628a8f03d89e13ee84cd29d26a31ef11e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 20:14:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:15 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:15 GMT
ARG VERSION=25.8.24.21
# Fri, 22 May 2026 20:14:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:43 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:43 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:43 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:43 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:43 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe324c3e425059558f6841667b6fdeef96748949b777b74f036ffad5699d483`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 7.6 MB (7578944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc4217bd1ce03a48e06768a3445f22cd7c0aa27a375891ee1d650a43ec72b6`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 178.7 MB (178706607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecae983caf8ebdae2d5ff5c251c9e8d12058a947fffa05f736089c06d6661c2`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df70b86b1fb877d6e9ca88035405b4611d54af75ce40dd7c1b2167d248dc91`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d166ff932a7464238d955c4d69a40ecc6c55e500a3fdc19cebe57a0982f4e81d`  
		Last Modified: Fri, 22 May 2026 20:15:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00ec4e11070cc3aba308e1e6f30c3240691c138889156e56c0bf9629d7c5951`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe88076300a4de524dc2224fa04ac1ea0009ef631c14779f09f7cae96ffe6e3`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.24.21` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fb26df47139f46b43de4845b7fca3f09c957b99050150c8cc37d08b1b117cd1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75508d39e8f9d467b113f529ecc496dbb6e37e17d171e493b89331b6b8a1e459`

```dockerfile
```

-	Layers:
	-	`sha256:5ca3b6c1f220620f13df3362507b6ff8738149fc9418671509d14c9d5991d967`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 26.4 KB (26423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.24.21-jammy`

```console
$ docker pull clickhouse@sha256:18bf639a964a6ec2f73961b64ee741c9df937a0d7f3c88044af890e36aa01602
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.24.21-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:58bfef34cb332f1a648d4b81384c7738d586cc1138c8a418efc53eda87bb1a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.7 MB (229742631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0393b6b82a0974311360423dc34ee7458f7b26a5d42c4dc13b7a0aaf4ec7ea7d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 20:13:52 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:13:52 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:13:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:13:52 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:13:52 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:13:52 GMT
ARG VERSION=25.8.24.21
# Fri, 22 May 2026 20:13:52 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:14 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:16 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:16 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:16 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:16 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:16 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:16 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:16 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c0282c550652100f28e2da62108bbc623017749bbe71b18ceed33443f6dca7`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 7.6 MB (7599313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de18a01773d2ca6e805635a191ef8028857524798956f388c84d8d729cd777e9`  
		Last Modified: Fri, 22 May 2026 20:14:42 GMT  
		Size: 191.5 MB (191536614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639ff7803e6996c30df508f76b8c465b314ff831e581d5b0d02e537b212d0d0c`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710ba67d0e879220e450304d634ca9b7b15596de2fc8d005d514472a526d6ee`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 865.7 KB (865746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9131807896f9276949683ba8ef23858cde62f8411b3dda83086dbe22f4e9312`  
		Last Modified: Fri, 22 May 2026 20:14:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e0d51b44dc15ef33221555f31fa9bbcc54f772815d462cf7d3f006323d956b`  
		Last Modified: Fri, 22 May 2026 20:14:39 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739128bc428a8fb7fd804f52eebc6d032fb0c6e957f8affb75a0860a630bcc0e`  
		Last Modified: Fri, 22 May 2026 20:14:40 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.24.21-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:f072909f3378c3cc2f19ca644f6dd9883a1b08407d49ef7184aacf0fd2b70edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a1b66315f609e8da306d637cdae3a64861bbd0dec81cf9651ef8d0ec697b453`

```dockerfile
```

-	Layers:
	-	`sha256:8f9a0766d415c439caca1a36b8646543e0e00fe3750281efd3a6f04fb9e41fc6`  
		Last Modified: Fri, 22 May 2026 20:14:38 GMT  
		Size: 26.2 KB (26235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.24.21-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:07aaeee0079c154e2f553132a44663f68f79807ffb7071d98cbcaf87e449b277
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.8 MB (214762200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa7e71f6e177009a33b95ff3d378b8628a8f03d89e13ee84cd29d26a31ef11e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 20:14:15 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:15 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:15 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:15 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:15 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:15 GMT
ARG VERSION=25.8.24.21
# Fri, 22 May 2026 20:14:15 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:43 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:43 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.24.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:43 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:43 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:43 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:43 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:43 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe324c3e425059558f6841667b6fdeef96748949b777b74f036ffad5699d483`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 7.6 MB (7578944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2cc4217bd1ce03a48e06768a3445f22cd7c0aa27a375891ee1d650a43ec72b6`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 178.7 MB (178706607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ecae983caf8ebdae2d5ff5c251c9e8d12058a947fffa05f736089c06d6661c2`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82df70b86b1fb877d6e9ca88035405b4611d54af75ce40dd7c1b2167d248dc91`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d166ff932a7464238d955c4d69a40ecc6c55e500a3fdc19cebe57a0982f4e81d`  
		Last Modified: Fri, 22 May 2026 20:15:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00ec4e11070cc3aba308e1e6f30c3240691c138889156e56c0bf9629d7c5951`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe88076300a4de524dc2224fa04ac1ea0009ef631c14779f09f7cae96ffe6e3`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.24.21-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fb26df47139f46b43de4845b7fca3f09c957b99050150c8cc37d08b1b117cd1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75508d39e8f9d467b113f529ecc496dbb6e37e17d171e493b89331b6b8a1e459`

```dockerfile
```

-	Layers:
	-	`sha256:5ca3b6c1f220620f13df3362507b6ff8738149fc9418671509d14c9d5991d967`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 26.4 KB (26423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3`

```console
$ docker pull clickhouse@sha256:97e8f72ba5ea68bae106dc03c39fcd7bb0eeaa0a1fa5b3403b3ea39b2bfa3381
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:943fdd9d6bafc53242d5ab2d2857b41f9ab8969dde7268fd33d380d03ae6e4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265176695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7ac6e6ee39b0bbd98fddd354104fc5798a4c5cf9ba560c2f074ccb02c42ecc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:43 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:43 GMT
ARG VERSION=26.3.15.4
# Fri, 26 Jun 2026 17:48:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:08 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:08 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:09 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38216c34971dba715121ac70e16c64042afc90e8ba74b1ec38601e47eb5d18da`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 7.6 MB (7555064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620737f98b2c2b28baaeb715e057822c54c3ac17763a32f2063b0944bf99ac4`  
		Last Modified: Fri, 26 Jun 2026 17:49:39 GMT  
		Size: 227.0 MB (227014894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e403cc00187b13b2ed2cb89cc5c4a942425ce2d5e42ffb06a25bb95a4bd08`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f2820a7bed2f24263b822edd2552d79c8204b27737832fe14957bda5f46dc3`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5459ef7da2345df368e41e7a127ac94d12e4c09bc30dede769c6d488977c721`  
		Last Modified: Fri, 26 Jun 2026 17:49:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9abffa579062c580b6b12358a3e0ad321124c23c7d6420577aa01ea99d7b48`  
		Last Modified: Fri, 26 Jun 2026 17:49:35 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8572df1a216f1627c9cac98c314d96fcdac6d32f361ec2e05d874da0f3d26203`  
		Last Modified: Fri, 26 Jun 2026 17:49:36 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:38463182a568ad43f21797199ad0a821010bab9b292010e77ef08bf6d0b351b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cddaad96ffb5d9257bbb54159f1057110220aa939ca4465b6022467f819470`

```dockerfile
```

-	Layers:
	-	`sha256:b1cba557c25f569db8a1f37e266f3981051019aef51d8698a745fc8867882b80`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 26.8 KB (26836 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:87ba1cec7d207db221a87afadbae9908b05e60c129e49123a66dc88ca4c1fd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246611660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7dcb539318c303284510428f79ae3b3ed165a4f6d1db2dd7443748d3180ec0b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:34 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:34 GMT
ARG VERSION=26.3.15.4
# Fri, 26 Jun 2026 17:53:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:54:00 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:54:00 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:54:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:54:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8a137aaa0902a87fb2cae745f866ee4a1c7908934a431dfb3a7146c032ac1`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 7.5 MB (7535269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a98ccb396d35d69ff41db54de6a8ffc02060dbcf8c5654f4b3ca3826141a21`  
		Last Modified: Fri, 26 Jun 2026 17:54:26 GMT  
		Size: 210.6 MB (210599719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ece11b79f8fe48a2dbe3cd3f13ca80e9c44e80ac2043a9a2d7641a2da83396e`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aebc0b3f40e42a3896fd2cf5777b4be657fffc9e5742514dda2f59728e83275`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44abb41eab15f74bb7625f8ffc079d7444cfead6ad401e1c29fe2f898c391f7`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fdd25aadbcfad460702922ee99ab4fe6365a32d33fbcc95245aa0be456a79`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdbd261ff900784ddbeeb91f1f57ae786a90a768b5eadf3dd147b211f2bc50b`  
		Last Modified: Fri, 26 Jun 2026 17:54:24 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:28c285e03cdabab87ffbdf61692940646bd26ece6500faef94cef4d10f12a4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f54c943e26a32b57061a001eeb5c9ddf0281057b0d7bcdfbe5bce15cfce1ec7`

```dockerfile
```

-	Layers:
	-	`sha256:9eee0a9398985ea52f2e4891a8e34f384d1006b45866ceb9cc45871305b004d4`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 27.0 KB (27047 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3-jammy`

```console
$ docker pull clickhouse@sha256:97e8f72ba5ea68bae106dc03c39fcd7bb0eeaa0a1fa5b3403b3ea39b2bfa3381
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:943fdd9d6bafc53242d5ab2d2857b41f9ab8969dde7268fd33d380d03ae6e4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265176695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7ac6e6ee39b0bbd98fddd354104fc5798a4c5cf9ba560c2f074ccb02c42ecc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:43 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:43 GMT
ARG VERSION=26.3.15.4
# Fri, 26 Jun 2026 17:48:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:08 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:08 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:09 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38216c34971dba715121ac70e16c64042afc90e8ba74b1ec38601e47eb5d18da`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 7.6 MB (7555064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620737f98b2c2b28baaeb715e057822c54c3ac17763a32f2063b0944bf99ac4`  
		Last Modified: Fri, 26 Jun 2026 17:49:39 GMT  
		Size: 227.0 MB (227014894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e403cc00187b13b2ed2cb89cc5c4a942425ce2d5e42ffb06a25bb95a4bd08`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f2820a7bed2f24263b822edd2552d79c8204b27737832fe14957bda5f46dc3`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5459ef7da2345df368e41e7a127ac94d12e4c09bc30dede769c6d488977c721`  
		Last Modified: Fri, 26 Jun 2026 17:49:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9abffa579062c580b6b12358a3e0ad321124c23c7d6420577aa01ea99d7b48`  
		Last Modified: Fri, 26 Jun 2026 17:49:35 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8572df1a216f1627c9cac98c314d96fcdac6d32f361ec2e05d874da0f3d26203`  
		Last Modified: Fri, 26 Jun 2026 17:49:36 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:38463182a568ad43f21797199ad0a821010bab9b292010e77ef08bf6d0b351b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cddaad96ffb5d9257bbb54159f1057110220aa939ca4465b6022467f819470`

```dockerfile
```

-	Layers:
	-	`sha256:b1cba557c25f569db8a1f37e266f3981051019aef51d8698a745fc8867882b80`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 26.8 KB (26836 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:87ba1cec7d207db221a87afadbae9908b05e60c129e49123a66dc88ca4c1fd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246611660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7dcb539318c303284510428f79ae3b3ed165a4f6d1db2dd7443748d3180ec0b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:34 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:34 GMT
ARG VERSION=26.3.15.4
# Fri, 26 Jun 2026 17:53:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:54:00 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:54:00 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:54:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:54:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8a137aaa0902a87fb2cae745f866ee4a1c7908934a431dfb3a7146c032ac1`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 7.5 MB (7535269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a98ccb396d35d69ff41db54de6a8ffc02060dbcf8c5654f4b3ca3826141a21`  
		Last Modified: Fri, 26 Jun 2026 17:54:26 GMT  
		Size: 210.6 MB (210599719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ece11b79f8fe48a2dbe3cd3f13ca80e9c44e80ac2043a9a2d7641a2da83396e`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aebc0b3f40e42a3896fd2cf5777b4be657fffc9e5742514dda2f59728e83275`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44abb41eab15f74bb7625f8ffc079d7444cfead6ad401e1c29fe2f898c391f7`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fdd25aadbcfad460702922ee99ab4fe6365a32d33fbcc95245aa0be456a79`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdbd261ff900784ddbeeb91f1f57ae786a90a768b5eadf3dd147b211f2bc50b`  
		Last Modified: Fri, 26 Jun 2026 17:54:24 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:28c285e03cdabab87ffbdf61692940646bd26ece6500faef94cef4d10f12a4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f54c943e26a32b57061a001eeb5c9ddf0281057b0d7bcdfbe5bce15cfce1ec7`

```dockerfile
```

-	Layers:
	-	`sha256:9eee0a9398985ea52f2e4891a8e34f384d1006b45866ceb9cc45871305b004d4`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 27.0 KB (27047 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.15`

```console
$ docker pull clickhouse@sha256:97e8f72ba5ea68bae106dc03c39fcd7bb0eeaa0a1fa5b3403b3ea39b2bfa3381
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.15` - linux; amd64

```console
$ docker pull clickhouse@sha256:943fdd9d6bafc53242d5ab2d2857b41f9ab8969dde7268fd33d380d03ae6e4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265176695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7ac6e6ee39b0bbd98fddd354104fc5798a4c5cf9ba560c2f074ccb02c42ecc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:43 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:43 GMT
ARG VERSION=26.3.15.4
# Fri, 26 Jun 2026 17:48:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:08 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:08 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:09 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38216c34971dba715121ac70e16c64042afc90e8ba74b1ec38601e47eb5d18da`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 7.6 MB (7555064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620737f98b2c2b28baaeb715e057822c54c3ac17763a32f2063b0944bf99ac4`  
		Last Modified: Fri, 26 Jun 2026 17:49:39 GMT  
		Size: 227.0 MB (227014894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e403cc00187b13b2ed2cb89cc5c4a942425ce2d5e42ffb06a25bb95a4bd08`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f2820a7bed2f24263b822edd2552d79c8204b27737832fe14957bda5f46dc3`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5459ef7da2345df368e41e7a127ac94d12e4c09bc30dede769c6d488977c721`  
		Last Modified: Fri, 26 Jun 2026 17:49:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9abffa579062c580b6b12358a3e0ad321124c23c7d6420577aa01ea99d7b48`  
		Last Modified: Fri, 26 Jun 2026 17:49:35 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8572df1a216f1627c9cac98c314d96fcdac6d32f361ec2e05d874da0f3d26203`  
		Last Modified: Fri, 26 Jun 2026 17:49:36 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.15` - unknown; unknown

```console
$ docker pull clickhouse@sha256:38463182a568ad43f21797199ad0a821010bab9b292010e77ef08bf6d0b351b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cddaad96ffb5d9257bbb54159f1057110220aa939ca4465b6022467f819470`

```dockerfile
```

-	Layers:
	-	`sha256:b1cba557c25f569db8a1f37e266f3981051019aef51d8698a745fc8867882b80`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 26.8 KB (26836 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.15` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:87ba1cec7d207db221a87afadbae9908b05e60c129e49123a66dc88ca4c1fd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246611660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7dcb539318c303284510428f79ae3b3ed165a4f6d1db2dd7443748d3180ec0b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:34 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:34 GMT
ARG VERSION=26.3.15.4
# Fri, 26 Jun 2026 17:53:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:54:00 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:54:00 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:54:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:54:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8a137aaa0902a87fb2cae745f866ee4a1c7908934a431dfb3a7146c032ac1`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 7.5 MB (7535269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a98ccb396d35d69ff41db54de6a8ffc02060dbcf8c5654f4b3ca3826141a21`  
		Last Modified: Fri, 26 Jun 2026 17:54:26 GMT  
		Size: 210.6 MB (210599719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ece11b79f8fe48a2dbe3cd3f13ca80e9c44e80ac2043a9a2d7641a2da83396e`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aebc0b3f40e42a3896fd2cf5777b4be657fffc9e5742514dda2f59728e83275`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44abb41eab15f74bb7625f8ffc079d7444cfead6ad401e1c29fe2f898c391f7`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fdd25aadbcfad460702922ee99ab4fe6365a32d33fbcc95245aa0be456a79`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdbd261ff900784ddbeeb91f1f57ae786a90a768b5eadf3dd147b211f2bc50b`  
		Last Modified: Fri, 26 Jun 2026 17:54:24 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.15` - unknown; unknown

```console
$ docker pull clickhouse@sha256:28c285e03cdabab87ffbdf61692940646bd26ece6500faef94cef4d10f12a4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f54c943e26a32b57061a001eeb5c9ddf0281057b0d7bcdfbe5bce15cfce1ec7`

```dockerfile
```

-	Layers:
	-	`sha256:9eee0a9398985ea52f2e4891a8e34f384d1006b45866ceb9cc45871305b004d4`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 27.0 KB (27047 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.15-jammy`

```console
$ docker pull clickhouse@sha256:97e8f72ba5ea68bae106dc03c39fcd7bb0eeaa0a1fa5b3403b3ea39b2bfa3381
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.15-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:943fdd9d6bafc53242d5ab2d2857b41f9ab8969dde7268fd33d380d03ae6e4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265176695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7ac6e6ee39b0bbd98fddd354104fc5798a4c5cf9ba560c2f074ccb02c42ecc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:43 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:43 GMT
ARG VERSION=26.3.15.4
# Fri, 26 Jun 2026 17:48:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:08 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:08 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:09 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38216c34971dba715121ac70e16c64042afc90e8ba74b1ec38601e47eb5d18da`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 7.6 MB (7555064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620737f98b2c2b28baaeb715e057822c54c3ac17763a32f2063b0944bf99ac4`  
		Last Modified: Fri, 26 Jun 2026 17:49:39 GMT  
		Size: 227.0 MB (227014894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e403cc00187b13b2ed2cb89cc5c4a942425ce2d5e42ffb06a25bb95a4bd08`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f2820a7bed2f24263b822edd2552d79c8204b27737832fe14957bda5f46dc3`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5459ef7da2345df368e41e7a127ac94d12e4c09bc30dede769c6d488977c721`  
		Last Modified: Fri, 26 Jun 2026 17:49:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9abffa579062c580b6b12358a3e0ad321124c23c7d6420577aa01ea99d7b48`  
		Last Modified: Fri, 26 Jun 2026 17:49:35 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8572df1a216f1627c9cac98c314d96fcdac6d32f361ec2e05d874da0f3d26203`  
		Last Modified: Fri, 26 Jun 2026 17:49:36 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.15-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:38463182a568ad43f21797199ad0a821010bab9b292010e77ef08bf6d0b351b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cddaad96ffb5d9257bbb54159f1057110220aa939ca4465b6022467f819470`

```dockerfile
```

-	Layers:
	-	`sha256:b1cba557c25f569db8a1f37e266f3981051019aef51d8698a745fc8867882b80`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 26.8 KB (26836 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.15-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:87ba1cec7d207db221a87afadbae9908b05e60c129e49123a66dc88ca4c1fd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246611660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7dcb539318c303284510428f79ae3b3ed165a4f6d1db2dd7443748d3180ec0b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:34 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:34 GMT
ARG VERSION=26.3.15.4
# Fri, 26 Jun 2026 17:53:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:54:00 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:54:00 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:54:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:54:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8a137aaa0902a87fb2cae745f866ee4a1c7908934a431dfb3a7146c032ac1`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 7.5 MB (7535269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a98ccb396d35d69ff41db54de6a8ffc02060dbcf8c5654f4b3ca3826141a21`  
		Last Modified: Fri, 26 Jun 2026 17:54:26 GMT  
		Size: 210.6 MB (210599719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ece11b79f8fe48a2dbe3cd3f13ca80e9c44e80ac2043a9a2d7641a2da83396e`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aebc0b3f40e42a3896fd2cf5777b4be657fffc9e5742514dda2f59728e83275`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44abb41eab15f74bb7625f8ffc079d7444cfead6ad401e1c29fe2f898c391f7`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fdd25aadbcfad460702922ee99ab4fe6365a32d33fbcc95245aa0be456a79`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdbd261ff900784ddbeeb91f1f57ae786a90a768b5eadf3dd147b211f2bc50b`  
		Last Modified: Fri, 26 Jun 2026 17:54:24 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.15-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:28c285e03cdabab87ffbdf61692940646bd26ece6500faef94cef4d10f12a4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f54c943e26a32b57061a001eeb5c9ddf0281057b0d7bcdfbe5bce15cfce1ec7`

```dockerfile
```

-	Layers:
	-	`sha256:9eee0a9398985ea52f2e4891a8e34f384d1006b45866ceb9cc45871305b004d4`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 27.0 KB (27047 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.15.4`

```console
$ docker pull clickhouse@sha256:97e8f72ba5ea68bae106dc03c39fcd7bb0eeaa0a1fa5b3403b3ea39b2bfa3381
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.15.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:943fdd9d6bafc53242d5ab2d2857b41f9ab8969dde7268fd33d380d03ae6e4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265176695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7ac6e6ee39b0bbd98fddd354104fc5798a4c5cf9ba560c2f074ccb02c42ecc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:43 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:43 GMT
ARG VERSION=26.3.15.4
# Fri, 26 Jun 2026 17:48:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:08 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:08 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:09 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38216c34971dba715121ac70e16c64042afc90e8ba74b1ec38601e47eb5d18da`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 7.6 MB (7555064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620737f98b2c2b28baaeb715e057822c54c3ac17763a32f2063b0944bf99ac4`  
		Last Modified: Fri, 26 Jun 2026 17:49:39 GMT  
		Size: 227.0 MB (227014894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e403cc00187b13b2ed2cb89cc5c4a942425ce2d5e42ffb06a25bb95a4bd08`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f2820a7bed2f24263b822edd2552d79c8204b27737832fe14957bda5f46dc3`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5459ef7da2345df368e41e7a127ac94d12e4c09bc30dede769c6d488977c721`  
		Last Modified: Fri, 26 Jun 2026 17:49:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9abffa579062c580b6b12358a3e0ad321124c23c7d6420577aa01ea99d7b48`  
		Last Modified: Fri, 26 Jun 2026 17:49:35 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8572df1a216f1627c9cac98c314d96fcdac6d32f361ec2e05d874da0f3d26203`  
		Last Modified: Fri, 26 Jun 2026 17:49:36 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.15.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:38463182a568ad43f21797199ad0a821010bab9b292010e77ef08bf6d0b351b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cddaad96ffb5d9257bbb54159f1057110220aa939ca4465b6022467f819470`

```dockerfile
```

-	Layers:
	-	`sha256:b1cba557c25f569db8a1f37e266f3981051019aef51d8698a745fc8867882b80`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 26.8 KB (26836 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.15.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:87ba1cec7d207db221a87afadbae9908b05e60c129e49123a66dc88ca4c1fd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246611660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7dcb539318c303284510428f79ae3b3ed165a4f6d1db2dd7443748d3180ec0b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:34 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:34 GMT
ARG VERSION=26.3.15.4
# Fri, 26 Jun 2026 17:53:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:54:00 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:54:00 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:54:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:54:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8a137aaa0902a87fb2cae745f866ee4a1c7908934a431dfb3a7146c032ac1`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 7.5 MB (7535269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a98ccb396d35d69ff41db54de6a8ffc02060dbcf8c5654f4b3ca3826141a21`  
		Last Modified: Fri, 26 Jun 2026 17:54:26 GMT  
		Size: 210.6 MB (210599719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ece11b79f8fe48a2dbe3cd3f13ca80e9c44e80ac2043a9a2d7641a2da83396e`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aebc0b3f40e42a3896fd2cf5777b4be657fffc9e5742514dda2f59728e83275`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44abb41eab15f74bb7625f8ffc079d7444cfead6ad401e1c29fe2f898c391f7`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fdd25aadbcfad460702922ee99ab4fe6365a32d33fbcc95245aa0be456a79`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdbd261ff900784ddbeeb91f1f57ae786a90a768b5eadf3dd147b211f2bc50b`  
		Last Modified: Fri, 26 Jun 2026 17:54:24 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.15.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:28c285e03cdabab87ffbdf61692940646bd26ece6500faef94cef4d10f12a4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f54c943e26a32b57061a001eeb5c9ddf0281057b0d7bcdfbe5bce15cfce1ec7`

```dockerfile
```

-	Layers:
	-	`sha256:9eee0a9398985ea52f2e4891a8e34f384d1006b45866ceb9cc45871305b004d4`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 27.0 KB (27047 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.15.4-jammy`

```console
$ docker pull clickhouse@sha256:97e8f72ba5ea68bae106dc03c39fcd7bb0eeaa0a1fa5b3403b3ea39b2bfa3381
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3.15.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:943fdd9d6bafc53242d5ab2d2857b41f9ab8969dde7268fd33d380d03ae6e4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265176695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7ac6e6ee39b0bbd98fddd354104fc5798a4c5cf9ba560c2f074ccb02c42ecc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:43 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:43 GMT
ARG VERSION=26.3.15.4
# Fri, 26 Jun 2026 17:48:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:08 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:08 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:09 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38216c34971dba715121ac70e16c64042afc90e8ba74b1ec38601e47eb5d18da`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 7.6 MB (7555064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620737f98b2c2b28baaeb715e057822c54c3ac17763a32f2063b0944bf99ac4`  
		Last Modified: Fri, 26 Jun 2026 17:49:39 GMT  
		Size: 227.0 MB (227014894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e403cc00187b13b2ed2cb89cc5c4a942425ce2d5e42ffb06a25bb95a4bd08`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f2820a7bed2f24263b822edd2552d79c8204b27737832fe14957bda5f46dc3`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5459ef7da2345df368e41e7a127ac94d12e4c09bc30dede769c6d488977c721`  
		Last Modified: Fri, 26 Jun 2026 17:49:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9abffa579062c580b6b12358a3e0ad321124c23c7d6420577aa01ea99d7b48`  
		Last Modified: Fri, 26 Jun 2026 17:49:35 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8572df1a216f1627c9cac98c314d96fcdac6d32f361ec2e05d874da0f3d26203`  
		Last Modified: Fri, 26 Jun 2026 17:49:36 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.15.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:38463182a568ad43f21797199ad0a821010bab9b292010e77ef08bf6d0b351b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cddaad96ffb5d9257bbb54159f1057110220aa939ca4465b6022467f819470`

```dockerfile
```

-	Layers:
	-	`sha256:b1cba557c25f569db8a1f37e266f3981051019aef51d8698a745fc8867882b80`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 26.8 KB (26836 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3.15.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:87ba1cec7d207db221a87afadbae9908b05e60c129e49123a66dc88ca4c1fd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246611660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7dcb539318c303284510428f79ae3b3ed165a4f6d1db2dd7443748d3180ec0b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:34 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:34 GMT
ARG VERSION=26.3.15.4
# Fri, 26 Jun 2026 17:53:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:54:00 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:54:00 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:54:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:54:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8a137aaa0902a87fb2cae745f866ee4a1c7908934a431dfb3a7146c032ac1`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 7.5 MB (7535269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a98ccb396d35d69ff41db54de6a8ffc02060dbcf8c5654f4b3ca3826141a21`  
		Last Modified: Fri, 26 Jun 2026 17:54:26 GMT  
		Size: 210.6 MB (210599719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ece11b79f8fe48a2dbe3cd3f13ca80e9c44e80ac2043a9a2d7641a2da83396e`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aebc0b3f40e42a3896fd2cf5777b4be657fffc9e5742514dda2f59728e83275`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44abb41eab15f74bb7625f8ffc079d7444cfead6ad401e1c29fe2f898c391f7`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fdd25aadbcfad460702922ee99ab4fe6365a32d33fbcc95245aa0be456a79`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdbd261ff900784ddbeeb91f1f57ae786a90a768b5eadf3dd147b211f2bc50b`  
		Last Modified: Fri, 26 Jun 2026 17:54:24 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3.15.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:28c285e03cdabab87ffbdf61692940646bd26ece6500faef94cef4d10f12a4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f54c943e26a32b57061a001eeb5c9ddf0281057b0d7bcdfbe5bce15cfce1ec7`

```dockerfile
```

-	Layers:
	-	`sha256:9eee0a9398985ea52f2e4891a8e34f384d1006b45866ceb9cc45871305b004d4`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 27.0 KB (27047 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4`

```console
$ docker pull clickhouse@sha256:5490a9b2c0f53ec0eeab084778885be482301e9b2b0f217d68484312f00bad1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:bc9fe1e236dc2e9611b28d916797ce7a7881593b32e1d6ebcb284c30ed60630c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257145112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fb3da541cf9be2b4c1694411c41eaa766717280fd2286c61c198145058b823`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:38 GMT
ARG VERSION=26.4.4.38
# Fri, 26 Jun 2026 17:48:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:04 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7520498bf1735c3fcd9e01aa9cdc9b336be160ddc707cbc10a1a3a08ed8efc32`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 7.6 MB (7555115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec015b555c14c78bad7043f7110ae91ea31e0222f908802ebba50874062751c`  
		Last Modified: Fri, 26 Jun 2026 17:49:32 GMT  
		Size: 219.0 MB (218983264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81ff442279c8c49ea99079aef633ff47deadceab8d81882fc29b786d0d67017`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc766a86fae68346afffa13a12e3ecf1478e8b3d72accc7fa7456e0b7e6e2a52`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c105726107bd198b01f9d5de39f0acbe64862791de4703d60019ae3d81329de`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7a724a880ca477e200c7c32259a3d3bf6f679b59b8c63403b7f0b73097ff58`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c8a620a07316711ffe7b12fdee2b774637d08a5f4b19f95443f2f630970421`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9ed23fda52c07ad533c37407b51cd3c6a1b0296b1455fd9f520cca4202ee2abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6749f6018d1d7b0f449faba2497f8c851250c1268f780f4653d3be063621ceb`

```dockerfile
```

-	Layers:
	-	`sha256:2f12dcdff7d67111082abf70610729c539259639b23dd47318af1fc1113c1e3e`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:fd70c17d1a37dd31fcf5db990e6e1c6c3db3fa3cd084d50efaa71652f3638763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240946391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62dcbc9fd653524abd00ea404aaa20c5b78390d623bbef6ab4cb3c04d60618a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:35 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:35 GMT
ARG VERSION=26.4.4.38
# Fri, 26 Jun 2026 17:53:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:54:01 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:54:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:54:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:54:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:54:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8cf9aa9c7e23b151e904056ed590c45f7669c0134cb653d11fa99160db2b9f`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 7.5 MB (7535243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a060b90545607909c92e1640e3ccb3361aa5980e7d421191dcfa964ef5f82e`  
		Last Modified: Fri, 26 Jun 2026 17:54:26 GMT  
		Size: 204.9 MB (204934476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e224ad6a1589935bebbaf5b731f3c6cddd8131a4a34a65853e0554421b6753d2`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154c53a39b59d7a3e2b55bd79aba24e19a05c372ad9b96de5d95bd791a02361a`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810b8ce0297a4ab00c6cee61962a664ef815d15b2260463795af724204dd662f`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9168a705ad840ba9bfe1be3ea7e25ca2da468d5116b8df899fa049e88d890fb`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6ebc2955526fb57dbcbadcd96fca459120c49e3a88e5e2fa1274749c8485c8`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c841314bb5557aab25637a6e21776ee072184e27b30ab697d11ee2b33ccb1950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab97eaa4ccb830884072cd19b990643f1c5c0654e0e5bbc6cb2ab7b5c049513`

```dockerfile
```

-	Layers:
	-	`sha256:457a7024cc92effd0eb2907c8adc71de61c40db42b2f4815eedd4a259fbf0e65`  
		Last Modified: Fri, 26 Jun 2026 17:54:20 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4-jammy`

```console
$ docker pull clickhouse@sha256:5490a9b2c0f53ec0eeab084778885be482301e9b2b0f217d68484312f00bad1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:bc9fe1e236dc2e9611b28d916797ce7a7881593b32e1d6ebcb284c30ed60630c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257145112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fb3da541cf9be2b4c1694411c41eaa766717280fd2286c61c198145058b823`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:38 GMT
ARG VERSION=26.4.4.38
# Fri, 26 Jun 2026 17:48:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:04 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7520498bf1735c3fcd9e01aa9cdc9b336be160ddc707cbc10a1a3a08ed8efc32`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 7.6 MB (7555115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec015b555c14c78bad7043f7110ae91ea31e0222f908802ebba50874062751c`  
		Last Modified: Fri, 26 Jun 2026 17:49:32 GMT  
		Size: 219.0 MB (218983264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81ff442279c8c49ea99079aef633ff47deadceab8d81882fc29b786d0d67017`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc766a86fae68346afffa13a12e3ecf1478e8b3d72accc7fa7456e0b7e6e2a52`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c105726107bd198b01f9d5de39f0acbe64862791de4703d60019ae3d81329de`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7a724a880ca477e200c7c32259a3d3bf6f679b59b8c63403b7f0b73097ff58`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c8a620a07316711ffe7b12fdee2b774637d08a5f4b19f95443f2f630970421`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9ed23fda52c07ad533c37407b51cd3c6a1b0296b1455fd9f520cca4202ee2abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6749f6018d1d7b0f449faba2497f8c851250c1268f780f4653d3be063621ceb`

```dockerfile
```

-	Layers:
	-	`sha256:2f12dcdff7d67111082abf70610729c539259639b23dd47318af1fc1113c1e3e`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:fd70c17d1a37dd31fcf5db990e6e1c6c3db3fa3cd084d50efaa71652f3638763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240946391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62dcbc9fd653524abd00ea404aaa20c5b78390d623bbef6ab4cb3c04d60618a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:35 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:35 GMT
ARG VERSION=26.4.4.38
# Fri, 26 Jun 2026 17:53:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:54:01 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:54:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:54:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:54:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:54:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8cf9aa9c7e23b151e904056ed590c45f7669c0134cb653d11fa99160db2b9f`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 7.5 MB (7535243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a060b90545607909c92e1640e3ccb3361aa5980e7d421191dcfa964ef5f82e`  
		Last Modified: Fri, 26 Jun 2026 17:54:26 GMT  
		Size: 204.9 MB (204934476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e224ad6a1589935bebbaf5b731f3c6cddd8131a4a34a65853e0554421b6753d2`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154c53a39b59d7a3e2b55bd79aba24e19a05c372ad9b96de5d95bd791a02361a`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810b8ce0297a4ab00c6cee61962a664ef815d15b2260463795af724204dd662f`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9168a705ad840ba9bfe1be3ea7e25ca2da468d5116b8df899fa049e88d890fb`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6ebc2955526fb57dbcbadcd96fca459120c49e3a88e5e2fa1274749c8485c8`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c841314bb5557aab25637a6e21776ee072184e27b30ab697d11ee2b33ccb1950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab97eaa4ccb830884072cd19b990643f1c5c0654e0e5bbc6cb2ab7b5c049513`

```dockerfile
```

-	Layers:
	-	`sha256:457a7024cc92effd0eb2907c8adc71de61c40db42b2f4815eedd4a259fbf0e65`  
		Last Modified: Fri, 26 Jun 2026 17:54:20 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4.4`

```console
$ docker pull clickhouse@sha256:5490a9b2c0f53ec0eeab084778885be482301e9b2b0f217d68484312f00bad1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:bc9fe1e236dc2e9611b28d916797ce7a7881593b32e1d6ebcb284c30ed60630c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257145112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fb3da541cf9be2b4c1694411c41eaa766717280fd2286c61c198145058b823`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:38 GMT
ARG VERSION=26.4.4.38
# Fri, 26 Jun 2026 17:48:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:04 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7520498bf1735c3fcd9e01aa9cdc9b336be160ddc707cbc10a1a3a08ed8efc32`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 7.6 MB (7555115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec015b555c14c78bad7043f7110ae91ea31e0222f908802ebba50874062751c`  
		Last Modified: Fri, 26 Jun 2026 17:49:32 GMT  
		Size: 219.0 MB (218983264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81ff442279c8c49ea99079aef633ff47deadceab8d81882fc29b786d0d67017`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc766a86fae68346afffa13a12e3ecf1478e8b3d72accc7fa7456e0b7e6e2a52`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c105726107bd198b01f9d5de39f0acbe64862791de4703d60019ae3d81329de`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7a724a880ca477e200c7c32259a3d3bf6f679b59b8c63403b7f0b73097ff58`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c8a620a07316711ffe7b12fdee2b774637d08a5f4b19f95443f2f630970421`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9ed23fda52c07ad533c37407b51cd3c6a1b0296b1455fd9f520cca4202ee2abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6749f6018d1d7b0f449faba2497f8c851250c1268f780f4653d3be063621ceb`

```dockerfile
```

-	Layers:
	-	`sha256:2f12dcdff7d67111082abf70610729c539259639b23dd47318af1fc1113c1e3e`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:fd70c17d1a37dd31fcf5db990e6e1c6c3db3fa3cd084d50efaa71652f3638763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240946391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62dcbc9fd653524abd00ea404aaa20c5b78390d623bbef6ab4cb3c04d60618a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:35 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:35 GMT
ARG VERSION=26.4.4.38
# Fri, 26 Jun 2026 17:53:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:54:01 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:54:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:54:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:54:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:54:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8cf9aa9c7e23b151e904056ed590c45f7669c0134cb653d11fa99160db2b9f`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 7.5 MB (7535243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a060b90545607909c92e1640e3ccb3361aa5980e7d421191dcfa964ef5f82e`  
		Last Modified: Fri, 26 Jun 2026 17:54:26 GMT  
		Size: 204.9 MB (204934476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e224ad6a1589935bebbaf5b731f3c6cddd8131a4a34a65853e0554421b6753d2`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154c53a39b59d7a3e2b55bd79aba24e19a05c372ad9b96de5d95bd791a02361a`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810b8ce0297a4ab00c6cee61962a664ef815d15b2260463795af724204dd662f`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9168a705ad840ba9bfe1be3ea7e25ca2da468d5116b8df899fa049e88d890fb`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6ebc2955526fb57dbcbadcd96fca459120c49e3a88e5e2fa1274749c8485c8`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c841314bb5557aab25637a6e21776ee072184e27b30ab697d11ee2b33ccb1950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab97eaa4ccb830884072cd19b990643f1c5c0654e0e5bbc6cb2ab7b5c049513`

```dockerfile
```

-	Layers:
	-	`sha256:457a7024cc92effd0eb2907c8adc71de61c40db42b2f4815eedd4a259fbf0e65`  
		Last Modified: Fri, 26 Jun 2026 17:54:20 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4.4-jammy`

```console
$ docker pull clickhouse@sha256:5490a9b2c0f53ec0eeab084778885be482301e9b2b0f217d68484312f00bad1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:bc9fe1e236dc2e9611b28d916797ce7a7881593b32e1d6ebcb284c30ed60630c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257145112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fb3da541cf9be2b4c1694411c41eaa766717280fd2286c61c198145058b823`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:38 GMT
ARG VERSION=26.4.4.38
# Fri, 26 Jun 2026 17:48:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:04 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7520498bf1735c3fcd9e01aa9cdc9b336be160ddc707cbc10a1a3a08ed8efc32`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 7.6 MB (7555115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec015b555c14c78bad7043f7110ae91ea31e0222f908802ebba50874062751c`  
		Last Modified: Fri, 26 Jun 2026 17:49:32 GMT  
		Size: 219.0 MB (218983264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81ff442279c8c49ea99079aef633ff47deadceab8d81882fc29b786d0d67017`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc766a86fae68346afffa13a12e3ecf1478e8b3d72accc7fa7456e0b7e6e2a52`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c105726107bd198b01f9d5de39f0acbe64862791de4703d60019ae3d81329de`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7a724a880ca477e200c7c32259a3d3bf6f679b59b8c63403b7f0b73097ff58`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c8a620a07316711ffe7b12fdee2b774637d08a5f4b19f95443f2f630970421`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9ed23fda52c07ad533c37407b51cd3c6a1b0296b1455fd9f520cca4202ee2abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6749f6018d1d7b0f449faba2497f8c851250c1268f780f4653d3be063621ceb`

```dockerfile
```

-	Layers:
	-	`sha256:2f12dcdff7d67111082abf70610729c539259639b23dd47318af1fc1113c1e3e`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:fd70c17d1a37dd31fcf5db990e6e1c6c3db3fa3cd084d50efaa71652f3638763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240946391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62dcbc9fd653524abd00ea404aaa20c5b78390d623bbef6ab4cb3c04d60618a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:35 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:35 GMT
ARG VERSION=26.4.4.38
# Fri, 26 Jun 2026 17:53:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:54:01 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:54:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:54:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:54:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:54:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8cf9aa9c7e23b151e904056ed590c45f7669c0134cb653d11fa99160db2b9f`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 7.5 MB (7535243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a060b90545607909c92e1640e3ccb3361aa5980e7d421191dcfa964ef5f82e`  
		Last Modified: Fri, 26 Jun 2026 17:54:26 GMT  
		Size: 204.9 MB (204934476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e224ad6a1589935bebbaf5b731f3c6cddd8131a4a34a65853e0554421b6753d2`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154c53a39b59d7a3e2b55bd79aba24e19a05c372ad9b96de5d95bd791a02361a`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810b8ce0297a4ab00c6cee61962a664ef815d15b2260463795af724204dd662f`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9168a705ad840ba9bfe1be3ea7e25ca2da468d5116b8df899fa049e88d890fb`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6ebc2955526fb57dbcbadcd96fca459120c49e3a88e5e2fa1274749c8485c8`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c841314bb5557aab25637a6e21776ee072184e27b30ab697d11ee2b33ccb1950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab97eaa4ccb830884072cd19b990643f1c5c0654e0e5bbc6cb2ab7b5c049513`

```dockerfile
```

-	Layers:
	-	`sha256:457a7024cc92effd0eb2907c8adc71de61c40db42b2f4815eedd4a259fbf0e65`  
		Last Modified: Fri, 26 Jun 2026 17:54:20 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4.4.38`

```console
$ docker pull clickhouse@sha256:5490a9b2c0f53ec0eeab084778885be482301e9b2b0f217d68484312f00bad1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4.4.38` - linux; amd64

```console
$ docker pull clickhouse@sha256:bc9fe1e236dc2e9611b28d916797ce7a7881593b32e1d6ebcb284c30ed60630c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257145112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fb3da541cf9be2b4c1694411c41eaa766717280fd2286c61c198145058b823`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:38 GMT
ARG VERSION=26.4.4.38
# Fri, 26 Jun 2026 17:48:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:04 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7520498bf1735c3fcd9e01aa9cdc9b336be160ddc707cbc10a1a3a08ed8efc32`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 7.6 MB (7555115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec015b555c14c78bad7043f7110ae91ea31e0222f908802ebba50874062751c`  
		Last Modified: Fri, 26 Jun 2026 17:49:32 GMT  
		Size: 219.0 MB (218983264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81ff442279c8c49ea99079aef633ff47deadceab8d81882fc29b786d0d67017`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc766a86fae68346afffa13a12e3ecf1478e8b3d72accc7fa7456e0b7e6e2a52`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c105726107bd198b01f9d5de39f0acbe64862791de4703d60019ae3d81329de`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7a724a880ca477e200c7c32259a3d3bf6f679b59b8c63403b7f0b73097ff58`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c8a620a07316711ffe7b12fdee2b774637d08a5f4b19f95443f2f630970421`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.4.38` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9ed23fda52c07ad533c37407b51cd3c6a1b0296b1455fd9f520cca4202ee2abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6749f6018d1d7b0f449faba2497f8c851250c1268f780f4653d3be063621ceb`

```dockerfile
```

-	Layers:
	-	`sha256:2f12dcdff7d67111082abf70610729c539259639b23dd47318af1fc1113c1e3e`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4.4.38` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:fd70c17d1a37dd31fcf5db990e6e1c6c3db3fa3cd084d50efaa71652f3638763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240946391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62dcbc9fd653524abd00ea404aaa20c5b78390d623bbef6ab4cb3c04d60618a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:35 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:35 GMT
ARG VERSION=26.4.4.38
# Fri, 26 Jun 2026 17:53:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:54:01 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:54:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:54:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:54:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:54:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8cf9aa9c7e23b151e904056ed590c45f7669c0134cb653d11fa99160db2b9f`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 7.5 MB (7535243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a060b90545607909c92e1640e3ccb3361aa5980e7d421191dcfa964ef5f82e`  
		Last Modified: Fri, 26 Jun 2026 17:54:26 GMT  
		Size: 204.9 MB (204934476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e224ad6a1589935bebbaf5b731f3c6cddd8131a4a34a65853e0554421b6753d2`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154c53a39b59d7a3e2b55bd79aba24e19a05c372ad9b96de5d95bd791a02361a`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810b8ce0297a4ab00c6cee61962a664ef815d15b2260463795af724204dd662f`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9168a705ad840ba9bfe1be3ea7e25ca2da468d5116b8df899fa049e88d890fb`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6ebc2955526fb57dbcbadcd96fca459120c49e3a88e5e2fa1274749c8485c8`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.4.38` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c841314bb5557aab25637a6e21776ee072184e27b30ab697d11ee2b33ccb1950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab97eaa4ccb830884072cd19b990643f1c5c0654e0e5bbc6cb2ab7b5c049513`

```dockerfile
```

-	Layers:
	-	`sha256:457a7024cc92effd0eb2907c8adc71de61c40db42b2f4815eedd4a259fbf0e65`  
		Last Modified: Fri, 26 Jun 2026 17:54:20 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4.4.38-jammy`

```console
$ docker pull clickhouse@sha256:5490a9b2c0f53ec0eeab084778885be482301e9b2b0f217d68484312f00bad1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4.4.38-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:bc9fe1e236dc2e9611b28d916797ce7a7881593b32e1d6ebcb284c30ed60630c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257145112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fb3da541cf9be2b4c1694411c41eaa766717280fd2286c61c198145058b823`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:38 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:38 GMT
ARG VERSION=26.4.4.38
# Fri, 26 Jun 2026 17:48:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:04 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:04 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:04 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:04 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7520498bf1735c3fcd9e01aa9cdc9b336be160ddc707cbc10a1a3a08ed8efc32`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 7.6 MB (7555115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec015b555c14c78bad7043f7110ae91ea31e0222f908802ebba50874062751c`  
		Last Modified: Fri, 26 Jun 2026 17:49:32 GMT  
		Size: 219.0 MB (218983264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81ff442279c8c49ea99079aef633ff47deadceab8d81882fc29b786d0d67017`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc766a86fae68346afffa13a12e3ecf1478e8b3d72accc7fa7456e0b7e6e2a52`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c105726107bd198b01f9d5de39f0acbe64862791de4703d60019ae3d81329de`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7a724a880ca477e200c7c32259a3d3bf6f679b59b8c63403b7f0b73097ff58`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5c8a620a07316711ffe7b12fdee2b774637d08a5f4b19f95443f2f630970421`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.4.38-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9ed23fda52c07ad533c37407b51cd3c6a1b0296b1455fd9f520cca4202ee2abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6749f6018d1d7b0f449faba2497f8c851250c1268f780f4653d3be063621ceb`

```dockerfile
```

-	Layers:
	-	`sha256:2f12dcdff7d67111082abf70610729c539259639b23dd47318af1fc1113c1e3e`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4.4.38-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:fd70c17d1a37dd31fcf5db990e6e1c6c3db3fa3cd084d50efaa71652f3638763
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240946391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62dcbc9fd653524abd00ea404aaa20c5b78390d623bbef6ab4cb3c04d60618a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:35 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:35 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:35 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:35 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:35 GMT
ARG VERSION=26.4.4.38
# Fri, 26 Jun 2026 17:53:35 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:54:01 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:54:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.4.38 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:54:01 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:54:01 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:54:01 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:54:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8cf9aa9c7e23b151e904056ed590c45f7669c0134cb653d11fa99160db2b9f`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 7.5 MB (7535243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a060b90545607909c92e1640e3ccb3361aa5980e7d421191dcfa964ef5f82e`  
		Last Modified: Fri, 26 Jun 2026 17:54:26 GMT  
		Size: 204.9 MB (204934476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e224ad6a1589935bebbaf5b731f3c6cddd8131a4a34a65853e0554421b6753d2`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154c53a39b59d7a3e2b55bd79aba24e19a05c372ad9b96de5d95bd791a02361a`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:810b8ce0297a4ab00c6cee61962a664ef815d15b2260463795af724204dd662f`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9168a705ad840ba9bfe1be3ea7e25ca2da468d5116b8df899fa049e88d890fb`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc6ebc2955526fb57dbcbadcd96fca459120c49e3a88e5e2fa1274749c8485c8`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.4.38-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c841314bb5557aab25637a6e21776ee072184e27b30ab697d11ee2b33ccb1950
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ab97eaa4ccb830884072cd19b990643f1c5c0654e0e5bbc6cb2ab7b5c049513`

```dockerfile
```

-	Layers:
	-	`sha256:457a7024cc92effd0eb2907c8adc71de61c40db42b2f4815eedd4a259fbf0e65`  
		Last Modified: Fri, 26 Jun 2026 17:54:20 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.5`

```console
$ docker pull clickhouse@sha256:7e74f0a4c13733f45f11a783cdfe712273220f37b4bc2e66c6389e91427a6770
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:53231f9d8910f2bf8023a5c12f403da171dc32886bf598b80408fadf639ce14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261391816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1382d83a1461d18a2e2558f7b4b988133ab89835c47f382a0e2797dd32a04d78`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:36 GMT
ARG VERSION=26.5.3.52
# Fri, 26 Jun 2026 17:48:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:01 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:01 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:02 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:02 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463352a3264930f02f9ffb69e200c163bf1cc1843bbda180fad3999231973014`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 7.6 MB (7555039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a544d79e69644dcc071eeda3d5c34c6a6fdb9b877040bf9a580fe2b2c004ae`  
		Last Modified: Fri, 26 Jun 2026 17:49:32 GMT  
		Size: 223.2 MB (223230047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed1281811609cac707694dbaacb26040c5ce88cf9b865a46edb76d93cdc1ca7`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d0b421df4edf934fff42d42f5005fc571173b1be57c741c4f05d132f924974`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69f9c494f5efe09fed621e0861b832ae7c9c971de0bef6d3d6b4b0ca121dddc`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c164df2d361d4edb0407a50f3815eb3b24e36963e33b6f8b36847be91b41f49`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0d6c45240b715b7ed32cffb574770793646da4a5702bc20c2470a9f8ab83ec`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:00c1a376173c0a75daf1eb98ec9b8df7f7fc96fd18ca0707faf47fd07645af86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7e521b77498aab37807ddf34e5e17e391f0ec157c224e8f68de46b38940b49`

```dockerfile
```

-	Layers:
	-	`sha256:23c8667820bb59f98de2399ca094a9f7c22b568742724ba073b0808d30c595ba`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0db55768f09d1439f8aa0cde4dfe62d29851e97d2b579cf58806d5539ce4864e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247200542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592b6d055dc5d1c5d3a7907c39d41941f9097e55edd6771bf33ee34294353b35`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:27 GMT
ARG VERSION=26.5.3.52
# Fri, 26 Jun 2026 17:53:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:53:54 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:53:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:53:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:53:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:53:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc33f9b57fa7d57e87efad20c03ca51da3bff4ea4d0e740af9c87a4217d6b36b`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 7.5 MB (7535259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046eab11a99682a8dde9fe257a433d95a2fd6411d55a2eccd737a6ceaa24be1b`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 211.2 MB (211188611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f71f0c7d8f36695c089f35d2a6e92610e1585547da892a53fd3adea5a3aec74`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972f876f872c67d92f6843b7e9cb8e93bc1470e77d84539685f3ff1b878e09a1`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50065ee90e073f2044341ddd5b2f22c28e778122069519d147db4b68c13f5491`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca50da3dd824df56605558094758fdd85617c31c148ec2b282210f19da1d5984`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c503afdb6351f35485a264efde5fb2da225c10dff23e8b3c3de460346b071`  
		Last Modified: Fri, 26 Jun 2026 17:54:18 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:776f7fd79de9880ffdf1c92b336aad3d623135786645de34940af232c09d87d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63231a5509729c05796cbdf97d63db79639aab1a7f87f39efbf30136043e7bb`

```dockerfile
```

-	Layers:
	-	`sha256:8f7fba1e89b6dcb3b052445fca6a8b92bf5f7ed57847c78ad519f8b268722147`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.5-jammy`

```console
$ docker pull clickhouse@sha256:7e74f0a4c13733f45f11a783cdfe712273220f37b4bc2e66c6389e91427a6770
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:53231f9d8910f2bf8023a5c12f403da171dc32886bf598b80408fadf639ce14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261391816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1382d83a1461d18a2e2558f7b4b988133ab89835c47f382a0e2797dd32a04d78`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:36 GMT
ARG VERSION=26.5.3.52
# Fri, 26 Jun 2026 17:48:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:01 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:01 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:02 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:02 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463352a3264930f02f9ffb69e200c163bf1cc1843bbda180fad3999231973014`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 7.6 MB (7555039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a544d79e69644dcc071eeda3d5c34c6a6fdb9b877040bf9a580fe2b2c004ae`  
		Last Modified: Fri, 26 Jun 2026 17:49:32 GMT  
		Size: 223.2 MB (223230047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed1281811609cac707694dbaacb26040c5ce88cf9b865a46edb76d93cdc1ca7`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d0b421df4edf934fff42d42f5005fc571173b1be57c741c4f05d132f924974`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69f9c494f5efe09fed621e0861b832ae7c9c971de0bef6d3d6b4b0ca121dddc`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c164df2d361d4edb0407a50f3815eb3b24e36963e33b6f8b36847be91b41f49`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0d6c45240b715b7ed32cffb574770793646da4a5702bc20c2470a9f8ab83ec`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:00c1a376173c0a75daf1eb98ec9b8df7f7fc96fd18ca0707faf47fd07645af86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7e521b77498aab37807ddf34e5e17e391f0ec157c224e8f68de46b38940b49`

```dockerfile
```

-	Layers:
	-	`sha256:23c8667820bb59f98de2399ca094a9f7c22b568742724ba073b0808d30c595ba`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0db55768f09d1439f8aa0cde4dfe62d29851e97d2b579cf58806d5539ce4864e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247200542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592b6d055dc5d1c5d3a7907c39d41941f9097e55edd6771bf33ee34294353b35`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:27 GMT
ARG VERSION=26.5.3.52
# Fri, 26 Jun 2026 17:53:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:53:54 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:53:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:53:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:53:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:53:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc33f9b57fa7d57e87efad20c03ca51da3bff4ea4d0e740af9c87a4217d6b36b`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 7.5 MB (7535259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046eab11a99682a8dde9fe257a433d95a2fd6411d55a2eccd737a6ceaa24be1b`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 211.2 MB (211188611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f71f0c7d8f36695c089f35d2a6e92610e1585547da892a53fd3adea5a3aec74`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972f876f872c67d92f6843b7e9cb8e93bc1470e77d84539685f3ff1b878e09a1`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50065ee90e073f2044341ddd5b2f22c28e778122069519d147db4b68c13f5491`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca50da3dd824df56605558094758fdd85617c31c148ec2b282210f19da1d5984`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c503afdb6351f35485a264efde5fb2da225c10dff23e8b3c3de460346b071`  
		Last Modified: Fri, 26 Jun 2026 17:54:18 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:776f7fd79de9880ffdf1c92b336aad3d623135786645de34940af232c09d87d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63231a5509729c05796cbdf97d63db79639aab1a7f87f39efbf30136043e7bb`

```dockerfile
```

-	Layers:
	-	`sha256:8f7fba1e89b6dcb3b052445fca6a8b92bf5f7ed57847c78ad519f8b268722147`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.5.3`

```console
$ docker pull clickhouse@sha256:7e74f0a4c13733f45f11a783cdfe712273220f37b4bc2e66c6389e91427a6770
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.5.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:53231f9d8910f2bf8023a5c12f403da171dc32886bf598b80408fadf639ce14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261391816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1382d83a1461d18a2e2558f7b4b988133ab89835c47f382a0e2797dd32a04d78`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:36 GMT
ARG VERSION=26.5.3.52
# Fri, 26 Jun 2026 17:48:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:01 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:01 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:02 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:02 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463352a3264930f02f9ffb69e200c163bf1cc1843bbda180fad3999231973014`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 7.6 MB (7555039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a544d79e69644dcc071eeda3d5c34c6a6fdb9b877040bf9a580fe2b2c004ae`  
		Last Modified: Fri, 26 Jun 2026 17:49:32 GMT  
		Size: 223.2 MB (223230047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed1281811609cac707694dbaacb26040c5ce88cf9b865a46edb76d93cdc1ca7`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d0b421df4edf934fff42d42f5005fc571173b1be57c741c4f05d132f924974`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69f9c494f5efe09fed621e0861b832ae7c9c971de0bef6d3d6b4b0ca121dddc`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c164df2d361d4edb0407a50f3815eb3b24e36963e33b6f8b36847be91b41f49`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0d6c45240b715b7ed32cffb574770793646da4a5702bc20c2470a9f8ab83ec`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:00c1a376173c0a75daf1eb98ec9b8df7f7fc96fd18ca0707faf47fd07645af86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7e521b77498aab37807ddf34e5e17e391f0ec157c224e8f68de46b38940b49`

```dockerfile
```

-	Layers:
	-	`sha256:23c8667820bb59f98de2399ca094a9f7c22b568742724ba073b0808d30c595ba`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.5.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0db55768f09d1439f8aa0cde4dfe62d29851e97d2b579cf58806d5539ce4864e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247200542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592b6d055dc5d1c5d3a7907c39d41941f9097e55edd6771bf33ee34294353b35`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:27 GMT
ARG VERSION=26.5.3.52
# Fri, 26 Jun 2026 17:53:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:53:54 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:53:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:53:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:53:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:53:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc33f9b57fa7d57e87efad20c03ca51da3bff4ea4d0e740af9c87a4217d6b36b`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 7.5 MB (7535259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046eab11a99682a8dde9fe257a433d95a2fd6411d55a2eccd737a6ceaa24be1b`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 211.2 MB (211188611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f71f0c7d8f36695c089f35d2a6e92610e1585547da892a53fd3adea5a3aec74`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972f876f872c67d92f6843b7e9cb8e93bc1470e77d84539685f3ff1b878e09a1`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50065ee90e073f2044341ddd5b2f22c28e778122069519d147db4b68c13f5491`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca50da3dd824df56605558094758fdd85617c31c148ec2b282210f19da1d5984`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c503afdb6351f35485a264efde5fb2da225c10dff23e8b3c3de460346b071`  
		Last Modified: Fri, 26 Jun 2026 17:54:18 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:776f7fd79de9880ffdf1c92b336aad3d623135786645de34940af232c09d87d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63231a5509729c05796cbdf97d63db79639aab1a7f87f39efbf30136043e7bb`

```dockerfile
```

-	Layers:
	-	`sha256:8f7fba1e89b6dcb3b052445fca6a8b92bf5f7ed57847c78ad519f8b268722147`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.5.3-jammy`

```console
$ docker pull clickhouse@sha256:7e74f0a4c13733f45f11a783cdfe712273220f37b4bc2e66c6389e91427a6770
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.5.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:53231f9d8910f2bf8023a5c12f403da171dc32886bf598b80408fadf639ce14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261391816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1382d83a1461d18a2e2558f7b4b988133ab89835c47f382a0e2797dd32a04d78`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:36 GMT
ARG VERSION=26.5.3.52
# Fri, 26 Jun 2026 17:48:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:01 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:01 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:02 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:02 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463352a3264930f02f9ffb69e200c163bf1cc1843bbda180fad3999231973014`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 7.6 MB (7555039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a544d79e69644dcc071eeda3d5c34c6a6fdb9b877040bf9a580fe2b2c004ae`  
		Last Modified: Fri, 26 Jun 2026 17:49:32 GMT  
		Size: 223.2 MB (223230047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed1281811609cac707694dbaacb26040c5ce88cf9b865a46edb76d93cdc1ca7`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d0b421df4edf934fff42d42f5005fc571173b1be57c741c4f05d132f924974`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69f9c494f5efe09fed621e0861b832ae7c9c971de0bef6d3d6b4b0ca121dddc`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c164df2d361d4edb0407a50f3815eb3b24e36963e33b6f8b36847be91b41f49`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0d6c45240b715b7ed32cffb574770793646da4a5702bc20c2470a9f8ab83ec`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:00c1a376173c0a75daf1eb98ec9b8df7f7fc96fd18ca0707faf47fd07645af86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7e521b77498aab37807ddf34e5e17e391f0ec157c224e8f68de46b38940b49`

```dockerfile
```

-	Layers:
	-	`sha256:23c8667820bb59f98de2399ca094a9f7c22b568742724ba073b0808d30c595ba`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.5.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0db55768f09d1439f8aa0cde4dfe62d29851e97d2b579cf58806d5539ce4864e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247200542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592b6d055dc5d1c5d3a7907c39d41941f9097e55edd6771bf33ee34294353b35`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:27 GMT
ARG VERSION=26.5.3.52
# Fri, 26 Jun 2026 17:53:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:53:54 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:53:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:53:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:53:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:53:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc33f9b57fa7d57e87efad20c03ca51da3bff4ea4d0e740af9c87a4217d6b36b`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 7.5 MB (7535259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046eab11a99682a8dde9fe257a433d95a2fd6411d55a2eccd737a6ceaa24be1b`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 211.2 MB (211188611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f71f0c7d8f36695c089f35d2a6e92610e1585547da892a53fd3adea5a3aec74`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972f876f872c67d92f6843b7e9cb8e93bc1470e77d84539685f3ff1b878e09a1`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50065ee90e073f2044341ddd5b2f22c28e778122069519d147db4b68c13f5491`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca50da3dd824df56605558094758fdd85617c31c148ec2b282210f19da1d5984`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c503afdb6351f35485a264efde5fb2da225c10dff23e8b3c3de460346b071`  
		Last Modified: Fri, 26 Jun 2026 17:54:18 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:776f7fd79de9880ffdf1c92b336aad3d623135786645de34940af232c09d87d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63231a5509729c05796cbdf97d63db79639aab1a7f87f39efbf30136043e7bb`

```dockerfile
```

-	Layers:
	-	`sha256:8f7fba1e89b6dcb3b052445fca6a8b92bf5f7ed57847c78ad519f8b268722147`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.5.3.52`

```console
$ docker pull clickhouse@sha256:7e74f0a4c13733f45f11a783cdfe712273220f37b4bc2e66c6389e91427a6770
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.5.3.52` - linux; amd64

```console
$ docker pull clickhouse@sha256:53231f9d8910f2bf8023a5c12f403da171dc32886bf598b80408fadf639ce14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261391816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1382d83a1461d18a2e2558f7b4b988133ab89835c47f382a0e2797dd32a04d78`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:36 GMT
ARG VERSION=26.5.3.52
# Fri, 26 Jun 2026 17:48:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:01 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:01 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:02 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:02 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463352a3264930f02f9ffb69e200c163bf1cc1843bbda180fad3999231973014`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 7.6 MB (7555039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a544d79e69644dcc071eeda3d5c34c6a6fdb9b877040bf9a580fe2b2c004ae`  
		Last Modified: Fri, 26 Jun 2026 17:49:32 GMT  
		Size: 223.2 MB (223230047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed1281811609cac707694dbaacb26040c5ce88cf9b865a46edb76d93cdc1ca7`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d0b421df4edf934fff42d42f5005fc571173b1be57c741c4f05d132f924974`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69f9c494f5efe09fed621e0861b832ae7c9c971de0bef6d3d6b4b0ca121dddc`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c164df2d361d4edb0407a50f3815eb3b24e36963e33b6f8b36847be91b41f49`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0d6c45240b715b7ed32cffb574770793646da4a5702bc20c2470a9f8ab83ec`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5.3.52` - unknown; unknown

```console
$ docker pull clickhouse@sha256:00c1a376173c0a75daf1eb98ec9b8df7f7fc96fd18ca0707faf47fd07645af86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7e521b77498aab37807ddf34e5e17e391f0ec157c224e8f68de46b38940b49`

```dockerfile
```

-	Layers:
	-	`sha256:23c8667820bb59f98de2399ca094a9f7c22b568742724ba073b0808d30c595ba`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.5.3.52` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0db55768f09d1439f8aa0cde4dfe62d29851e97d2b579cf58806d5539ce4864e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247200542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592b6d055dc5d1c5d3a7907c39d41941f9097e55edd6771bf33ee34294353b35`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:27 GMT
ARG VERSION=26.5.3.52
# Fri, 26 Jun 2026 17:53:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:53:54 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:53:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:53:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:53:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:53:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc33f9b57fa7d57e87efad20c03ca51da3bff4ea4d0e740af9c87a4217d6b36b`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 7.5 MB (7535259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046eab11a99682a8dde9fe257a433d95a2fd6411d55a2eccd737a6ceaa24be1b`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 211.2 MB (211188611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f71f0c7d8f36695c089f35d2a6e92610e1585547da892a53fd3adea5a3aec74`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972f876f872c67d92f6843b7e9cb8e93bc1470e77d84539685f3ff1b878e09a1`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50065ee90e073f2044341ddd5b2f22c28e778122069519d147db4b68c13f5491`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca50da3dd824df56605558094758fdd85617c31c148ec2b282210f19da1d5984`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c503afdb6351f35485a264efde5fb2da225c10dff23e8b3c3de460346b071`  
		Last Modified: Fri, 26 Jun 2026 17:54:18 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5.3.52` - unknown; unknown

```console
$ docker pull clickhouse@sha256:776f7fd79de9880ffdf1c92b336aad3d623135786645de34940af232c09d87d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63231a5509729c05796cbdf97d63db79639aab1a7f87f39efbf30136043e7bb`

```dockerfile
```

-	Layers:
	-	`sha256:8f7fba1e89b6dcb3b052445fca6a8b92bf5f7ed57847c78ad519f8b268722147`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.5.3.52-jammy`

```console
$ docker pull clickhouse@sha256:7e74f0a4c13733f45f11a783cdfe712273220f37b4bc2e66c6389e91427a6770
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.5.3.52-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:53231f9d8910f2bf8023a5c12f403da171dc32886bf598b80408fadf639ce14b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.4 MB (261391816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1382d83a1461d18a2e2558f7b4b988133ab89835c47f382a0e2797dd32a04d78`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:36 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:36 GMT
ARG VERSION=26.5.3.52
# Fri, 26 Jun 2026 17:48:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:01 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:01 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:02 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:02 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:02 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463352a3264930f02f9ffb69e200c163bf1cc1843bbda180fad3999231973014`  
		Last Modified: Fri, 26 Jun 2026 17:49:28 GMT  
		Size: 7.6 MB (7555039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a544d79e69644dcc071eeda3d5c34c6a6fdb9b877040bf9a580fe2b2c004ae`  
		Last Modified: Fri, 26 Jun 2026 17:49:32 GMT  
		Size: 223.2 MB (223230047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed1281811609cac707694dbaacb26040c5ce88cf9b865a46edb76d93cdc1ca7`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8d0b421df4edf934fff42d42f5005fc571173b1be57c741c4f05d132f924974`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69f9c494f5efe09fed621e0861b832ae7c9c971de0bef6d3d6b4b0ca121dddc`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c164df2d361d4edb0407a50f3815eb3b24e36963e33b6f8b36847be91b41f49`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0d6c45240b715b7ed32cffb574770793646da4a5702bc20c2470a9f8ab83ec`  
		Last Modified: Fri, 26 Jun 2026 17:49:29 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5.3.52-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:00c1a376173c0a75daf1eb98ec9b8df7f7fc96fd18ca0707faf47fd07645af86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7e521b77498aab37807ddf34e5e17e391f0ec157c224e8f68de46b38940b49`

```dockerfile
```

-	Layers:
	-	`sha256:23c8667820bb59f98de2399ca094a9f7c22b568742724ba073b0808d30c595ba`  
		Last Modified: Fri, 26 Jun 2026 17:49:27 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.5.3.52-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0db55768f09d1439f8aa0cde4dfe62d29851e97d2b579cf58806d5539ce4864e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 MB (247200542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:592b6d055dc5d1c5d3a7907c39d41941f9097e55edd6771bf33ee34294353b35`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:27 GMT
ARG VERSION=26.5.3.52
# Fri, 26 Jun 2026 17:53:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:52 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:53:54 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:53:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.3.52 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:53:54 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:53:54 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:53:54 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:53:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc33f9b57fa7d57e87efad20c03ca51da3bff4ea4d0e740af9c87a4217d6b36b`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 7.5 MB (7535259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046eab11a99682a8dde9fe257a433d95a2fd6411d55a2eccd737a6ceaa24be1b`  
		Last Modified: Fri, 26 Jun 2026 17:54:21 GMT  
		Size: 211.2 MB (211188611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f71f0c7d8f36695c089f35d2a6e92610e1585547da892a53fd3adea5a3aec74`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972f876f872c67d92f6843b7e9cb8e93bc1470e77d84539685f3ff1b878e09a1`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50065ee90e073f2044341ddd5b2f22c28e778122069519d147db4b68c13f5491`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca50da3dd824df56605558094758fdd85617c31c148ec2b282210f19da1d5984`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05c503afdb6351f35485a264efde5fb2da225c10dff23e8b3c3de460346b071`  
		Last Modified: Fri, 26 Jun 2026 17:54:18 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5.3.52-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:776f7fd79de9880ffdf1c92b336aad3d623135786645de34940af232c09d87d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63231a5509729c05796cbdf97d63db79639aab1a7f87f39efbf30136043e7bb`

```dockerfile
```

-	Layers:
	-	`sha256:8f7fba1e89b6dcb3b052445fca6a8b92bf5f7ed57847c78ad519f8b268722147`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.6`

```console
$ docker pull clickhouse@sha256:f673e67e03d4690afca8cda7d0afc2fc8da9b406e1935a97401b4572e11b107d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:494f62a5f20029b8a33d2151b2aeea10574393c38b4635108e78a705f2880f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276605679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbe212fc5fe12f7cdf4e027f0473db2742932d70eaab99a2d4142ed9de21ea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:09 GMT
ARG VERSION=26.6.1.1193
# Fri, 26 Jun 2026 17:48:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:48:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:48:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:48:37 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:48:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:48:37 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:48:37 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:48:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f400e751dc35077f621dfe51df04c2822947bfbba4130c430417ae7f313fe58`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 7.6 MB (7555000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2020a25fe8c2113a1ec061a7f071077524a01c6e799618b0d1788910befb050`  
		Last Modified: Fri, 26 Jun 2026 17:49:08 GMT  
		Size: 238.4 MB (238443942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac524d0f7f9668dee3b1e22accb284edf0a0cda26afcf81d0b4e1dc27dc32646`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95de8187a290253fb1310500b63672b998ba8362e836fcc30b4725dc22234d82`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedb3b3ff28f5b250206aaf80b1f23b1428146c67f3b2c61584f9414ad55e943`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb921857db850e297ae55e3d8d498402174784aa95656c9dd34d0ff7fd35bb4`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4944d35d5bb5b5f94eb8839da4d7c1173e941cc487bc25806835c600f5862f4`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fe38dae352d894ad6febed1e983ae39dff1f405938a7405fbafa46af59e5c66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c14e099a4d73b5ea9802483c6f28bc40888796cd0259a05256e6ed39e3236cf`

```dockerfile
```

-	Layers:
	-	`sha256:bce8189ac79717129be3c6057f5b2bbda0f9ea5e7fe6e43bf8b698bfba040d97`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 26.9 KB (26852 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec8059c6f50dc22f9cb7ce3f397b00348235fda587ad9d1823dd5a792e13c9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257073199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee7920992da407dacadf2a17f3af221ed4e216720b20091f44fc77a20d47b88`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:27 GMT
ARG VERSION=26.6.1.1193
# Fri, 26 Jun 2026 17:53:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:53:53 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:53:53 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:53:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:53:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7631f1782bde1c888eb4c855a766a931272a7bde65dcf5a061a55cd2f689bf`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 7.5 MB (7535260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f8cb798bceaaf770e77942a73995377421cdb301a03afa33070de3bdbc464`  
		Last Modified: Fri, 26 Jun 2026 17:54:19 GMT  
		Size: 221.1 MB (221061268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed3648937c5e0ad96293e2b57fda1083882f56f4f5262708bcd25b16df5348`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d2fed349b01ac209682e2db57923bec00a3429e7d969029987b0f78b77f35`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb471e0275ac28a26c07a3efc49cced03307c99800b4465d3ee502eafad72b9`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f06e8bdb3811b9e7d2cf82fc61c1b1e629d7af1c1b556d83cddd97f42f378d4`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1cb65e0225531d5afca142313b4308c459c52c8760654e60b14818890c008`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6c1b56573cff05a72abb45aa47769fefa463886dfd9b76e0708e19e94897cdea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aae4933083cb3c7cd8a1bd0ce5f547b2f25ce6be5c9f5ab0f0cbf40db8bac03`

```dockerfile
```

-	Layers:
	-	`sha256:5ea793d24c52a96b076993e670b1d01dbd1f9f3ed75222d52f2a436bdeac477b`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 27.1 KB (27064 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.6-jammy`

```console
$ docker pull clickhouse@sha256:f673e67e03d4690afca8cda7d0afc2fc8da9b406e1935a97401b4572e11b107d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:494f62a5f20029b8a33d2151b2aeea10574393c38b4635108e78a705f2880f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276605679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbe212fc5fe12f7cdf4e027f0473db2742932d70eaab99a2d4142ed9de21ea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:09 GMT
ARG VERSION=26.6.1.1193
# Fri, 26 Jun 2026 17:48:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:48:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:48:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:48:37 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:48:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:48:37 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:48:37 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:48:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f400e751dc35077f621dfe51df04c2822947bfbba4130c430417ae7f313fe58`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 7.6 MB (7555000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2020a25fe8c2113a1ec061a7f071077524a01c6e799618b0d1788910befb050`  
		Last Modified: Fri, 26 Jun 2026 17:49:08 GMT  
		Size: 238.4 MB (238443942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac524d0f7f9668dee3b1e22accb284edf0a0cda26afcf81d0b4e1dc27dc32646`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95de8187a290253fb1310500b63672b998ba8362e836fcc30b4725dc22234d82`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedb3b3ff28f5b250206aaf80b1f23b1428146c67f3b2c61584f9414ad55e943`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb921857db850e297ae55e3d8d498402174784aa95656c9dd34d0ff7fd35bb4`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4944d35d5bb5b5f94eb8839da4d7c1173e941cc487bc25806835c600f5862f4`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fe38dae352d894ad6febed1e983ae39dff1f405938a7405fbafa46af59e5c66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c14e099a4d73b5ea9802483c6f28bc40888796cd0259a05256e6ed39e3236cf`

```dockerfile
```

-	Layers:
	-	`sha256:bce8189ac79717129be3c6057f5b2bbda0f9ea5e7fe6e43bf8b698bfba040d97`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 26.9 KB (26852 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec8059c6f50dc22f9cb7ce3f397b00348235fda587ad9d1823dd5a792e13c9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257073199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee7920992da407dacadf2a17f3af221ed4e216720b20091f44fc77a20d47b88`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:27 GMT
ARG VERSION=26.6.1.1193
# Fri, 26 Jun 2026 17:53:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:53:53 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:53:53 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:53:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:53:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7631f1782bde1c888eb4c855a766a931272a7bde65dcf5a061a55cd2f689bf`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 7.5 MB (7535260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f8cb798bceaaf770e77942a73995377421cdb301a03afa33070de3bdbc464`  
		Last Modified: Fri, 26 Jun 2026 17:54:19 GMT  
		Size: 221.1 MB (221061268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed3648937c5e0ad96293e2b57fda1083882f56f4f5262708bcd25b16df5348`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d2fed349b01ac209682e2db57923bec00a3429e7d969029987b0f78b77f35`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb471e0275ac28a26c07a3efc49cced03307c99800b4465d3ee502eafad72b9`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f06e8bdb3811b9e7d2cf82fc61c1b1e629d7af1c1b556d83cddd97f42f378d4`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1cb65e0225531d5afca142313b4308c459c52c8760654e60b14818890c008`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6c1b56573cff05a72abb45aa47769fefa463886dfd9b76e0708e19e94897cdea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aae4933083cb3c7cd8a1bd0ce5f547b2f25ce6be5c9f5ab0f0cbf40db8bac03`

```dockerfile
```

-	Layers:
	-	`sha256:5ea793d24c52a96b076993e670b1d01dbd1f9f3ed75222d52f2a436bdeac477b`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 27.1 KB (27064 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.6.1`

```console
$ docker pull clickhouse@sha256:f673e67e03d4690afca8cda7d0afc2fc8da9b406e1935a97401b4572e11b107d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.6.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:494f62a5f20029b8a33d2151b2aeea10574393c38b4635108e78a705f2880f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276605679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbe212fc5fe12f7cdf4e027f0473db2742932d70eaab99a2d4142ed9de21ea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:09 GMT
ARG VERSION=26.6.1.1193
# Fri, 26 Jun 2026 17:48:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:48:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:48:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:48:37 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:48:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:48:37 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:48:37 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:48:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f400e751dc35077f621dfe51df04c2822947bfbba4130c430417ae7f313fe58`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 7.6 MB (7555000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2020a25fe8c2113a1ec061a7f071077524a01c6e799618b0d1788910befb050`  
		Last Modified: Fri, 26 Jun 2026 17:49:08 GMT  
		Size: 238.4 MB (238443942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac524d0f7f9668dee3b1e22accb284edf0a0cda26afcf81d0b4e1dc27dc32646`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95de8187a290253fb1310500b63672b998ba8362e836fcc30b4725dc22234d82`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedb3b3ff28f5b250206aaf80b1f23b1428146c67f3b2c61584f9414ad55e943`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb921857db850e297ae55e3d8d498402174784aa95656c9dd34d0ff7fd35bb4`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4944d35d5bb5b5f94eb8839da4d7c1173e941cc487bc25806835c600f5862f4`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.6.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fe38dae352d894ad6febed1e983ae39dff1f405938a7405fbafa46af59e5c66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c14e099a4d73b5ea9802483c6f28bc40888796cd0259a05256e6ed39e3236cf`

```dockerfile
```

-	Layers:
	-	`sha256:bce8189ac79717129be3c6057f5b2bbda0f9ea5e7fe6e43bf8b698bfba040d97`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 26.9 KB (26852 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.6.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec8059c6f50dc22f9cb7ce3f397b00348235fda587ad9d1823dd5a792e13c9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257073199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee7920992da407dacadf2a17f3af221ed4e216720b20091f44fc77a20d47b88`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:27 GMT
ARG VERSION=26.6.1.1193
# Fri, 26 Jun 2026 17:53:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:53:53 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:53:53 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:53:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:53:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7631f1782bde1c888eb4c855a766a931272a7bde65dcf5a061a55cd2f689bf`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 7.5 MB (7535260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f8cb798bceaaf770e77942a73995377421cdb301a03afa33070de3bdbc464`  
		Last Modified: Fri, 26 Jun 2026 17:54:19 GMT  
		Size: 221.1 MB (221061268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed3648937c5e0ad96293e2b57fda1083882f56f4f5262708bcd25b16df5348`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d2fed349b01ac209682e2db57923bec00a3429e7d969029987b0f78b77f35`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb471e0275ac28a26c07a3efc49cced03307c99800b4465d3ee502eafad72b9`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f06e8bdb3811b9e7d2cf82fc61c1b1e629d7af1c1b556d83cddd97f42f378d4`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1cb65e0225531d5afca142313b4308c459c52c8760654e60b14818890c008`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.6.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6c1b56573cff05a72abb45aa47769fefa463886dfd9b76e0708e19e94897cdea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aae4933083cb3c7cd8a1bd0ce5f547b2f25ce6be5c9f5ab0f0cbf40db8bac03`

```dockerfile
```

-	Layers:
	-	`sha256:5ea793d24c52a96b076993e670b1d01dbd1f9f3ed75222d52f2a436bdeac477b`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 27.1 KB (27064 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.6.1-jammy`

```console
$ docker pull clickhouse@sha256:f673e67e03d4690afca8cda7d0afc2fc8da9b406e1935a97401b4572e11b107d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.6.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:494f62a5f20029b8a33d2151b2aeea10574393c38b4635108e78a705f2880f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276605679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbe212fc5fe12f7cdf4e027f0473db2742932d70eaab99a2d4142ed9de21ea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:09 GMT
ARG VERSION=26.6.1.1193
# Fri, 26 Jun 2026 17:48:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:48:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:48:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:48:37 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:48:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:48:37 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:48:37 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:48:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f400e751dc35077f621dfe51df04c2822947bfbba4130c430417ae7f313fe58`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 7.6 MB (7555000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2020a25fe8c2113a1ec061a7f071077524a01c6e799618b0d1788910befb050`  
		Last Modified: Fri, 26 Jun 2026 17:49:08 GMT  
		Size: 238.4 MB (238443942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac524d0f7f9668dee3b1e22accb284edf0a0cda26afcf81d0b4e1dc27dc32646`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95de8187a290253fb1310500b63672b998ba8362e836fcc30b4725dc22234d82`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedb3b3ff28f5b250206aaf80b1f23b1428146c67f3b2c61584f9414ad55e943`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb921857db850e297ae55e3d8d498402174784aa95656c9dd34d0ff7fd35bb4`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4944d35d5bb5b5f94eb8839da4d7c1173e941cc487bc25806835c600f5862f4`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.6.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fe38dae352d894ad6febed1e983ae39dff1f405938a7405fbafa46af59e5c66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c14e099a4d73b5ea9802483c6f28bc40888796cd0259a05256e6ed39e3236cf`

```dockerfile
```

-	Layers:
	-	`sha256:bce8189ac79717129be3c6057f5b2bbda0f9ea5e7fe6e43bf8b698bfba040d97`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 26.9 KB (26852 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.6.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec8059c6f50dc22f9cb7ce3f397b00348235fda587ad9d1823dd5a792e13c9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257073199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee7920992da407dacadf2a17f3af221ed4e216720b20091f44fc77a20d47b88`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:27 GMT
ARG VERSION=26.6.1.1193
# Fri, 26 Jun 2026 17:53:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:53:53 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:53:53 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:53:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:53:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7631f1782bde1c888eb4c855a766a931272a7bde65dcf5a061a55cd2f689bf`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 7.5 MB (7535260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f8cb798bceaaf770e77942a73995377421cdb301a03afa33070de3bdbc464`  
		Last Modified: Fri, 26 Jun 2026 17:54:19 GMT  
		Size: 221.1 MB (221061268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed3648937c5e0ad96293e2b57fda1083882f56f4f5262708bcd25b16df5348`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d2fed349b01ac209682e2db57923bec00a3429e7d969029987b0f78b77f35`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb471e0275ac28a26c07a3efc49cced03307c99800b4465d3ee502eafad72b9`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f06e8bdb3811b9e7d2cf82fc61c1b1e629d7af1c1b556d83cddd97f42f378d4`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1cb65e0225531d5afca142313b4308c459c52c8760654e60b14818890c008`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.6.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6c1b56573cff05a72abb45aa47769fefa463886dfd9b76e0708e19e94897cdea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aae4933083cb3c7cd8a1bd0ce5f547b2f25ce6be5c9f5ab0f0cbf40db8bac03`

```dockerfile
```

-	Layers:
	-	`sha256:5ea793d24c52a96b076993e670b1d01dbd1f9f3ed75222d52f2a436bdeac477b`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 27.1 KB (27064 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.6.1.1193`

```console
$ docker pull clickhouse@sha256:f673e67e03d4690afca8cda7d0afc2fc8da9b406e1935a97401b4572e11b107d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.6.1.1193` - linux; amd64

```console
$ docker pull clickhouse@sha256:494f62a5f20029b8a33d2151b2aeea10574393c38b4635108e78a705f2880f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276605679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbe212fc5fe12f7cdf4e027f0473db2742932d70eaab99a2d4142ed9de21ea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:09 GMT
ARG VERSION=26.6.1.1193
# Fri, 26 Jun 2026 17:48:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:48:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:48:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:48:37 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:48:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:48:37 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:48:37 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:48:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f400e751dc35077f621dfe51df04c2822947bfbba4130c430417ae7f313fe58`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 7.6 MB (7555000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2020a25fe8c2113a1ec061a7f071077524a01c6e799618b0d1788910befb050`  
		Last Modified: Fri, 26 Jun 2026 17:49:08 GMT  
		Size: 238.4 MB (238443942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac524d0f7f9668dee3b1e22accb284edf0a0cda26afcf81d0b4e1dc27dc32646`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95de8187a290253fb1310500b63672b998ba8362e836fcc30b4725dc22234d82`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedb3b3ff28f5b250206aaf80b1f23b1428146c67f3b2c61584f9414ad55e943`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb921857db850e297ae55e3d8d498402174784aa95656c9dd34d0ff7fd35bb4`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4944d35d5bb5b5f94eb8839da4d7c1173e941cc487bc25806835c600f5862f4`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.6.1.1193` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fe38dae352d894ad6febed1e983ae39dff1f405938a7405fbafa46af59e5c66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c14e099a4d73b5ea9802483c6f28bc40888796cd0259a05256e6ed39e3236cf`

```dockerfile
```

-	Layers:
	-	`sha256:bce8189ac79717129be3c6057f5b2bbda0f9ea5e7fe6e43bf8b698bfba040d97`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 26.9 KB (26852 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.6.1.1193` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec8059c6f50dc22f9cb7ce3f397b00348235fda587ad9d1823dd5a792e13c9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257073199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee7920992da407dacadf2a17f3af221ed4e216720b20091f44fc77a20d47b88`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:27 GMT
ARG VERSION=26.6.1.1193
# Fri, 26 Jun 2026 17:53:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:53:53 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:53:53 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:53:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:53:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7631f1782bde1c888eb4c855a766a931272a7bde65dcf5a061a55cd2f689bf`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 7.5 MB (7535260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f8cb798bceaaf770e77942a73995377421cdb301a03afa33070de3bdbc464`  
		Last Modified: Fri, 26 Jun 2026 17:54:19 GMT  
		Size: 221.1 MB (221061268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed3648937c5e0ad96293e2b57fda1083882f56f4f5262708bcd25b16df5348`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d2fed349b01ac209682e2db57923bec00a3429e7d969029987b0f78b77f35`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb471e0275ac28a26c07a3efc49cced03307c99800b4465d3ee502eafad72b9`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f06e8bdb3811b9e7d2cf82fc61c1b1e629d7af1c1b556d83cddd97f42f378d4`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1cb65e0225531d5afca142313b4308c459c52c8760654e60b14818890c008`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.6.1.1193` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6c1b56573cff05a72abb45aa47769fefa463886dfd9b76e0708e19e94897cdea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aae4933083cb3c7cd8a1bd0ce5f547b2f25ce6be5c9f5ab0f0cbf40db8bac03`

```dockerfile
```

-	Layers:
	-	`sha256:5ea793d24c52a96b076993e670b1d01dbd1f9f3ed75222d52f2a436bdeac477b`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 27.1 KB (27064 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.6.1.1193-jammy`

```console
$ docker pull clickhouse@sha256:f673e67e03d4690afca8cda7d0afc2fc8da9b406e1935a97401b4572e11b107d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.6.1.1193-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:494f62a5f20029b8a33d2151b2aeea10574393c38b4635108e78a705f2880f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276605679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbe212fc5fe12f7cdf4e027f0473db2742932d70eaab99a2d4142ed9de21ea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:09 GMT
ARG VERSION=26.6.1.1193
# Fri, 26 Jun 2026 17:48:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:48:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:48:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:48:37 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:48:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:48:37 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:48:37 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:48:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f400e751dc35077f621dfe51df04c2822947bfbba4130c430417ae7f313fe58`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 7.6 MB (7555000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2020a25fe8c2113a1ec061a7f071077524a01c6e799618b0d1788910befb050`  
		Last Modified: Fri, 26 Jun 2026 17:49:08 GMT  
		Size: 238.4 MB (238443942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac524d0f7f9668dee3b1e22accb284edf0a0cda26afcf81d0b4e1dc27dc32646`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95de8187a290253fb1310500b63672b998ba8362e836fcc30b4725dc22234d82`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedb3b3ff28f5b250206aaf80b1f23b1428146c67f3b2c61584f9414ad55e943`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb921857db850e297ae55e3d8d498402174784aa95656c9dd34d0ff7fd35bb4`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4944d35d5bb5b5f94eb8839da4d7c1173e941cc487bc25806835c600f5862f4`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.6.1.1193-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fe38dae352d894ad6febed1e983ae39dff1f405938a7405fbafa46af59e5c66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c14e099a4d73b5ea9802483c6f28bc40888796cd0259a05256e6ed39e3236cf`

```dockerfile
```

-	Layers:
	-	`sha256:bce8189ac79717129be3c6057f5b2bbda0f9ea5e7fe6e43bf8b698bfba040d97`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 26.9 KB (26852 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.6.1.1193-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec8059c6f50dc22f9cb7ce3f397b00348235fda587ad9d1823dd5a792e13c9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257073199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee7920992da407dacadf2a17f3af221ed4e216720b20091f44fc77a20d47b88`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:27 GMT
ARG VERSION=26.6.1.1193
# Fri, 26 Jun 2026 17:53:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:53:53 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:53:53 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:53:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:53:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7631f1782bde1c888eb4c855a766a931272a7bde65dcf5a061a55cd2f689bf`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 7.5 MB (7535260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f8cb798bceaaf770e77942a73995377421cdb301a03afa33070de3bdbc464`  
		Last Modified: Fri, 26 Jun 2026 17:54:19 GMT  
		Size: 221.1 MB (221061268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed3648937c5e0ad96293e2b57fda1083882f56f4f5262708bcd25b16df5348`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d2fed349b01ac209682e2db57923bec00a3429e7d969029987b0f78b77f35`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb471e0275ac28a26c07a3efc49cced03307c99800b4465d3ee502eafad72b9`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f06e8bdb3811b9e7d2cf82fc61c1b1e629d7af1c1b556d83cddd97f42f378d4`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1cb65e0225531d5afca142313b4308c459c52c8760654e60b14818890c008`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.6.1.1193-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6c1b56573cff05a72abb45aa47769fefa463886dfd9b76e0708e19e94897cdea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aae4933083cb3c7cd8a1bd0ce5f547b2f25ce6be5c9f5ab0f0cbf40db8bac03`

```dockerfile
```

-	Layers:
	-	`sha256:5ea793d24c52a96b076993e670b1d01dbd1f9f3ed75222d52f2a436bdeac477b`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 27.1 KB (27064 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:f673e67e03d4690afca8cda7d0afc2fc8da9b406e1935a97401b4572e11b107d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:494f62a5f20029b8a33d2151b2aeea10574393c38b4635108e78a705f2880f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276605679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbe212fc5fe12f7cdf4e027f0473db2742932d70eaab99a2d4142ed9de21ea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:09 GMT
ARG VERSION=26.6.1.1193
# Fri, 26 Jun 2026 17:48:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:48:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:48:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:48:37 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:48:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:48:37 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:48:37 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:48:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f400e751dc35077f621dfe51df04c2822947bfbba4130c430417ae7f313fe58`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 7.6 MB (7555000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2020a25fe8c2113a1ec061a7f071077524a01c6e799618b0d1788910befb050`  
		Last Modified: Fri, 26 Jun 2026 17:49:08 GMT  
		Size: 238.4 MB (238443942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac524d0f7f9668dee3b1e22accb284edf0a0cda26afcf81d0b4e1dc27dc32646`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95de8187a290253fb1310500b63672b998ba8362e836fcc30b4725dc22234d82`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedb3b3ff28f5b250206aaf80b1f23b1428146c67f3b2c61584f9414ad55e943`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb921857db850e297ae55e3d8d498402174784aa95656c9dd34d0ff7fd35bb4`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4944d35d5bb5b5f94eb8839da4d7c1173e941cc487bc25806835c600f5862f4`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fe38dae352d894ad6febed1e983ae39dff1f405938a7405fbafa46af59e5c66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c14e099a4d73b5ea9802483c6f28bc40888796cd0259a05256e6ed39e3236cf`

```dockerfile
```

-	Layers:
	-	`sha256:bce8189ac79717129be3c6057f5b2bbda0f9ea5e7fe6e43bf8b698bfba040d97`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 26.9 KB (26852 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec8059c6f50dc22f9cb7ce3f397b00348235fda587ad9d1823dd5a792e13c9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257073199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee7920992da407dacadf2a17f3af221ed4e216720b20091f44fc77a20d47b88`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:27 GMT
ARG VERSION=26.6.1.1193
# Fri, 26 Jun 2026 17:53:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:53:53 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:53:53 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:53:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:53:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7631f1782bde1c888eb4c855a766a931272a7bde65dcf5a061a55cd2f689bf`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 7.5 MB (7535260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f8cb798bceaaf770e77942a73995377421cdb301a03afa33070de3bdbc464`  
		Last Modified: Fri, 26 Jun 2026 17:54:19 GMT  
		Size: 221.1 MB (221061268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed3648937c5e0ad96293e2b57fda1083882f56f4f5262708bcd25b16df5348`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d2fed349b01ac209682e2db57923bec00a3429e7d969029987b0f78b77f35`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb471e0275ac28a26c07a3efc49cced03307c99800b4465d3ee502eafad72b9`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f06e8bdb3811b9e7d2cf82fc61c1b1e629d7af1c1b556d83cddd97f42f378d4`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1cb65e0225531d5afca142313b4308c459c52c8760654e60b14818890c008`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6c1b56573cff05a72abb45aa47769fefa463886dfd9b76e0708e19e94897cdea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aae4933083cb3c7cd8a1bd0ce5f547b2f25ce6be5c9f5ab0f0cbf40db8bac03`

```dockerfile
```

-	Layers:
	-	`sha256:5ea793d24c52a96b076993e670b1d01dbd1f9f3ed75222d52f2a436bdeac477b`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 27.1 KB (27064 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:f673e67e03d4690afca8cda7d0afc2fc8da9b406e1935a97401b4572e11b107d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:494f62a5f20029b8a33d2151b2aeea10574393c38b4635108e78a705f2880f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276605679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ebbe212fc5fe12f7cdf4e027f0473db2742932d70eaab99a2d4142ed9de21ea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:09 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:09 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:09 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:09 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:09 GMT
ARG VERSION=26.6.1.1193
# Fri, 26 Jun 2026 17:48:09 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:48:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:48:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:48:37 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:48:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:48:37 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:48:37 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:48:37 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:48:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f400e751dc35077f621dfe51df04c2822947bfbba4130c430417ae7f313fe58`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 7.6 MB (7555000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2020a25fe8c2113a1ec061a7f071077524a01c6e799618b0d1788910befb050`  
		Last Modified: Fri, 26 Jun 2026 17:49:08 GMT  
		Size: 238.4 MB (238443942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac524d0f7f9668dee3b1e22accb284edf0a0cda26afcf81d0b4e1dc27dc32646`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 187.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95de8187a290253fb1310500b63672b998ba8362e836fcc30b4725dc22234d82`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedb3b3ff28f5b250206aaf80b1f23b1428146c67f3b2c61584f9414ad55e943`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb921857db850e297ae55e3d8d498402174784aa95656c9dd34d0ff7fd35bb4`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4944d35d5bb5b5f94eb8839da4d7c1173e941cc487bc25806835c600f5862f4`  
		Last Modified: Fri, 26 Jun 2026 17:49:04 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fe38dae352d894ad6febed1e983ae39dff1f405938a7405fbafa46af59e5c66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c14e099a4d73b5ea9802483c6f28bc40888796cd0259a05256e6ed39e3236cf`

```dockerfile
```

-	Layers:
	-	`sha256:bce8189ac79717129be3c6057f5b2bbda0f9ea5e7fe6e43bf8b698bfba040d97`  
		Last Modified: Fri, 26 Jun 2026 17:49:03 GMT  
		Size: 26.9 KB (26852 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:ec8059c6f50dc22f9cb7ce3f397b00348235fda587ad9d1823dd5a792e13c9aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.1 MB (257073199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ee7920992da407dacadf2a17f3af221ed4e216720b20091f44fc77a20d47b88`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:27 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:27 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:27 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:27 GMT
ARG VERSION=26.6.1.1193
# Fri, 26 Jun 2026 17:53:27 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:53:53 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:53:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.6.1.1193 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:53:53 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:53:53 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:53:53 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:53:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7631f1782bde1c888eb4c855a766a931272a7bde65dcf5a061a55cd2f689bf`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 7.5 MB (7535260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187f8cb798bceaaf770e77942a73995377421cdb301a03afa33070de3bdbc464`  
		Last Modified: Fri, 26 Jun 2026 17:54:19 GMT  
		Size: 221.1 MB (221061268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93ed3648937c5e0ad96293e2b57fda1083882f56f4f5262708bcd25b16df5348`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7d2fed349b01ac209682e2db57923bec00a3429e7d969029987b0f78b77f35`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beb471e0275ac28a26c07a3efc49cced03307c99800b4465d3ee502eafad72b9`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f06e8bdb3811b9e7d2cf82fc61c1b1e629d7af1c1b556d83cddd97f42f378d4`  
		Last Modified: Fri, 26 Jun 2026 17:54:16 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d1cb65e0225531d5afca142313b4308c459c52c8760654e60b14818890c008`  
		Last Modified: Fri, 26 Jun 2026 17:54:17 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6c1b56573cff05a72abb45aa47769fefa463886dfd9b76e0708e19e94897cdea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aae4933083cb3c7cd8a1bd0ce5f547b2f25ce6be5c9f5ab0f0cbf40db8bac03`

```dockerfile
```

-	Layers:
	-	`sha256:5ea793d24c52a96b076993e670b1d01dbd1f9f3ed75222d52f2a436bdeac477b`  
		Last Modified: Fri, 26 Jun 2026 17:54:15 GMT  
		Size: 27.1 KB (27064 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:97e8f72ba5ea68bae106dc03c39fcd7bb0eeaa0a1fa5b3403b3ea39b2bfa3381
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:943fdd9d6bafc53242d5ab2d2857b41f9ab8969dde7268fd33d380d03ae6e4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265176695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7ac6e6ee39b0bbd98fddd354104fc5798a4c5cf9ba560c2f074ccb02c42ecc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:43 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:43 GMT
ARG VERSION=26.3.15.4
# Fri, 26 Jun 2026 17:48:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:08 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:08 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:09 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38216c34971dba715121ac70e16c64042afc90e8ba74b1ec38601e47eb5d18da`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 7.6 MB (7555064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620737f98b2c2b28baaeb715e057822c54c3ac17763a32f2063b0944bf99ac4`  
		Last Modified: Fri, 26 Jun 2026 17:49:39 GMT  
		Size: 227.0 MB (227014894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e403cc00187b13b2ed2cb89cc5c4a942425ce2d5e42ffb06a25bb95a4bd08`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f2820a7bed2f24263b822edd2552d79c8204b27737832fe14957bda5f46dc3`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5459ef7da2345df368e41e7a127ac94d12e4c09bc30dede769c6d488977c721`  
		Last Modified: Fri, 26 Jun 2026 17:49:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9abffa579062c580b6b12358a3e0ad321124c23c7d6420577aa01ea99d7b48`  
		Last Modified: Fri, 26 Jun 2026 17:49:35 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8572df1a216f1627c9cac98c314d96fcdac6d32f361ec2e05d874da0f3d26203`  
		Last Modified: Fri, 26 Jun 2026 17:49:36 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:38463182a568ad43f21797199ad0a821010bab9b292010e77ef08bf6d0b351b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cddaad96ffb5d9257bbb54159f1057110220aa939ca4465b6022467f819470`

```dockerfile
```

-	Layers:
	-	`sha256:b1cba557c25f569db8a1f37e266f3981051019aef51d8698a745fc8867882b80`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 26.8 KB (26836 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:87ba1cec7d207db221a87afadbae9908b05e60c129e49123a66dc88ca4c1fd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246611660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7dcb539318c303284510428f79ae3b3ed165a4f6d1db2dd7443748d3180ec0b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:34 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:34 GMT
ARG VERSION=26.3.15.4
# Fri, 26 Jun 2026 17:53:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:54:00 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:54:00 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:54:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:54:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8a137aaa0902a87fb2cae745f866ee4a1c7908934a431dfb3a7146c032ac1`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 7.5 MB (7535269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a98ccb396d35d69ff41db54de6a8ffc02060dbcf8c5654f4b3ca3826141a21`  
		Last Modified: Fri, 26 Jun 2026 17:54:26 GMT  
		Size: 210.6 MB (210599719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ece11b79f8fe48a2dbe3cd3f13ca80e9c44e80ac2043a9a2d7641a2da83396e`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aebc0b3f40e42a3896fd2cf5777b4be657fffc9e5742514dda2f59728e83275`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44abb41eab15f74bb7625f8ffc079d7444cfead6ad401e1c29fe2f898c391f7`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fdd25aadbcfad460702922ee99ab4fe6365a32d33fbcc95245aa0be456a79`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdbd261ff900784ddbeeb91f1f57ae786a90a768b5eadf3dd147b211f2bc50b`  
		Last Modified: Fri, 26 Jun 2026 17:54:24 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:28c285e03cdabab87ffbdf61692940646bd26ece6500faef94cef4d10f12a4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f54c943e26a32b57061a001eeb5c9ddf0281057b0d7bcdfbe5bce15cfce1ec7`

```dockerfile
```

-	Layers:
	-	`sha256:9eee0a9398985ea52f2e4891a8e34f384d1006b45866ceb9cc45871305b004d4`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 27.0 KB (27047 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:97e8f72ba5ea68bae106dc03c39fcd7bb0eeaa0a1fa5b3403b3ea39b2bfa3381
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:943fdd9d6bafc53242d5ab2d2857b41f9ab8969dde7268fd33d380d03ae6e4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.2 MB (265176695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7ac6e6ee39b0bbd98fddd354104fc5798a4c5cf9ba560c2f074ccb02c42ecc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:49:21 GMT
ARG RELEASE
# Sat, 09 May 2026 04:49:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:49:21 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:49:23 GMT
ADD file:14c8897ef5107db11b35f5a0c05bdcb883c0a6daa83d07d4439865541f08514c in / 
# Sat, 09 May 2026 04:49:23 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:48:43 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:48:43 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:48:43 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:48:43 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:48:43 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:48:43 GMT
ARG VERSION=26.3.15.4
# Fri, 26 Jun 2026 17:48:43 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:49:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:49:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:49:08 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:49:08 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:49:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:49:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:49:09 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:49:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:49:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38216c34971dba715121ac70e16c64042afc90e8ba74b1ec38601e47eb5d18da`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 7.6 MB (7555064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620737f98b2c2b28baaeb715e057822c54c3ac17763a32f2063b0944bf99ac4`  
		Last Modified: Fri, 26 Jun 2026 17:49:39 GMT  
		Size: 227.0 MB (227014894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d1e403cc00187b13b2ed2cb89cc5c4a942425ce2d5e42ffb06a25bb95a4bd08`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2f2820a7bed2f24263b822edd2552d79c8204b27737832fe14957bda5f46dc3`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5459ef7da2345df368e41e7a127ac94d12e4c09bc30dede769c6d488977c721`  
		Last Modified: Fri, 26 Jun 2026 17:49:35 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9abffa579062c580b6b12358a3e0ad321124c23c7d6420577aa01ea99d7b48`  
		Last Modified: Fri, 26 Jun 2026 17:49:35 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8572df1a216f1627c9cac98c314d96fcdac6d32f361ec2e05d874da0f3d26203`  
		Last Modified: Fri, 26 Jun 2026 17:49:36 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:38463182a568ad43f21797199ad0a821010bab9b292010e77ef08bf6d0b351b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cddaad96ffb5d9257bbb54159f1057110220aa939ca4465b6022467f819470`

```dockerfile
```

-	Layers:
	-	`sha256:b1cba557c25f569db8a1f37e266f3981051019aef51d8698a745fc8867882b80`  
		Last Modified: Fri, 26 Jun 2026 17:49:34 GMT  
		Size: 26.8 KB (26836 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:87ba1cec7d207db221a87afadbae9908b05e60c129e49123a66dc88ca4c1fd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246611660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7dcb539318c303284510428f79ae3b3ed165a4f6d1db2dd7443748d3180ec0b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 09 May 2026 04:50:55 GMT
ARG RELEASE
# Sat, 09 May 2026 04:50:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 09 May 2026 04:50:55 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 09 May 2026 04:50:57 GMT
ADD file:a8d1411696ccaba92b4557162d508331f7cb7973e559947ad40c3f25d9402b10 in / 
# Sat, 09 May 2026 04:50:57 GMT
CMD ["/bin/bash"]
# Fri, 26 Jun 2026 17:53:34 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 26 Jun 2026 17:53:34 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 26 Jun 2026 17:53:34 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 26 Jun 2026 17:53:34 GMT
ARG REPO_CHANNEL=stable
# Fri, 26 Jun 2026 17:53:34 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 26 Jun 2026 17:53:34 GMT
ARG VERSION=26.3.15.4
# Fri, 26 Jun 2026 17:53:34 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 26 Jun 2026 17:53:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:53:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
ENV LANG=en_US.UTF-8
# Fri, 26 Jun 2026 17:54:00 GMT
ENV TZ=UTC
# Fri, 26 Jun 2026 17:54:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.15.4 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 26 Jun 2026 17:54:00 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 26 Jun 2026 17:54:00 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 26 Jun 2026 17:54:00 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 26 Jun 2026 17:54:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55a8a137aaa0902a87fb2cae745f866ee4a1c7908934a431dfb3a7146c032ac1`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 7.5 MB (7535269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a98ccb396d35d69ff41db54de6a8ffc02060dbcf8c5654f4b3ca3826141a21`  
		Last Modified: Fri, 26 Jun 2026 17:54:26 GMT  
		Size: 210.6 MB (210599719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ece11b79f8fe48a2dbe3cd3f13ca80e9c44e80ac2043a9a2d7641a2da83396e`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aebc0b3f40e42a3896fd2cf5777b4be657fffc9e5742514dda2f59728e83275`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44abb41eab15f74bb7625f8ffc079d7444cfead6ad401e1c29fe2f898c391f7`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e9fdd25aadbcfad460702922ee99ab4fe6365a32d33fbcc95245aa0be456a79`  
		Last Modified: Fri, 26 Jun 2026 17:54:23 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfdbd261ff900784ddbeeb91f1f57ae786a90a768b5eadf3dd147b211f2bc50b`  
		Last Modified: Fri, 26 Jun 2026 17:54:24 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:28c285e03cdabab87ffbdf61692940646bd26ece6500faef94cef4d10f12a4d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 KB (27047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f54c943e26a32b57061a001eeb5c9ddf0281057b0d7bcdfbe5bce15cfce1ec7`

```dockerfile
```

-	Layers:
	-	`sha256:9eee0a9398985ea52f2e4891a8e34f384d1006b45866ceb9cc45871305b004d4`  
		Last Modified: Fri, 26 Jun 2026 17:54:22 GMT  
		Size: 27.0 KB (27047 bytes)  
		MIME: application/vnd.in-toto+json
