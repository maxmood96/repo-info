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
-	[`clickhouse:26.3.12`](#clickhouse26312)
-	[`clickhouse:26.3.12-jammy`](#clickhouse26312-jammy)
-	[`clickhouse:26.3.12.3`](#clickhouse263123)
-	[`clickhouse:26.3.12.3-jammy`](#clickhouse263123-jammy)
-	[`clickhouse:26.4`](#clickhouse264)
-	[`clickhouse:26.4-jammy`](#clickhouse264-jammy)
-	[`clickhouse:26.4.3`](#clickhouse2643)
-	[`clickhouse:26.4.3-jammy`](#clickhouse2643-jammy)
-	[`clickhouse:26.4.3.37`](#clickhouse264337)
-	[`clickhouse:26.4.3.37-jammy`](#clickhouse264337-jammy)
-	[`clickhouse:26.5`](#clickhouse265)
-	[`clickhouse:26.5-jammy`](#clickhouse265-jammy)
-	[`clickhouse:26.5.1`](#clickhouse2651)
-	[`clickhouse:26.5.1-jammy`](#clickhouse2651-jammy)
-	[`clickhouse:26.5.1.882`](#clickhouse2651882)
-	[`clickhouse:26.5.1.882-jammy`](#clickhouse2651882-jammy)
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
$ docker pull clickhouse@sha256:0816d912717473854976f4c68cc869d119078cafd5639b66902e4afde57d8b8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:75b9d1ade272302ddfbdce179cf1ba2ae2ab9f42dfdf372e50b0130c0c25bff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264806066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159c355b977fff2e7e0899d85f4e35a94c1d52749b8dc8a5143dbce7d383c6d8`
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
# Fri, 15 May 2026 21:11:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:17 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:41 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:41 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7011ff31f15e81789181937898b770e8b20b75cf4ac3ef78b97441d3895c70`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 7.6 MB (7599287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36c3946d863cfb6aeabf8668540972aa93dd1d777428e719b09b1a2d1e39c31`  
		Last Modified: Fri, 15 May 2026 21:12:09 GMT  
		Size: 226.6 MB (226600051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d4144f9ed5a53a15944747b9467e80ba1dde55642fc88064fb7226612a373c`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da53b00944850a6ab3faf7cecc0e73e11c4bd0900b574b9eff650006b2ef9a08`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6532a2ef48b0172a1c83e184e13040f8e205d68ff052c2991ac28443438694aa`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b8fb6bfa5222d530fe781d4a428a54675a8eb4c1c49c099949efefd100b6ee`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03d873d57029deeaf43e26876afdc29cd14dad2f670531da07b6553cbf3a447`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4c3e22f4dd15fa758f2f94b8bedee58eced1dbee16e9f3ea5d12135a60bdc99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bf87ad8c04cf103c51c25a99ee5f06ae243ed357d37eff9e29671c3c73415b`

```dockerfile
```

-	Layers:
	-	`sha256:7291f19213dbdbd100fa399ee1f565dd83938a0e80d26182282b328a6ef08f82`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b888f4a4071d6e577c99d19d44acb5afe679862bbb38065a2efd4f19e87d5aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2b13e25b8289f6522e8a0b26d7f6f0b525e63565b9b3015b7bb666e0600e2e`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cc0127d140f4f8c2a885ded7884fa962d5608a5d20bd3a3b794c5c508553cd`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 7.6 MB (7578951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666017bd70a350c629f1f4092c945a7b1784d2461fb2dea8b1f18df61cfaf5c`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 210.2 MB (210218608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f297032f7c5cb81104c89b306611dd912900edc6da997eac7fc6d311b6d49`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e718e1bd582339ceed14e1c2affbb3fd7494d973c32fbe5733b19dcc07769d20`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35576b3658950c1a35f38c292b3a539ce0ca08972b9f88ff22530d9d09c3dac`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d85c621d654cd9ce41a7e1185c8ea3e3f3c4e8fee6ed505e7a8993e08e17dc`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cb445f6e3b234bab5117b35b93673292561e373afe668d0cd4c186a542fda`  
		Last Modified: Fri, 15 May 2026 21:12:20 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1113b00cddfa85f071107508d76a42d623e1f0ed7dd80cf3bb4d321dae039e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb3f778675a38b71cc10cd5549bf85eb6a50f3e603073c688eb53818f358bd1`

```dockerfile
```

-	Layers:
	-	`sha256:ba403868bf4d6c70f1b487bb61927529bba0717192a39e16d9b32151b4b9bf83`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3-jammy`

```console
$ docker pull clickhouse@sha256:0816d912717473854976f4c68cc869d119078cafd5639b66902e4afde57d8b8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:75b9d1ade272302ddfbdce179cf1ba2ae2ab9f42dfdf372e50b0130c0c25bff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264806066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159c355b977fff2e7e0899d85f4e35a94c1d52749b8dc8a5143dbce7d383c6d8`
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
# Fri, 15 May 2026 21:11:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:17 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:41 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:41 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7011ff31f15e81789181937898b770e8b20b75cf4ac3ef78b97441d3895c70`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 7.6 MB (7599287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36c3946d863cfb6aeabf8668540972aa93dd1d777428e719b09b1a2d1e39c31`  
		Last Modified: Fri, 15 May 2026 21:12:09 GMT  
		Size: 226.6 MB (226600051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d4144f9ed5a53a15944747b9467e80ba1dde55642fc88064fb7226612a373c`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da53b00944850a6ab3faf7cecc0e73e11c4bd0900b574b9eff650006b2ef9a08`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6532a2ef48b0172a1c83e184e13040f8e205d68ff052c2991ac28443438694aa`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b8fb6bfa5222d530fe781d4a428a54675a8eb4c1c49c099949efefd100b6ee`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03d873d57029deeaf43e26876afdc29cd14dad2f670531da07b6553cbf3a447`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4c3e22f4dd15fa758f2f94b8bedee58eced1dbee16e9f3ea5d12135a60bdc99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bf87ad8c04cf103c51c25a99ee5f06ae243ed357d37eff9e29671c3c73415b`

```dockerfile
```

-	Layers:
	-	`sha256:7291f19213dbdbd100fa399ee1f565dd83938a0e80d26182282b328a6ef08f82`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b888f4a4071d6e577c99d19d44acb5afe679862bbb38065a2efd4f19e87d5aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2b13e25b8289f6522e8a0b26d7f6f0b525e63565b9b3015b7bb666e0600e2e`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cc0127d140f4f8c2a885ded7884fa962d5608a5d20bd3a3b794c5c508553cd`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 7.6 MB (7578951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666017bd70a350c629f1f4092c945a7b1784d2461fb2dea8b1f18df61cfaf5c`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 210.2 MB (210218608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f297032f7c5cb81104c89b306611dd912900edc6da997eac7fc6d311b6d49`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e718e1bd582339ceed14e1c2affbb3fd7494d973c32fbe5733b19dcc07769d20`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35576b3658950c1a35f38c292b3a539ce0ca08972b9f88ff22530d9d09c3dac`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d85c621d654cd9ce41a7e1185c8ea3e3f3c4e8fee6ed505e7a8993e08e17dc`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cb445f6e3b234bab5117b35b93673292561e373afe668d0cd4c186a542fda`  
		Last Modified: Fri, 15 May 2026 21:12:20 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1113b00cddfa85f071107508d76a42d623e1f0ed7dd80cf3bb4d321dae039e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb3f778675a38b71cc10cd5549bf85eb6a50f3e603073c688eb53818f358bd1`

```dockerfile
```

-	Layers:
	-	`sha256:ba403868bf4d6c70f1b487bb61927529bba0717192a39e16d9b32151b4b9bf83`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.3.12`

**does not exist** (yet?)

## `clickhouse:26.3.12-jammy`

**does not exist** (yet?)

## `clickhouse:26.3.12.3`

**does not exist** (yet?)

## `clickhouse:26.3.12.3-jammy`

**does not exist** (yet?)

## `clickhouse:26.4`

```console
$ docker pull clickhouse@sha256:873ba11767d149d060edd52f410c98eb48be79d3e012cdf184b2b59d0c717c40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4` - linux; amd64

```console
$ docker pull clickhouse@sha256:3cda099914ec4fd33495e42093861ff00f494777c9e690712e269f1d5481b3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257167694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5ccd25d5ba7c9b2455c4d655be6679ab66b7893d4e3e68c069e378425c1beb`
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
# Fri, 22 May 2026 20:14:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:17 GMT
ARG VERSION=26.4.3.37
# Fri, 22 May 2026 20:14:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:41 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:42 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0db493d85c1eb4c72585bbe2ec7f4d290b717ec245cc5b29d86388796e64ac`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 7.6 MB (7599293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0a3c0f1622a9ccf324248018b5e911ecce0c6ddbf39be1f56d9522bc42e12d`  
		Last Modified: Fri, 22 May 2026 20:15:10 GMT  
		Size: 219.0 MB (218961670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e76819fc891a56a655a4f1e2e8dbdf3cf9186d7c40dad7df0bd1afac631dc2`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1625b7dc03fd21233cb08119490b4107e7a430e5c36807c2a4e69e4a6b7051`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a64469001e59a1aaa5d7fe00e430787e4acd36ae40294fbb621709e0878507`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545c72bcd040aadd58e5db23c8b45e5c6088adbfc56b45d8fa02e6a9826ef017`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e5089e5a7783210222c48830ef1ffb47fa9e31710dd42a2864e5c150a76d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea44876912603335a22993dd830f84c45f2df829f0f3f1c0c9bd1d8a0728a13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41643ee530b2a8a5d5261ea56300eac83137bbf0a8646038a2a1c055992c392`

```dockerfile
```

-	Layers:
	-	`sha256:88bbc6f0c094c8782e3fdafc1c15e35b88fb98a8c775bacde6c3258fb726efd8`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4cc78aa48a3f4226f73bfb0c3a3e9b9eed15e052ea46980fa5a08d6cdc909ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240979988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bfe92ae84834a846b7dc33a6111d43fbb090a8078ffc16aaba68cb5c6d3f443`
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
# Fri, 22 May 2026 20:14:12 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:12 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:12 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:12 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:12 GMT
ARG VERSION=26.4.3.37
# Fri, 22 May 2026 20:14:12 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:38 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631ef5c9eb7f10c5423689961c622ac46c44b9c0bd2382f5f1e39451cc5cf1b6`  
		Last Modified: Fri, 22 May 2026 20:15:01 GMT  
		Size: 7.6 MB (7578931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de521df4cb86db81920b12f54a8b826fb099c6a5422bfdfecee7c74811b6ff5`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 204.9 MB (204924384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39283df4009c295bb245cfa2fe546eeff40047367ff3a85b444c711dc21cb1d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00bb2b95ec9ef3dc794fd02410cb174ccf1c7dbbe41eba68f5b1704564b6562`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b9f0464f230f04f980382fb8c3d8ff2bf5fcc005e6d175509e0a45edf8dfde`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe929808ea533fd9ec3d3def9ba1be2b75ec807910662d105b42937d7f5c593`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d30b96c821de60360fe077b437002fa0fa5f585a94816b130ba5deece55879`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bb575c107ddad8dca9981fa80a3dbaa30ec9ea68b638c40a5fc8fd2f41831f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d840a511b82a6129e4653080f4055be2cdc08a4db35a657bdcb6c913cea98e`

```dockerfile
```

-	Layers:
	-	`sha256:d3c7e38cba108738fbccab17421caa78b6f63c9d36970fed159ba09ba99483d5`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4-jammy`

```console
$ docker pull clickhouse@sha256:873ba11767d149d060edd52f410c98eb48be79d3e012cdf184b2b59d0c717c40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:3cda099914ec4fd33495e42093861ff00f494777c9e690712e269f1d5481b3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257167694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5ccd25d5ba7c9b2455c4d655be6679ab66b7893d4e3e68c069e378425c1beb`
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
# Fri, 22 May 2026 20:14:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:17 GMT
ARG VERSION=26.4.3.37
# Fri, 22 May 2026 20:14:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:41 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:42 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0db493d85c1eb4c72585bbe2ec7f4d290b717ec245cc5b29d86388796e64ac`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 7.6 MB (7599293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0a3c0f1622a9ccf324248018b5e911ecce0c6ddbf39be1f56d9522bc42e12d`  
		Last Modified: Fri, 22 May 2026 20:15:10 GMT  
		Size: 219.0 MB (218961670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e76819fc891a56a655a4f1e2e8dbdf3cf9186d7c40dad7df0bd1afac631dc2`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1625b7dc03fd21233cb08119490b4107e7a430e5c36807c2a4e69e4a6b7051`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a64469001e59a1aaa5d7fe00e430787e4acd36ae40294fbb621709e0878507`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545c72bcd040aadd58e5db23c8b45e5c6088adbfc56b45d8fa02e6a9826ef017`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e5089e5a7783210222c48830ef1ffb47fa9e31710dd42a2864e5c150a76d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea44876912603335a22993dd830f84c45f2df829f0f3f1c0c9bd1d8a0728a13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41643ee530b2a8a5d5261ea56300eac83137bbf0a8646038a2a1c055992c392`

```dockerfile
```

-	Layers:
	-	`sha256:88bbc6f0c094c8782e3fdafc1c15e35b88fb98a8c775bacde6c3258fb726efd8`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4cc78aa48a3f4226f73bfb0c3a3e9b9eed15e052ea46980fa5a08d6cdc909ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240979988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bfe92ae84834a846b7dc33a6111d43fbb090a8078ffc16aaba68cb5c6d3f443`
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
# Fri, 22 May 2026 20:14:12 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:12 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:12 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:12 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:12 GMT
ARG VERSION=26.4.3.37
# Fri, 22 May 2026 20:14:12 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:38 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631ef5c9eb7f10c5423689961c622ac46c44b9c0bd2382f5f1e39451cc5cf1b6`  
		Last Modified: Fri, 22 May 2026 20:15:01 GMT  
		Size: 7.6 MB (7578931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de521df4cb86db81920b12f54a8b826fb099c6a5422bfdfecee7c74811b6ff5`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 204.9 MB (204924384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39283df4009c295bb245cfa2fe546eeff40047367ff3a85b444c711dc21cb1d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00bb2b95ec9ef3dc794fd02410cb174ccf1c7dbbe41eba68f5b1704564b6562`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b9f0464f230f04f980382fb8c3d8ff2bf5fcc005e6d175509e0a45edf8dfde`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe929808ea533fd9ec3d3def9ba1be2b75ec807910662d105b42937d7f5c593`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d30b96c821de60360fe077b437002fa0fa5f585a94816b130ba5deece55879`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bb575c107ddad8dca9981fa80a3dbaa30ec9ea68b638c40a5fc8fd2f41831f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d840a511b82a6129e4653080f4055be2cdc08a4db35a657bdcb6c913cea98e`

```dockerfile
```

-	Layers:
	-	`sha256:d3c7e38cba108738fbccab17421caa78b6f63c9d36970fed159ba09ba99483d5`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4.3`

```console
$ docker pull clickhouse@sha256:873ba11767d149d060edd52f410c98eb48be79d3e012cdf184b2b59d0c717c40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:3cda099914ec4fd33495e42093861ff00f494777c9e690712e269f1d5481b3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257167694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5ccd25d5ba7c9b2455c4d655be6679ab66b7893d4e3e68c069e378425c1beb`
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
# Fri, 22 May 2026 20:14:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:17 GMT
ARG VERSION=26.4.3.37
# Fri, 22 May 2026 20:14:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:41 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:42 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0db493d85c1eb4c72585bbe2ec7f4d290b717ec245cc5b29d86388796e64ac`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 7.6 MB (7599293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0a3c0f1622a9ccf324248018b5e911ecce0c6ddbf39be1f56d9522bc42e12d`  
		Last Modified: Fri, 22 May 2026 20:15:10 GMT  
		Size: 219.0 MB (218961670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e76819fc891a56a655a4f1e2e8dbdf3cf9186d7c40dad7df0bd1afac631dc2`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1625b7dc03fd21233cb08119490b4107e7a430e5c36807c2a4e69e4a6b7051`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a64469001e59a1aaa5d7fe00e430787e4acd36ae40294fbb621709e0878507`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545c72bcd040aadd58e5db23c8b45e5c6088adbfc56b45d8fa02e6a9826ef017`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e5089e5a7783210222c48830ef1ffb47fa9e31710dd42a2864e5c150a76d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea44876912603335a22993dd830f84c45f2df829f0f3f1c0c9bd1d8a0728a13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41643ee530b2a8a5d5261ea56300eac83137bbf0a8646038a2a1c055992c392`

```dockerfile
```

-	Layers:
	-	`sha256:88bbc6f0c094c8782e3fdafc1c15e35b88fb98a8c775bacde6c3258fb726efd8`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4cc78aa48a3f4226f73bfb0c3a3e9b9eed15e052ea46980fa5a08d6cdc909ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240979988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bfe92ae84834a846b7dc33a6111d43fbb090a8078ffc16aaba68cb5c6d3f443`
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
# Fri, 22 May 2026 20:14:12 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:12 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:12 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:12 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:12 GMT
ARG VERSION=26.4.3.37
# Fri, 22 May 2026 20:14:12 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:38 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631ef5c9eb7f10c5423689961c622ac46c44b9c0bd2382f5f1e39451cc5cf1b6`  
		Last Modified: Fri, 22 May 2026 20:15:01 GMT  
		Size: 7.6 MB (7578931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de521df4cb86db81920b12f54a8b826fb099c6a5422bfdfecee7c74811b6ff5`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 204.9 MB (204924384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39283df4009c295bb245cfa2fe546eeff40047367ff3a85b444c711dc21cb1d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00bb2b95ec9ef3dc794fd02410cb174ccf1c7dbbe41eba68f5b1704564b6562`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b9f0464f230f04f980382fb8c3d8ff2bf5fcc005e6d175509e0a45edf8dfde`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe929808ea533fd9ec3d3def9ba1be2b75ec807910662d105b42937d7f5c593`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d30b96c821de60360fe077b437002fa0fa5f585a94816b130ba5deece55879`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bb575c107ddad8dca9981fa80a3dbaa30ec9ea68b638c40a5fc8fd2f41831f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d840a511b82a6129e4653080f4055be2cdc08a4db35a657bdcb6c913cea98e`

```dockerfile
```

-	Layers:
	-	`sha256:d3c7e38cba108738fbccab17421caa78b6f63c9d36970fed159ba09ba99483d5`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4.3-jammy`

```console
$ docker pull clickhouse@sha256:873ba11767d149d060edd52f410c98eb48be79d3e012cdf184b2b59d0c717c40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:3cda099914ec4fd33495e42093861ff00f494777c9e690712e269f1d5481b3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257167694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5ccd25d5ba7c9b2455c4d655be6679ab66b7893d4e3e68c069e378425c1beb`
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
# Fri, 22 May 2026 20:14:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:17 GMT
ARG VERSION=26.4.3.37
# Fri, 22 May 2026 20:14:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:41 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:42 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0db493d85c1eb4c72585bbe2ec7f4d290b717ec245cc5b29d86388796e64ac`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 7.6 MB (7599293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0a3c0f1622a9ccf324248018b5e911ecce0c6ddbf39be1f56d9522bc42e12d`  
		Last Modified: Fri, 22 May 2026 20:15:10 GMT  
		Size: 219.0 MB (218961670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e76819fc891a56a655a4f1e2e8dbdf3cf9186d7c40dad7df0bd1afac631dc2`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1625b7dc03fd21233cb08119490b4107e7a430e5c36807c2a4e69e4a6b7051`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a64469001e59a1aaa5d7fe00e430787e4acd36ae40294fbb621709e0878507`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545c72bcd040aadd58e5db23c8b45e5c6088adbfc56b45d8fa02e6a9826ef017`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e5089e5a7783210222c48830ef1ffb47fa9e31710dd42a2864e5c150a76d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea44876912603335a22993dd830f84c45f2df829f0f3f1c0c9bd1d8a0728a13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41643ee530b2a8a5d5261ea56300eac83137bbf0a8646038a2a1c055992c392`

```dockerfile
```

-	Layers:
	-	`sha256:88bbc6f0c094c8782e3fdafc1c15e35b88fb98a8c775bacde6c3258fb726efd8`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4cc78aa48a3f4226f73bfb0c3a3e9b9eed15e052ea46980fa5a08d6cdc909ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240979988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bfe92ae84834a846b7dc33a6111d43fbb090a8078ffc16aaba68cb5c6d3f443`
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
# Fri, 22 May 2026 20:14:12 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:12 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:12 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:12 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:12 GMT
ARG VERSION=26.4.3.37
# Fri, 22 May 2026 20:14:12 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:38 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631ef5c9eb7f10c5423689961c622ac46c44b9c0bd2382f5f1e39451cc5cf1b6`  
		Last Modified: Fri, 22 May 2026 20:15:01 GMT  
		Size: 7.6 MB (7578931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de521df4cb86db81920b12f54a8b826fb099c6a5422bfdfecee7c74811b6ff5`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 204.9 MB (204924384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39283df4009c295bb245cfa2fe546eeff40047367ff3a85b444c711dc21cb1d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00bb2b95ec9ef3dc794fd02410cb174ccf1c7dbbe41eba68f5b1704564b6562`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b9f0464f230f04f980382fb8c3d8ff2bf5fcc005e6d175509e0a45edf8dfde`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe929808ea533fd9ec3d3def9ba1be2b75ec807910662d105b42937d7f5c593`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d30b96c821de60360fe077b437002fa0fa5f585a94816b130ba5deece55879`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bb575c107ddad8dca9981fa80a3dbaa30ec9ea68b638c40a5fc8fd2f41831f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d840a511b82a6129e4653080f4055be2cdc08a4db35a657bdcb6c913cea98e`

```dockerfile
```

-	Layers:
	-	`sha256:d3c7e38cba108738fbccab17421caa78b6f63c9d36970fed159ba09ba99483d5`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4.3.37`

```console
$ docker pull clickhouse@sha256:873ba11767d149d060edd52f410c98eb48be79d3e012cdf184b2b59d0c717c40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4.3.37` - linux; amd64

```console
$ docker pull clickhouse@sha256:3cda099914ec4fd33495e42093861ff00f494777c9e690712e269f1d5481b3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257167694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5ccd25d5ba7c9b2455c4d655be6679ab66b7893d4e3e68c069e378425c1beb`
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
# Fri, 22 May 2026 20:14:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:17 GMT
ARG VERSION=26.4.3.37
# Fri, 22 May 2026 20:14:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:41 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:42 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0db493d85c1eb4c72585bbe2ec7f4d290b717ec245cc5b29d86388796e64ac`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 7.6 MB (7599293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0a3c0f1622a9ccf324248018b5e911ecce0c6ddbf39be1f56d9522bc42e12d`  
		Last Modified: Fri, 22 May 2026 20:15:10 GMT  
		Size: 219.0 MB (218961670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e76819fc891a56a655a4f1e2e8dbdf3cf9186d7c40dad7df0bd1afac631dc2`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1625b7dc03fd21233cb08119490b4107e7a430e5c36807c2a4e69e4a6b7051`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a64469001e59a1aaa5d7fe00e430787e4acd36ae40294fbb621709e0878507`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545c72bcd040aadd58e5db23c8b45e5c6088adbfc56b45d8fa02e6a9826ef017`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e5089e5a7783210222c48830ef1ffb47fa9e31710dd42a2864e5c150a76d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.3.37` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea44876912603335a22993dd830f84c45f2df829f0f3f1c0c9bd1d8a0728a13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41643ee530b2a8a5d5261ea56300eac83137bbf0a8646038a2a1c055992c392`

```dockerfile
```

-	Layers:
	-	`sha256:88bbc6f0c094c8782e3fdafc1c15e35b88fb98a8c775bacde6c3258fb726efd8`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4.3.37` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4cc78aa48a3f4226f73bfb0c3a3e9b9eed15e052ea46980fa5a08d6cdc909ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240979988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bfe92ae84834a846b7dc33a6111d43fbb090a8078ffc16aaba68cb5c6d3f443`
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
# Fri, 22 May 2026 20:14:12 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:12 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:12 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:12 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:12 GMT
ARG VERSION=26.4.3.37
# Fri, 22 May 2026 20:14:12 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:38 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631ef5c9eb7f10c5423689961c622ac46c44b9c0bd2382f5f1e39451cc5cf1b6`  
		Last Modified: Fri, 22 May 2026 20:15:01 GMT  
		Size: 7.6 MB (7578931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de521df4cb86db81920b12f54a8b826fb099c6a5422bfdfecee7c74811b6ff5`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 204.9 MB (204924384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39283df4009c295bb245cfa2fe546eeff40047367ff3a85b444c711dc21cb1d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00bb2b95ec9ef3dc794fd02410cb174ccf1c7dbbe41eba68f5b1704564b6562`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b9f0464f230f04f980382fb8c3d8ff2bf5fcc005e6d175509e0a45edf8dfde`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe929808ea533fd9ec3d3def9ba1be2b75ec807910662d105b42937d7f5c593`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d30b96c821de60360fe077b437002fa0fa5f585a94816b130ba5deece55879`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.3.37` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bb575c107ddad8dca9981fa80a3dbaa30ec9ea68b638c40a5fc8fd2f41831f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d840a511b82a6129e4653080f4055be2cdc08a4db35a657bdcb6c913cea98e`

```dockerfile
```

-	Layers:
	-	`sha256:d3c7e38cba108738fbccab17421caa78b6f63c9d36970fed159ba09ba99483d5`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.4.3.37-jammy`

```console
$ docker pull clickhouse@sha256:873ba11767d149d060edd52f410c98eb48be79d3e012cdf184b2b59d0c717c40
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.4.3.37-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:3cda099914ec4fd33495e42093861ff00f494777c9e690712e269f1d5481b3b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257167694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc5ccd25d5ba7c9b2455c4d655be6679ab66b7893d4e3e68c069e378425c1beb`
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
# Fri, 22 May 2026 20:14:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:17 GMT
ARG VERSION=26.4.3.37
# Fri, 22 May 2026 20:14:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:41 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:42 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d0db493d85c1eb4c72585bbe2ec7f4d290b717ec245cc5b29d86388796e64ac`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 7.6 MB (7599293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0a3c0f1622a9ccf324248018b5e911ecce0c6ddbf39be1f56d9522bc42e12d`  
		Last Modified: Fri, 22 May 2026 20:15:10 GMT  
		Size: 219.0 MB (218961670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e76819fc891a56a655a4f1e2e8dbdf3cf9186d7c40dad7df0bd1afac631dc2`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1625b7dc03fd21233cb08119490b4107e7a430e5c36807c2a4e69e4a6b7051`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a64469001e59a1aaa5d7fe00e430787e4acd36ae40294fbb621709e0878507`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545c72bcd040aadd58e5db23c8b45e5c6088adbfc56b45d8fa02e6a9826ef017`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e5089e5a7783210222c48830ef1ffb47fa9e31710dd42a2864e5c150a76d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.3.37-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ea44876912603335a22993dd830f84c45f2df829f0f3f1c0c9bd1d8a0728a13d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41643ee530b2a8a5d5261ea56300eac83137bbf0a8646038a2a1c055992c392`

```dockerfile
```

-	Layers:
	-	`sha256:88bbc6f0c094c8782e3fdafc1c15e35b88fb98a8c775bacde6c3258fb726efd8`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 26.2 KB (26220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.4.3.37-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4cc78aa48a3f4226f73bfb0c3a3e9b9eed15e052ea46980fa5a08d6cdc909ef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240979988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bfe92ae84834a846b7dc33a6111d43fbb090a8078ffc16aaba68cb5c6d3f443`
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
# Fri, 22 May 2026 20:14:12 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:12 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:12 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:12 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:12 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:12 GMT
ARG VERSION=26.4.3.37
# Fri, 22 May 2026 20:14:12 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:38 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:38 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.4.3.37 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:38 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:38 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:38 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:38 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:38 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631ef5c9eb7f10c5423689961c622ac46c44b9c0bd2382f5f1e39451cc5cf1b6`  
		Last Modified: Fri, 22 May 2026 20:15:01 GMT  
		Size: 7.6 MB (7578931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de521df4cb86db81920b12f54a8b826fb099c6a5422bfdfecee7c74811b6ff5`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 204.9 MB (204924384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39283df4009c295bb245cfa2fe546eeff40047367ff3a85b444c711dc21cb1d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00bb2b95ec9ef3dc794fd02410cb174ccf1c7dbbe41eba68f5b1704564b6562`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b9f0464f230f04f980382fb8c3d8ff2bf5fcc005e6d175509e0a45edf8dfde`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe929808ea533fd9ec3d3def9ba1be2b75ec807910662d105b42937d7f5c593`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d30b96c821de60360fe077b437002fa0fa5f585a94816b130ba5deece55879`  
		Last Modified: Fri, 22 May 2026 20:15:02 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.4.3.37-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bb575c107ddad8dca9981fa80a3dbaa30ec9ea68b638c40a5fc8fd2f41831f2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d840a511b82a6129e4653080f4055be2cdc08a4db35a657bdcb6c913cea98e`

```dockerfile
```

-	Layers:
	-	`sha256:d3c7e38cba108738fbccab17421caa78b6f63c9d36970fed159ba09ba99483d5`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 26.4 KB (26408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.5`

```console
$ docker pull clickhouse@sha256:770156c537ca9124046e138a3b5845c64ea58ce8722de7a2e05fd827f4976520
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:8d1bc439fd25e27e0719e3906189346621d3b30c3a1fce590f74df9e36ba1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261148941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ddf6fea0767ca6ece44e8bb8bebb226e1a2ce0650ff586d88bac748c91a5cc`
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
# Fri, 22 May 2026 20:14:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:13 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:39 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e180166c8efb533aaa3022823135bb6c8670b51d51f9fbc4d2f90a55107a9e`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 7.6 MB (7599255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1688ec152117f8ed0385e04486a1641ca44a13c333296f61f178c5bc149e57`  
		Last Modified: Fri, 22 May 2026 20:15:10 GMT  
		Size: 222.9 MB (222942955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530779b308d06014dc910f38ba3490dec2bdcca6e10781d2ab7a9ba99b865b36`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95592b500ee480fa70d1788e644c926270cc19e6dac6e7fc9d316053720b7a8f`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a80d826b2d9a7917270a5ebfc22fe4d95f9e6e822570ca073b157254798be5`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bf2de4fcdd30475c64afde6bbb742172517789fa890768e3cefa610227366`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4255ed0b8e5159dea3c2b93b37f0d4b795441100e719b8397c8f1b503ec27dce`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fe7ada49ccbfdb9f6156dcb2cd793fb050fe90dad55a33a7215604d783d0f45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787a9e4add1ea2d4690fd9ea7e6460ff1af96e7832168d2a7a02e798f9662745`

```dockerfile
```

-	Layers:
	-	`sha256:693f1c4a6051d189a846b168f4c9c5d7ad3592da8de5398429f4bbd31e9c3d3a`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 26.8 KB (26841 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:524e8364d7f9ac6839ec1c28db6edb4a5e41e6300cf1e2d5d1e13d3ddee72b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247055149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c881ac185dd2f404d2cee0c6e6ddf22c6c114b86b1d352db71fee93578da68`
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
# Fri, 22 May 2026 20:14:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:10 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:37 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:37 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:37 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:37 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64e86572324aa7eea2f61ea517db418403a7c9976b5d5ad7ec53f58db355941`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 7.6 MB (7578895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a15579d25cd8cffa07921868d5b209add90eb5919bc8c684b4ad5e8a51fe268`  
		Last Modified: Fri, 22 May 2026 20:15:03 GMT  
		Size: 211.0 MB (210999581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9628bf90ea72b5639b183121fa70adc2a3166f0f8b61dc64da557941faa4e889`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225291cf0df1a4ddb0e6c2efff7a08245ded5936d36da4db1fd512cf245badec`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be41faac692e17e0c8ebef7ec6d284a9d9fa553251e68a3806718719e6ab8d4c`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530f5f7fab3df30aee408ad771090089db66c4155964fc72c06e06b3bf3731a3`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e5089e5a7783210222c48830ef1ffb47fa9e31710dd42a2864e5c150a76d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5fda5509e5a7bd55544537246507374514e8551464ea9026eeb27b7d2afbb812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1237ad33491107f44515a662c43c3704d7f2028c202c1aa115967da20adb13`

```dockerfile
```

-	Layers:
	-	`sha256:accb5a6fedc2950811e0026389469e1d6c5acfe87f3fe0ef71fe9c7c1d5cf595`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 27.1 KB (27053 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.5-jammy`

```console
$ docker pull clickhouse@sha256:770156c537ca9124046e138a3b5845c64ea58ce8722de7a2e05fd827f4976520
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8d1bc439fd25e27e0719e3906189346621d3b30c3a1fce590f74df9e36ba1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261148941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ddf6fea0767ca6ece44e8bb8bebb226e1a2ce0650ff586d88bac748c91a5cc`
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
# Fri, 22 May 2026 20:14:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:13 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:39 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e180166c8efb533aaa3022823135bb6c8670b51d51f9fbc4d2f90a55107a9e`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 7.6 MB (7599255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1688ec152117f8ed0385e04486a1641ca44a13c333296f61f178c5bc149e57`  
		Last Modified: Fri, 22 May 2026 20:15:10 GMT  
		Size: 222.9 MB (222942955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530779b308d06014dc910f38ba3490dec2bdcca6e10781d2ab7a9ba99b865b36`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95592b500ee480fa70d1788e644c926270cc19e6dac6e7fc9d316053720b7a8f`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a80d826b2d9a7917270a5ebfc22fe4d95f9e6e822570ca073b157254798be5`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bf2de4fcdd30475c64afde6bbb742172517789fa890768e3cefa610227366`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4255ed0b8e5159dea3c2b93b37f0d4b795441100e719b8397c8f1b503ec27dce`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fe7ada49ccbfdb9f6156dcb2cd793fb050fe90dad55a33a7215604d783d0f45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787a9e4add1ea2d4690fd9ea7e6460ff1af96e7832168d2a7a02e798f9662745`

```dockerfile
```

-	Layers:
	-	`sha256:693f1c4a6051d189a846b168f4c9c5d7ad3592da8de5398429f4bbd31e9c3d3a`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 26.8 KB (26841 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:524e8364d7f9ac6839ec1c28db6edb4a5e41e6300cf1e2d5d1e13d3ddee72b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247055149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c881ac185dd2f404d2cee0c6e6ddf22c6c114b86b1d352db71fee93578da68`
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
# Fri, 22 May 2026 20:14:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:10 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:37 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:37 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:37 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:37 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64e86572324aa7eea2f61ea517db418403a7c9976b5d5ad7ec53f58db355941`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 7.6 MB (7578895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a15579d25cd8cffa07921868d5b209add90eb5919bc8c684b4ad5e8a51fe268`  
		Last Modified: Fri, 22 May 2026 20:15:03 GMT  
		Size: 211.0 MB (210999581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9628bf90ea72b5639b183121fa70adc2a3166f0f8b61dc64da557941faa4e889`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225291cf0df1a4ddb0e6c2efff7a08245ded5936d36da4db1fd512cf245badec`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be41faac692e17e0c8ebef7ec6d284a9d9fa553251e68a3806718719e6ab8d4c`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530f5f7fab3df30aee408ad771090089db66c4155964fc72c06e06b3bf3731a3`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e5089e5a7783210222c48830ef1ffb47fa9e31710dd42a2864e5c150a76d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5fda5509e5a7bd55544537246507374514e8551464ea9026eeb27b7d2afbb812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1237ad33491107f44515a662c43c3704d7f2028c202c1aa115967da20adb13`

```dockerfile
```

-	Layers:
	-	`sha256:accb5a6fedc2950811e0026389469e1d6c5acfe87f3fe0ef71fe9c7c1d5cf595`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 27.1 KB (27053 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.5.1`

```console
$ docker pull clickhouse@sha256:770156c537ca9124046e138a3b5845c64ea58ce8722de7a2e05fd827f4976520
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.5.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:8d1bc439fd25e27e0719e3906189346621d3b30c3a1fce590f74df9e36ba1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261148941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ddf6fea0767ca6ece44e8bb8bebb226e1a2ce0650ff586d88bac748c91a5cc`
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
# Fri, 22 May 2026 20:14:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:13 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:39 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e180166c8efb533aaa3022823135bb6c8670b51d51f9fbc4d2f90a55107a9e`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 7.6 MB (7599255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1688ec152117f8ed0385e04486a1641ca44a13c333296f61f178c5bc149e57`  
		Last Modified: Fri, 22 May 2026 20:15:10 GMT  
		Size: 222.9 MB (222942955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530779b308d06014dc910f38ba3490dec2bdcca6e10781d2ab7a9ba99b865b36`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95592b500ee480fa70d1788e644c926270cc19e6dac6e7fc9d316053720b7a8f`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a80d826b2d9a7917270a5ebfc22fe4d95f9e6e822570ca073b157254798be5`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bf2de4fcdd30475c64afde6bbb742172517789fa890768e3cefa610227366`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4255ed0b8e5159dea3c2b93b37f0d4b795441100e719b8397c8f1b503ec27dce`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fe7ada49ccbfdb9f6156dcb2cd793fb050fe90dad55a33a7215604d783d0f45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787a9e4add1ea2d4690fd9ea7e6460ff1af96e7832168d2a7a02e798f9662745`

```dockerfile
```

-	Layers:
	-	`sha256:693f1c4a6051d189a846b168f4c9c5d7ad3592da8de5398429f4bbd31e9c3d3a`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 26.8 KB (26841 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.5.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:524e8364d7f9ac6839ec1c28db6edb4a5e41e6300cf1e2d5d1e13d3ddee72b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247055149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c881ac185dd2f404d2cee0c6e6ddf22c6c114b86b1d352db71fee93578da68`
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
# Fri, 22 May 2026 20:14:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:10 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:37 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:37 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:37 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:37 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64e86572324aa7eea2f61ea517db418403a7c9976b5d5ad7ec53f58db355941`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 7.6 MB (7578895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a15579d25cd8cffa07921868d5b209add90eb5919bc8c684b4ad5e8a51fe268`  
		Last Modified: Fri, 22 May 2026 20:15:03 GMT  
		Size: 211.0 MB (210999581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9628bf90ea72b5639b183121fa70adc2a3166f0f8b61dc64da557941faa4e889`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225291cf0df1a4ddb0e6c2efff7a08245ded5936d36da4db1fd512cf245badec`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be41faac692e17e0c8ebef7ec6d284a9d9fa553251e68a3806718719e6ab8d4c`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530f5f7fab3df30aee408ad771090089db66c4155964fc72c06e06b3bf3731a3`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e5089e5a7783210222c48830ef1ffb47fa9e31710dd42a2864e5c150a76d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5fda5509e5a7bd55544537246507374514e8551464ea9026eeb27b7d2afbb812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1237ad33491107f44515a662c43c3704d7f2028c202c1aa115967da20adb13`

```dockerfile
```

-	Layers:
	-	`sha256:accb5a6fedc2950811e0026389469e1d6c5acfe87f3fe0ef71fe9c7c1d5cf595`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 27.1 KB (27053 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.5.1-jammy`

```console
$ docker pull clickhouse@sha256:770156c537ca9124046e138a3b5845c64ea58ce8722de7a2e05fd827f4976520
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.5.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8d1bc439fd25e27e0719e3906189346621d3b30c3a1fce590f74df9e36ba1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261148941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ddf6fea0767ca6ece44e8bb8bebb226e1a2ce0650ff586d88bac748c91a5cc`
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
# Fri, 22 May 2026 20:14:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:13 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:39 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e180166c8efb533aaa3022823135bb6c8670b51d51f9fbc4d2f90a55107a9e`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 7.6 MB (7599255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1688ec152117f8ed0385e04486a1641ca44a13c333296f61f178c5bc149e57`  
		Last Modified: Fri, 22 May 2026 20:15:10 GMT  
		Size: 222.9 MB (222942955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530779b308d06014dc910f38ba3490dec2bdcca6e10781d2ab7a9ba99b865b36`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95592b500ee480fa70d1788e644c926270cc19e6dac6e7fc9d316053720b7a8f`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a80d826b2d9a7917270a5ebfc22fe4d95f9e6e822570ca073b157254798be5`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bf2de4fcdd30475c64afde6bbb742172517789fa890768e3cefa610227366`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4255ed0b8e5159dea3c2b93b37f0d4b795441100e719b8397c8f1b503ec27dce`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fe7ada49ccbfdb9f6156dcb2cd793fb050fe90dad55a33a7215604d783d0f45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787a9e4add1ea2d4690fd9ea7e6460ff1af96e7832168d2a7a02e798f9662745`

```dockerfile
```

-	Layers:
	-	`sha256:693f1c4a6051d189a846b168f4c9c5d7ad3592da8de5398429f4bbd31e9c3d3a`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 26.8 KB (26841 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.5.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:524e8364d7f9ac6839ec1c28db6edb4a5e41e6300cf1e2d5d1e13d3ddee72b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247055149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c881ac185dd2f404d2cee0c6e6ddf22c6c114b86b1d352db71fee93578da68`
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
# Fri, 22 May 2026 20:14:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:10 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:37 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:37 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:37 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:37 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64e86572324aa7eea2f61ea517db418403a7c9976b5d5ad7ec53f58db355941`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 7.6 MB (7578895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a15579d25cd8cffa07921868d5b209add90eb5919bc8c684b4ad5e8a51fe268`  
		Last Modified: Fri, 22 May 2026 20:15:03 GMT  
		Size: 211.0 MB (210999581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9628bf90ea72b5639b183121fa70adc2a3166f0f8b61dc64da557941faa4e889`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225291cf0df1a4ddb0e6c2efff7a08245ded5936d36da4db1fd512cf245badec`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be41faac692e17e0c8ebef7ec6d284a9d9fa553251e68a3806718719e6ab8d4c`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530f5f7fab3df30aee408ad771090089db66c4155964fc72c06e06b3bf3731a3`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e5089e5a7783210222c48830ef1ffb47fa9e31710dd42a2864e5c150a76d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5fda5509e5a7bd55544537246507374514e8551464ea9026eeb27b7d2afbb812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1237ad33491107f44515a662c43c3704d7f2028c202c1aa115967da20adb13`

```dockerfile
```

-	Layers:
	-	`sha256:accb5a6fedc2950811e0026389469e1d6c5acfe87f3fe0ef71fe9c7c1d5cf595`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 27.1 KB (27053 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.5.1.882`

```console
$ docker pull clickhouse@sha256:770156c537ca9124046e138a3b5845c64ea58ce8722de7a2e05fd827f4976520
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.5.1.882` - linux; amd64

```console
$ docker pull clickhouse@sha256:8d1bc439fd25e27e0719e3906189346621d3b30c3a1fce590f74df9e36ba1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261148941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ddf6fea0767ca6ece44e8bb8bebb226e1a2ce0650ff586d88bac748c91a5cc`
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
# Fri, 22 May 2026 20:14:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:13 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:39 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e180166c8efb533aaa3022823135bb6c8670b51d51f9fbc4d2f90a55107a9e`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 7.6 MB (7599255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1688ec152117f8ed0385e04486a1641ca44a13c333296f61f178c5bc149e57`  
		Last Modified: Fri, 22 May 2026 20:15:10 GMT  
		Size: 222.9 MB (222942955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530779b308d06014dc910f38ba3490dec2bdcca6e10781d2ab7a9ba99b865b36`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95592b500ee480fa70d1788e644c926270cc19e6dac6e7fc9d316053720b7a8f`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a80d826b2d9a7917270a5ebfc22fe4d95f9e6e822570ca073b157254798be5`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bf2de4fcdd30475c64afde6bbb742172517789fa890768e3cefa610227366`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4255ed0b8e5159dea3c2b93b37f0d4b795441100e719b8397c8f1b503ec27dce`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5.1.882` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fe7ada49ccbfdb9f6156dcb2cd793fb050fe90dad55a33a7215604d783d0f45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787a9e4add1ea2d4690fd9ea7e6460ff1af96e7832168d2a7a02e798f9662745`

```dockerfile
```

-	Layers:
	-	`sha256:693f1c4a6051d189a846b168f4c9c5d7ad3592da8de5398429f4bbd31e9c3d3a`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 26.8 KB (26841 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.5.1.882` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:524e8364d7f9ac6839ec1c28db6edb4a5e41e6300cf1e2d5d1e13d3ddee72b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247055149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c881ac185dd2f404d2cee0c6e6ddf22c6c114b86b1d352db71fee93578da68`
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
# Fri, 22 May 2026 20:14:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:10 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:37 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:37 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:37 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:37 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64e86572324aa7eea2f61ea517db418403a7c9976b5d5ad7ec53f58db355941`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 7.6 MB (7578895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a15579d25cd8cffa07921868d5b209add90eb5919bc8c684b4ad5e8a51fe268`  
		Last Modified: Fri, 22 May 2026 20:15:03 GMT  
		Size: 211.0 MB (210999581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9628bf90ea72b5639b183121fa70adc2a3166f0f8b61dc64da557941faa4e889`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225291cf0df1a4ddb0e6c2efff7a08245ded5936d36da4db1fd512cf245badec`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be41faac692e17e0c8ebef7ec6d284a9d9fa553251e68a3806718719e6ab8d4c`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530f5f7fab3df30aee408ad771090089db66c4155964fc72c06e06b3bf3731a3`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e5089e5a7783210222c48830ef1ffb47fa9e31710dd42a2864e5c150a76d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5.1.882` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5fda5509e5a7bd55544537246507374514e8551464ea9026eeb27b7d2afbb812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1237ad33491107f44515a662c43c3704d7f2028c202c1aa115967da20adb13`

```dockerfile
```

-	Layers:
	-	`sha256:accb5a6fedc2950811e0026389469e1d6c5acfe87f3fe0ef71fe9c7c1d5cf595`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 27.1 KB (27053 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.5.1.882-jammy`

```console
$ docker pull clickhouse@sha256:770156c537ca9124046e138a3b5845c64ea58ce8722de7a2e05fd827f4976520
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.5.1.882-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8d1bc439fd25e27e0719e3906189346621d3b30c3a1fce590f74df9e36ba1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261148941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ddf6fea0767ca6ece44e8bb8bebb226e1a2ce0650ff586d88bac748c91a5cc`
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
# Fri, 22 May 2026 20:14:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:13 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:39 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e180166c8efb533aaa3022823135bb6c8670b51d51f9fbc4d2f90a55107a9e`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 7.6 MB (7599255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1688ec152117f8ed0385e04486a1641ca44a13c333296f61f178c5bc149e57`  
		Last Modified: Fri, 22 May 2026 20:15:10 GMT  
		Size: 222.9 MB (222942955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530779b308d06014dc910f38ba3490dec2bdcca6e10781d2ab7a9ba99b865b36`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95592b500ee480fa70d1788e644c926270cc19e6dac6e7fc9d316053720b7a8f`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a80d826b2d9a7917270a5ebfc22fe4d95f9e6e822570ca073b157254798be5`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bf2de4fcdd30475c64afde6bbb742172517789fa890768e3cefa610227366`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4255ed0b8e5159dea3c2b93b37f0d4b795441100e719b8397c8f1b503ec27dce`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5.1.882-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fe7ada49ccbfdb9f6156dcb2cd793fb050fe90dad55a33a7215604d783d0f45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787a9e4add1ea2d4690fd9ea7e6460ff1af96e7832168d2a7a02e798f9662745`

```dockerfile
```

-	Layers:
	-	`sha256:693f1c4a6051d189a846b168f4c9c5d7ad3592da8de5398429f4bbd31e9c3d3a`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 26.8 KB (26841 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.5.1.882-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:524e8364d7f9ac6839ec1c28db6edb4a5e41e6300cf1e2d5d1e13d3ddee72b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247055149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c881ac185dd2f404d2cee0c6e6ddf22c6c114b86b1d352db71fee93578da68`
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
# Fri, 22 May 2026 20:14:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:10 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:37 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:37 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:37 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:37 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64e86572324aa7eea2f61ea517db418403a7c9976b5d5ad7ec53f58db355941`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 7.6 MB (7578895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a15579d25cd8cffa07921868d5b209add90eb5919bc8c684b4ad5e8a51fe268`  
		Last Modified: Fri, 22 May 2026 20:15:03 GMT  
		Size: 211.0 MB (210999581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9628bf90ea72b5639b183121fa70adc2a3166f0f8b61dc64da557941faa4e889`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225291cf0df1a4ddb0e6c2efff7a08245ded5936d36da4db1fd512cf245badec`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be41faac692e17e0c8ebef7ec6d284a9d9fa553251e68a3806718719e6ab8d4c`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530f5f7fab3df30aee408ad771090089db66c4155964fc72c06e06b3bf3731a3`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e5089e5a7783210222c48830ef1ffb47fa9e31710dd42a2864e5c150a76d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.5.1.882-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5fda5509e5a7bd55544537246507374514e8551464ea9026eeb27b7d2afbb812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1237ad33491107f44515a662c43c3704d7f2028c202c1aa115967da20adb13`

```dockerfile
```

-	Layers:
	-	`sha256:accb5a6fedc2950811e0026389469e1d6c5acfe87f3fe0ef71fe9c7c1d5cf595`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 27.1 KB (27053 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:770156c537ca9124046e138a3b5845c64ea58ce8722de7a2e05fd827f4976520
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:8d1bc439fd25e27e0719e3906189346621d3b30c3a1fce590f74df9e36ba1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261148941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ddf6fea0767ca6ece44e8bb8bebb226e1a2ce0650ff586d88bac748c91a5cc`
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
# Fri, 22 May 2026 20:14:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:13 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:39 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e180166c8efb533aaa3022823135bb6c8670b51d51f9fbc4d2f90a55107a9e`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 7.6 MB (7599255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1688ec152117f8ed0385e04486a1641ca44a13c333296f61f178c5bc149e57`  
		Last Modified: Fri, 22 May 2026 20:15:10 GMT  
		Size: 222.9 MB (222942955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530779b308d06014dc910f38ba3490dec2bdcca6e10781d2ab7a9ba99b865b36`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95592b500ee480fa70d1788e644c926270cc19e6dac6e7fc9d316053720b7a8f`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a80d826b2d9a7917270a5ebfc22fe4d95f9e6e822570ca073b157254798be5`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bf2de4fcdd30475c64afde6bbb742172517789fa890768e3cefa610227366`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4255ed0b8e5159dea3c2b93b37f0d4b795441100e719b8397c8f1b503ec27dce`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fe7ada49ccbfdb9f6156dcb2cd793fb050fe90dad55a33a7215604d783d0f45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787a9e4add1ea2d4690fd9ea7e6460ff1af96e7832168d2a7a02e798f9662745`

```dockerfile
```

-	Layers:
	-	`sha256:693f1c4a6051d189a846b168f4c9c5d7ad3592da8de5398429f4bbd31e9c3d3a`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 26.8 KB (26841 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:524e8364d7f9ac6839ec1c28db6edb4a5e41e6300cf1e2d5d1e13d3ddee72b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247055149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c881ac185dd2f404d2cee0c6e6ddf22c6c114b86b1d352db71fee93578da68`
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
# Fri, 22 May 2026 20:14:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:10 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:37 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:37 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:37 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:37 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64e86572324aa7eea2f61ea517db418403a7c9976b5d5ad7ec53f58db355941`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 7.6 MB (7578895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a15579d25cd8cffa07921868d5b209add90eb5919bc8c684b4ad5e8a51fe268`  
		Last Modified: Fri, 22 May 2026 20:15:03 GMT  
		Size: 211.0 MB (210999581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9628bf90ea72b5639b183121fa70adc2a3166f0f8b61dc64da557941faa4e889`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225291cf0df1a4ddb0e6c2efff7a08245ded5936d36da4db1fd512cf245badec`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be41faac692e17e0c8ebef7ec6d284a9d9fa553251e68a3806718719e6ab8d4c`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530f5f7fab3df30aee408ad771090089db66c4155964fc72c06e06b3bf3731a3`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e5089e5a7783210222c48830ef1ffb47fa9e31710dd42a2864e5c150a76d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5fda5509e5a7bd55544537246507374514e8551464ea9026eeb27b7d2afbb812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1237ad33491107f44515a662c43c3704d7f2028c202c1aa115967da20adb13`

```dockerfile
```

-	Layers:
	-	`sha256:accb5a6fedc2950811e0026389469e1d6c5acfe87f3fe0ef71fe9c7c1d5cf595`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 27.1 KB (27053 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:770156c537ca9124046e138a3b5845c64ea58ce8722de7a2e05fd827f4976520
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:8d1bc439fd25e27e0719e3906189346621d3b30c3a1fce590f74df9e36ba1b15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261148941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ddf6fea0767ca6ece44e8bb8bebb226e1a2ce0650ff586d88bac748c91a5cc`
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
# Fri, 22 May 2026 20:14:13 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:13 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:13 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:13 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:13 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:13 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:13 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:39 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:39 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:39 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:39 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:39 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e180166c8efb533aaa3022823135bb6c8670b51d51f9fbc4d2f90a55107a9e`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 7.6 MB (7599255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b1688ec152117f8ed0385e04486a1641ca44a13c333296f61f178c5bc149e57`  
		Last Modified: Fri, 22 May 2026 20:15:10 GMT  
		Size: 222.9 MB (222942955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530779b308d06014dc910f38ba3490dec2bdcca6e10781d2ab7a9ba99b865b36`  
		Last Modified: Fri, 22 May 2026 20:15:04 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95592b500ee480fa70d1788e644c926270cc19e6dac6e7fc9d316053720b7a8f`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a80d826b2d9a7917270a5ebfc22fe4d95f9e6e822570ca073b157254798be5`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39bf2de4fcdd30475c64afde6bbb742172517789fa890768e3cefa610227366`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4255ed0b8e5159dea3c2b93b37f0d4b795441100e719b8397c8f1b503ec27dce`  
		Last Modified: Fri, 22 May 2026 20:15:06 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:fe7ada49ccbfdb9f6156dcb2cd793fb050fe90dad55a33a7215604d783d0f45f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787a9e4add1ea2d4690fd9ea7e6460ff1af96e7832168d2a7a02e798f9662745`

```dockerfile
```

-	Layers:
	-	`sha256:693f1c4a6051d189a846b168f4c9c5d7ad3592da8de5398429f4bbd31e9c3d3a`  
		Last Modified: Fri, 22 May 2026 20:15:05 GMT  
		Size: 26.8 KB (26841 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:524e8364d7f9ac6839ec1c28db6edb4a5e41e6300cf1e2d5d1e13d3ddee72b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247055149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46c881ac185dd2f404d2cee0c6e6ddf22c6c114b86b1d352db71fee93578da68`
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
# Fri, 22 May 2026 20:14:10 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 22 May 2026 20:14:10 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 22 May 2026 20:14:10 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 22 May 2026 20:14:10 GMT
ARG REPO_CHANNEL=stable
# Fri, 22 May 2026 20:14:10 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 22 May 2026 20:14:10 GMT
ARG VERSION=26.5.1.882
# Fri, 22 May 2026 20:14:10 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:35 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 22 May 2026 20:14:37 GMT
ENV LANG=en_US.UTF-8
# Fri, 22 May 2026 20:14:37 GMT
ENV TZ=UTC
# Fri, 22 May 2026 20:14:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.5.1.882 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 22 May 2026 20:14:37 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 22 May 2026 20:14:37 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 22 May 2026 20:14:37 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 22 May 2026 20:14:37 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 22 May 2026 20:14:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b64e86572324aa7eea2f61ea517db418403a7c9976b5d5ad7ec53f58db355941`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 7.6 MB (7578895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a15579d25cd8cffa07921868d5b209add90eb5919bc8c684b4ad5e8a51fe268`  
		Last Modified: Fri, 22 May 2026 20:15:03 GMT  
		Size: 211.0 MB (210999581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9628bf90ea72b5639b183121fa70adc2a3166f0f8b61dc64da557941faa4e889`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225291cf0df1a4ddb0e6c2efff7a08245ded5936d36da4db1fd512cf245badec`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be41faac692e17e0c8ebef7ec6d284a9d9fa553251e68a3806718719e6ab8d4c`  
		Last Modified: Fri, 22 May 2026 20:14:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:530f5f7fab3df30aee408ad771090089db66c4155964fc72c06e06b3bf3731a3`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe8e5089e5a7783210222c48830ef1ffb47fa9e31710dd42a2864e5c150a76d`  
		Last Modified: Fri, 22 May 2026 20:15:00 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:5fda5509e5a7bd55544537246507374514e8551464ea9026eeb27b7d2afbb812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb1237ad33491107f44515a662c43c3704d7f2028c202c1aa115967da20adb13`

```dockerfile
```

-	Layers:
	-	`sha256:accb5a6fedc2950811e0026389469e1d6c5acfe87f3fe0ef71fe9c7c1d5cf595`  
		Last Modified: Fri, 22 May 2026 20:14:58 GMT  
		Size: 27.1 KB (27053 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:0816d912717473854976f4c68cc869d119078cafd5639b66902e4afde57d8b8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:75b9d1ade272302ddfbdce179cf1ba2ae2ab9f42dfdf372e50b0130c0c25bff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264806066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159c355b977fff2e7e0899d85f4e35a94c1d52749b8dc8a5143dbce7d383c6d8`
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
# Fri, 15 May 2026 21:11:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:17 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:41 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:41 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7011ff31f15e81789181937898b770e8b20b75cf4ac3ef78b97441d3895c70`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 7.6 MB (7599287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36c3946d863cfb6aeabf8668540972aa93dd1d777428e719b09b1a2d1e39c31`  
		Last Modified: Fri, 15 May 2026 21:12:09 GMT  
		Size: 226.6 MB (226600051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d4144f9ed5a53a15944747b9467e80ba1dde55642fc88064fb7226612a373c`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da53b00944850a6ab3faf7cecc0e73e11c4bd0900b574b9eff650006b2ef9a08`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6532a2ef48b0172a1c83e184e13040f8e205d68ff052c2991ac28443438694aa`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b8fb6bfa5222d530fe781d4a428a54675a8eb4c1c49c099949efefd100b6ee`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03d873d57029deeaf43e26876afdc29cd14dad2f670531da07b6553cbf3a447`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4c3e22f4dd15fa758f2f94b8bedee58eced1dbee16e9f3ea5d12135a60bdc99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bf87ad8c04cf103c51c25a99ee5f06ae243ed357d37eff9e29671c3c73415b`

```dockerfile
```

-	Layers:
	-	`sha256:7291f19213dbdbd100fa399ee1f565dd83938a0e80d26182282b328a6ef08f82`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b888f4a4071d6e577c99d19d44acb5afe679862bbb38065a2efd4f19e87d5aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2b13e25b8289f6522e8a0b26d7f6f0b525e63565b9b3015b7bb666e0600e2e`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cc0127d140f4f8c2a885ded7884fa962d5608a5d20bd3a3b794c5c508553cd`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 7.6 MB (7578951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666017bd70a350c629f1f4092c945a7b1784d2461fb2dea8b1f18df61cfaf5c`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 210.2 MB (210218608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f297032f7c5cb81104c89b306611dd912900edc6da997eac7fc6d311b6d49`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e718e1bd582339ceed14e1c2affbb3fd7494d973c32fbe5733b19dcc07769d20`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35576b3658950c1a35f38c292b3a539ce0ca08972b9f88ff22530d9d09c3dac`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d85c621d654cd9ce41a7e1185c8ea3e3f3c4e8fee6ed505e7a8993e08e17dc`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cb445f6e3b234bab5117b35b93673292561e373afe668d0cd4c186a542fda`  
		Last Modified: Fri, 15 May 2026 21:12:20 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1113b00cddfa85f071107508d76a42d623e1f0ed7dd80cf3bb4d321dae039e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb3f778675a38b71cc10cd5549bf85eb6a50f3e603073c688eb53818f358bd1`

```dockerfile
```

-	Layers:
	-	`sha256:ba403868bf4d6c70f1b487bb61927529bba0717192a39e16d9b32151b4b9bf83`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:0816d912717473854976f4c68cc869d119078cafd5639b66902e4afde57d8b8c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:75b9d1ade272302ddfbdce179cf1ba2ae2ab9f42dfdf372e50b0130c0c25bff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264806066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:159c355b977fff2e7e0899d85f4e35a94c1d52749b8dc8a5143dbce7d383c6d8`
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
# Fri, 15 May 2026 21:11:17 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:17 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:17 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:17 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:17 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:17 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:17 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:40 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:41 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:41 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:41 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:41 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:41 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:41 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:40d16f30db405106ef8074779bdf41f012465c2a785bbeaa2eab9f2081099b47`  
		Last Modified: Sat, 09 May 2026 05:24:51 GMT  
		Size: 29.7 MB (29736684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7011ff31f15e81789181937898b770e8b20b75cf4ac3ef78b97441d3895c70`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 7.6 MB (7599287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36c3946d863cfb6aeabf8668540972aa93dd1d777428e719b09b1a2d1e39c31`  
		Last Modified: Fri, 15 May 2026 21:12:09 GMT  
		Size: 226.6 MB (226600051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d4144f9ed5a53a15944747b9467e80ba1dde55642fc88064fb7226612a373c`  
		Last Modified: Fri, 15 May 2026 21:12:03 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da53b00944850a6ab3faf7cecc0e73e11c4bd0900b574b9eff650006b2ef9a08`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6532a2ef48b0172a1c83e184e13040f8e205d68ff052c2991ac28443438694aa`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b8fb6bfa5222d530fe781d4a428a54675a8eb4c1c49c099949efefd100b6ee`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03d873d57029deeaf43e26876afdc29cd14dad2f670531da07b6553cbf3a447`  
		Last Modified: Fri, 15 May 2026 21:12:05 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c4c3e22f4dd15fa758f2f94b8bedee58eced1dbee16e9f3ea5d12135a60bdc99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53bf87ad8c04cf103c51c25a99ee5f06ae243ed357d37eff9e29671c3c73415b`

```dockerfile
```

-	Layers:
	-	`sha256:7291f19213dbdbd100fa399ee1f565dd83938a0e80d26182282b328a6ef08f82`  
		Last Modified: Fri, 15 May 2026 21:12:04 GMT  
		Size: 26.8 KB (26847 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:b888f4a4071d6e577c99d19d44acb5afe679862bbb38065a2efd4f19e87d5aca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246274230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c2b13e25b8289f6522e8a0b26d7f6f0b525e63565b9b3015b7bb666e0600e2e`
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
# Fri, 15 May 2026 21:11:25 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Fri, 15 May 2026 21:11:25 GMT
ARG apt_archive=http://archive.ubuntu.com
# Fri, 15 May 2026 21:11:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Fri, 15 May 2026 21:11:25 GMT
ARG REPO_CHANNEL=stable
# Fri, 15 May 2026 21:11:25 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Fri, 15 May 2026 21:11:25 GMT
ARG VERSION=26.3.10.62
# Fri, 15 May 2026 21:11:25 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && ( set +e;         for KEYSERVER in             hkp://keys.openpgp.org:80             hkp://pgp.mit.edu:80             hkp://keyserver.ubuntu.com:80; do             GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring                 --keyring /usr/share/keyrings/clickhouse-keyring.gpg                 --keyserver "$KEYSERVER"                 --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754 && break;         done || exit 1     )     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:54 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Fri, 15 May 2026 21:11:56 GMT
ENV LANG=en_US.UTF-8
# Fri, 15 May 2026 21:11:56 GMT
ENV TZ=UTC
# Fri, 15 May 2026 21:11:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.3.10.62 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Fri, 15 May 2026 21:11:56 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Fri, 15 May 2026 21:11:56 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Fri, 15 May 2026 21:11:56 GMT
VOLUME [/var/lib/clickhouse]
# Fri, 15 May 2026 21:11:56 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Fri, 15 May 2026 21:11:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:99267111abcc4caf5e9b6f06fd8b9ca7ae7bff04ce06b24ca352c6007daaa73e`  
		Last Modified: Sat, 09 May 2026 05:24:57 GMT  
		Size: 27.6 MB (27606623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cc0127d140f4f8c2a885ded7884fa962d5608a5d20bd3a3b794c5c508553cd`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 7.6 MB (7578951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2666017bd70a350c629f1f4092c945a7b1784d2461fb2dea8b1f18df61cfaf5c`  
		Last Modified: Fri, 15 May 2026 21:12:23 GMT  
		Size: 210.2 MB (210218608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f297032f7c5cb81104c89b306611dd912900edc6da997eac7fc6d311b6d49`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e718e1bd582339ceed14e1c2affbb3fd7494d973c32fbe5733b19dcc07769d20`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 865.7 KB (865747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35576b3658950c1a35f38c292b3a539ce0ca08972b9f88ff22530d9d09c3dac`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d85c621d654cd9ce41a7e1185c8ea3e3f3c4e8fee6ed505e7a8993e08e17dc`  
		Last Modified: Fri, 15 May 2026 21:12:19 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cb445f6e3b234bab5117b35b93673292561e373afe668d0cd4c186a542fda`  
		Last Modified: Fri, 15 May 2026 21:12:20 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d1113b00cddfa85f071107508d76a42d623e1f0ed7dd80cf3bb4d321dae039e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 KB (27059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb3f778675a38b71cc10cd5549bf85eb6a50f3e603073c688eb53818f358bd1`

```dockerfile
```

-	Layers:
	-	`sha256:ba403868bf4d6c70f1b487bb61927529bba0717192a39e16d9b32151b4b9bf83`  
		Last Modified: Fri, 15 May 2026 21:12:18 GMT  
		Size: 27.1 KB (27059 bytes)  
		MIME: application/vnd.in-toto+json
