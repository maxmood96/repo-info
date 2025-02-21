<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:24.11`](#clickhouse2411)
-	[`clickhouse:24.11-jammy`](#clickhouse2411-jammy)
-	[`clickhouse:24.11.5`](#clickhouse24115)
-	[`clickhouse:24.11.5-jammy`](#clickhouse24115-jammy)
-	[`clickhouse:24.11.5.49`](#clickhouse2411549)
-	[`clickhouse:24.11.5.49-jammy`](#clickhouse2411549-jammy)
-	[`clickhouse:24.12`](#clickhouse2412)
-	[`clickhouse:24.12-jammy`](#clickhouse2412-jammy)
-	[`clickhouse:24.12.5`](#clickhouse24125)
-	[`clickhouse:24.12.5-jammy`](#clickhouse24125-jammy)
-	[`clickhouse:24.12.5.81`](#clickhouse2412581)
-	[`clickhouse:24.12.5.81-jammy`](#clickhouse2412581-jammy)
-	[`clickhouse:24.3`](#clickhouse243)
-	[`clickhouse:24.3-focal`](#clickhouse243-focal)
-	[`clickhouse:24.3.18`](#clickhouse24318)
-	[`clickhouse:24.3.18-focal`](#clickhouse24318-focal)
-	[`clickhouse:24.3.18.7`](#clickhouse243187)
-	[`clickhouse:24.3.18.7-focal`](#clickhouse243187-focal)
-	[`clickhouse:24.8`](#clickhouse248)
-	[`clickhouse:24.8-focal`](#clickhouse248-focal)
-	[`clickhouse:24.8.14`](#clickhouse24814)
-	[`clickhouse:24.8.14-focal`](#clickhouse24814-focal)
-	[`clickhouse:24.8.14.39`](#clickhouse2481439)
-	[`clickhouse:24.8.14.39-focal`](#clickhouse2481439-focal)
-	[`clickhouse:25.1`](#clickhouse251)
-	[`clickhouse:25.1-jammy`](#clickhouse251-jammy)
-	[`clickhouse:25.1.5`](#clickhouse2515)
-	[`clickhouse:25.1.5-jammy`](#clickhouse2515-jammy)
-	[`clickhouse:25.1.5.31`](#clickhouse251531)
-	[`clickhouse:25.1.5.31-jammy`](#clickhouse251531-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-focal`](#clickhouselts-focal)

## `clickhouse:24.11`

```console
$ docker pull clickhouse@sha256:3dccb899860a6cd822a4c2dc1f457977ef0b5f75efeba6047f3ba23c07a1bcab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:014c816e9e0488282fbc49842afbe1f08394b2be0cb7e857a928d6375b98302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182686948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3168a9c6008e067f0ad6a7aac4f08a2d0496880832e6ea4e8a8c02385cb76552`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=24.11.5.49
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8852b147a6a6ef05f7fbb688d43041f989faddaf213706299702061b9c1a833a`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 7.1 MB (7146943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62b93ef7ef69d6a1e836f48bb520d4a32a8f1034e59a5ee6c67b30a4d8b9b0c`  
		Last Modified: Fri, 21 Feb 2025 01:49:35 GMT  
		Size: 145.1 MB (145133815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c23cecae3529689b2c25fab8859b814b9deeba81875aff630c909c8c772e87`  
		Last Modified: Fri, 21 Feb 2025 00:28:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e92360d8a55339c582ecba579430f51257faa9d8730841ac6304299b324855d`  
		Last Modified: Fri, 21 Feb 2025 00:28:14 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e139406f3f76bc007e615d3431c9497e89bd06371e586272b2c95090cff32120`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867d70103d6a9286f35639eb41c2219b8530ef84b952ddac2818f7c52d84925f`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a03910549fb062456c9f198daf13ceb06e99a13060decf015e10eee2c6bd3a`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d3466db8f7409947584badd4941e4e62655bf82feaffb8a4a132ca2e9ad88508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8241e7e4c9a3163f0d45134f6c20ef2cbb142dbb126f72c765811f5f94490f`

```dockerfile
```

-	Layers:
	-	`sha256:8884cee8b3587e5fd73b56cc53c2da0537b22158c6b3e443ef80872824cb23ec`  
		Last Modified: Fri, 21 Feb 2025 01:49:19 GMT  
		Size: 25.3 KB (25281 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b3f252ff69e35e149340cc31925403e3cdb5083786ff1ab12572e3bfccdad45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172830800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bbafcfaf3b38d7c0b6f72225a0f73c47dfff3985d3b1b0aa68eaac7d4c96fc`
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
ARG VERSION=24.11.5.49
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38b1d7c103d7b5a292806606b345258025dfaf42f24afe7fab258b0fbbd83e7`  
		Last Modified: Fri, 21 Feb 2025 01:49:34 GMT  
		Size: 137.5 MB (137481252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30664c01679a5f303c69e4d09b7030eb43dcc19cdaa69430ca9fd868ed73fe9`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ef3c6e210d8b67059892f694add04d787d6cfc755faff4363ec84f4a9764a2`  
		Last Modified: Fri, 21 Feb 2025 00:29:47 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2402f861630dae9bd2e0306473fcb81e5dc141177a88962209da7cd1756af5d0`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4722ef588abac0138c3c18910e7ba10133a1513e2eea4823ae62d5d965b97c84`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c91d1d98721e7b9b3f2a96e03db7fcacdc8be02e66d836ae571a15ac384a457`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9415f0f2ac3ed0c5ee5a9c0a268405675bba1fbf41e4dfdbfe4c4ca877f549de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5405bf9684cb592321437c06b3e69b76c4b41df2e96c87ae3934cd9162eff8`

```dockerfile
```

-	Layers:
	-	`sha256:8166745ce9a7c30b043d88de3aacfd861044ec563854f95b4011e7a9c8ad0d14`  
		Last Modified: Fri, 21 Feb 2025 01:49:20 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.11-jammy`

```console
$ docker pull clickhouse@sha256:3dccb899860a6cd822a4c2dc1f457977ef0b5f75efeba6047f3ba23c07a1bcab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:014c816e9e0488282fbc49842afbe1f08394b2be0cb7e857a928d6375b98302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182686948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3168a9c6008e067f0ad6a7aac4f08a2d0496880832e6ea4e8a8c02385cb76552`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=24.11.5.49
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8852b147a6a6ef05f7fbb688d43041f989faddaf213706299702061b9c1a833a`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 7.1 MB (7146943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62b93ef7ef69d6a1e836f48bb520d4a32a8f1034e59a5ee6c67b30a4d8b9b0c`  
		Last Modified: Fri, 21 Feb 2025 01:49:35 GMT  
		Size: 145.1 MB (145133815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c23cecae3529689b2c25fab8859b814b9deeba81875aff630c909c8c772e87`  
		Last Modified: Fri, 21 Feb 2025 00:28:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e92360d8a55339c582ecba579430f51257faa9d8730841ac6304299b324855d`  
		Last Modified: Fri, 21 Feb 2025 00:28:14 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e139406f3f76bc007e615d3431c9497e89bd06371e586272b2c95090cff32120`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867d70103d6a9286f35639eb41c2219b8530ef84b952ddac2818f7c52d84925f`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a03910549fb062456c9f198daf13ceb06e99a13060decf015e10eee2c6bd3a`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d3466db8f7409947584badd4941e4e62655bf82feaffb8a4a132ca2e9ad88508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8241e7e4c9a3163f0d45134f6c20ef2cbb142dbb126f72c765811f5f94490f`

```dockerfile
```

-	Layers:
	-	`sha256:8884cee8b3587e5fd73b56cc53c2da0537b22158c6b3e443ef80872824cb23ec`  
		Last Modified: Fri, 21 Feb 2025 01:49:19 GMT  
		Size: 25.3 KB (25281 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b3f252ff69e35e149340cc31925403e3cdb5083786ff1ab12572e3bfccdad45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172830800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bbafcfaf3b38d7c0b6f72225a0f73c47dfff3985d3b1b0aa68eaac7d4c96fc`
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
ARG VERSION=24.11.5.49
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38b1d7c103d7b5a292806606b345258025dfaf42f24afe7fab258b0fbbd83e7`  
		Last Modified: Fri, 21 Feb 2025 01:49:34 GMT  
		Size: 137.5 MB (137481252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30664c01679a5f303c69e4d09b7030eb43dcc19cdaa69430ca9fd868ed73fe9`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ef3c6e210d8b67059892f694add04d787d6cfc755faff4363ec84f4a9764a2`  
		Last Modified: Fri, 21 Feb 2025 00:29:47 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2402f861630dae9bd2e0306473fcb81e5dc141177a88962209da7cd1756af5d0`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4722ef588abac0138c3c18910e7ba10133a1513e2eea4823ae62d5d965b97c84`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c91d1d98721e7b9b3f2a96e03db7fcacdc8be02e66d836ae571a15ac384a457`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9415f0f2ac3ed0c5ee5a9c0a268405675bba1fbf41e4dfdbfe4c4ca877f549de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5405bf9684cb592321437c06b3e69b76c4b41df2e96c87ae3934cd9162eff8`

```dockerfile
```

-	Layers:
	-	`sha256:8166745ce9a7c30b043d88de3aacfd861044ec563854f95b4011e7a9c8ad0d14`  
		Last Modified: Fri, 21 Feb 2025 01:49:20 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.11.5`

```console
$ docker pull clickhouse@sha256:3dccb899860a6cd822a4c2dc1f457977ef0b5f75efeba6047f3ba23c07a1bcab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.11.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:014c816e9e0488282fbc49842afbe1f08394b2be0cb7e857a928d6375b98302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182686948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3168a9c6008e067f0ad6a7aac4f08a2d0496880832e6ea4e8a8c02385cb76552`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=24.11.5.49
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8852b147a6a6ef05f7fbb688d43041f989faddaf213706299702061b9c1a833a`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 7.1 MB (7146943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62b93ef7ef69d6a1e836f48bb520d4a32a8f1034e59a5ee6c67b30a4d8b9b0c`  
		Last Modified: Fri, 21 Feb 2025 01:49:35 GMT  
		Size: 145.1 MB (145133815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c23cecae3529689b2c25fab8859b814b9deeba81875aff630c909c8c772e87`  
		Last Modified: Fri, 21 Feb 2025 00:28:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e92360d8a55339c582ecba579430f51257faa9d8730841ac6304299b324855d`  
		Last Modified: Fri, 21 Feb 2025 00:28:14 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e139406f3f76bc007e615d3431c9497e89bd06371e586272b2c95090cff32120`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867d70103d6a9286f35639eb41c2219b8530ef84b952ddac2818f7c52d84925f`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a03910549fb062456c9f198daf13ceb06e99a13060decf015e10eee2c6bd3a`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d3466db8f7409947584badd4941e4e62655bf82feaffb8a4a132ca2e9ad88508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8241e7e4c9a3163f0d45134f6c20ef2cbb142dbb126f72c765811f5f94490f`

```dockerfile
```

-	Layers:
	-	`sha256:8884cee8b3587e5fd73b56cc53c2da0537b22158c6b3e443ef80872824cb23ec`  
		Last Modified: Fri, 21 Feb 2025 01:49:19 GMT  
		Size: 25.3 KB (25281 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.11.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b3f252ff69e35e149340cc31925403e3cdb5083786ff1ab12572e3bfccdad45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172830800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bbafcfaf3b38d7c0b6f72225a0f73c47dfff3985d3b1b0aa68eaac7d4c96fc`
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
ARG VERSION=24.11.5.49
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38b1d7c103d7b5a292806606b345258025dfaf42f24afe7fab258b0fbbd83e7`  
		Last Modified: Fri, 21 Feb 2025 01:49:34 GMT  
		Size: 137.5 MB (137481252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30664c01679a5f303c69e4d09b7030eb43dcc19cdaa69430ca9fd868ed73fe9`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ef3c6e210d8b67059892f694add04d787d6cfc755faff4363ec84f4a9764a2`  
		Last Modified: Fri, 21 Feb 2025 00:29:47 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2402f861630dae9bd2e0306473fcb81e5dc141177a88962209da7cd1756af5d0`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4722ef588abac0138c3c18910e7ba10133a1513e2eea4823ae62d5d965b97c84`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c91d1d98721e7b9b3f2a96e03db7fcacdc8be02e66d836ae571a15ac384a457`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9415f0f2ac3ed0c5ee5a9c0a268405675bba1fbf41e4dfdbfe4c4ca877f549de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5405bf9684cb592321437c06b3e69b76c4b41df2e96c87ae3934cd9162eff8`

```dockerfile
```

-	Layers:
	-	`sha256:8166745ce9a7c30b043d88de3aacfd861044ec563854f95b4011e7a9c8ad0d14`  
		Last Modified: Fri, 21 Feb 2025 01:49:20 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.11.5-jammy`

```console
$ docker pull clickhouse@sha256:3dccb899860a6cd822a4c2dc1f457977ef0b5f75efeba6047f3ba23c07a1bcab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.11.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:014c816e9e0488282fbc49842afbe1f08394b2be0cb7e857a928d6375b98302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182686948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3168a9c6008e067f0ad6a7aac4f08a2d0496880832e6ea4e8a8c02385cb76552`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=24.11.5.49
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8852b147a6a6ef05f7fbb688d43041f989faddaf213706299702061b9c1a833a`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 7.1 MB (7146943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62b93ef7ef69d6a1e836f48bb520d4a32a8f1034e59a5ee6c67b30a4d8b9b0c`  
		Last Modified: Fri, 21 Feb 2025 01:49:35 GMT  
		Size: 145.1 MB (145133815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c23cecae3529689b2c25fab8859b814b9deeba81875aff630c909c8c772e87`  
		Last Modified: Fri, 21 Feb 2025 00:28:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e92360d8a55339c582ecba579430f51257faa9d8730841ac6304299b324855d`  
		Last Modified: Fri, 21 Feb 2025 00:28:14 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e139406f3f76bc007e615d3431c9497e89bd06371e586272b2c95090cff32120`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867d70103d6a9286f35639eb41c2219b8530ef84b952ddac2818f7c52d84925f`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a03910549fb062456c9f198daf13ceb06e99a13060decf015e10eee2c6bd3a`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d3466db8f7409947584badd4941e4e62655bf82feaffb8a4a132ca2e9ad88508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8241e7e4c9a3163f0d45134f6c20ef2cbb142dbb126f72c765811f5f94490f`

```dockerfile
```

-	Layers:
	-	`sha256:8884cee8b3587e5fd73b56cc53c2da0537b22158c6b3e443ef80872824cb23ec`  
		Last Modified: Fri, 21 Feb 2025 01:49:19 GMT  
		Size: 25.3 KB (25281 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.11.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b3f252ff69e35e149340cc31925403e3cdb5083786ff1ab12572e3bfccdad45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172830800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bbafcfaf3b38d7c0b6f72225a0f73c47dfff3985d3b1b0aa68eaac7d4c96fc`
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
ARG VERSION=24.11.5.49
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38b1d7c103d7b5a292806606b345258025dfaf42f24afe7fab258b0fbbd83e7`  
		Last Modified: Fri, 21 Feb 2025 01:49:34 GMT  
		Size: 137.5 MB (137481252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30664c01679a5f303c69e4d09b7030eb43dcc19cdaa69430ca9fd868ed73fe9`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ef3c6e210d8b67059892f694add04d787d6cfc755faff4363ec84f4a9764a2`  
		Last Modified: Fri, 21 Feb 2025 00:29:47 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2402f861630dae9bd2e0306473fcb81e5dc141177a88962209da7cd1756af5d0`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4722ef588abac0138c3c18910e7ba10133a1513e2eea4823ae62d5d965b97c84`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c91d1d98721e7b9b3f2a96e03db7fcacdc8be02e66d836ae571a15ac384a457`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9415f0f2ac3ed0c5ee5a9c0a268405675bba1fbf41e4dfdbfe4c4ca877f549de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5405bf9684cb592321437c06b3e69b76c4b41df2e96c87ae3934cd9162eff8`

```dockerfile
```

-	Layers:
	-	`sha256:8166745ce9a7c30b043d88de3aacfd861044ec563854f95b4011e7a9c8ad0d14`  
		Last Modified: Fri, 21 Feb 2025 01:49:20 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.11.5.49`

```console
$ docker pull clickhouse@sha256:3dccb899860a6cd822a4c2dc1f457977ef0b5f75efeba6047f3ba23c07a1bcab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.11.5.49` - linux; amd64

```console
$ docker pull clickhouse@sha256:014c816e9e0488282fbc49842afbe1f08394b2be0cb7e857a928d6375b98302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182686948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3168a9c6008e067f0ad6a7aac4f08a2d0496880832e6ea4e8a8c02385cb76552`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=24.11.5.49
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8852b147a6a6ef05f7fbb688d43041f989faddaf213706299702061b9c1a833a`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 7.1 MB (7146943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62b93ef7ef69d6a1e836f48bb520d4a32a8f1034e59a5ee6c67b30a4d8b9b0c`  
		Last Modified: Fri, 21 Feb 2025 01:49:35 GMT  
		Size: 145.1 MB (145133815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c23cecae3529689b2c25fab8859b814b9deeba81875aff630c909c8c772e87`  
		Last Modified: Fri, 21 Feb 2025 00:28:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e92360d8a55339c582ecba579430f51257faa9d8730841ac6304299b324855d`  
		Last Modified: Fri, 21 Feb 2025 00:28:14 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e139406f3f76bc007e615d3431c9497e89bd06371e586272b2c95090cff32120`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867d70103d6a9286f35639eb41c2219b8530ef84b952ddac2818f7c52d84925f`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a03910549fb062456c9f198daf13ceb06e99a13060decf015e10eee2c6bd3a`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11.5.49` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d3466db8f7409947584badd4941e4e62655bf82feaffb8a4a132ca2e9ad88508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8241e7e4c9a3163f0d45134f6c20ef2cbb142dbb126f72c765811f5f94490f`

```dockerfile
```

-	Layers:
	-	`sha256:8884cee8b3587e5fd73b56cc53c2da0537b22158c6b3e443ef80872824cb23ec`  
		Last Modified: Fri, 21 Feb 2025 01:49:19 GMT  
		Size: 25.3 KB (25281 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.11.5.49` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b3f252ff69e35e149340cc31925403e3cdb5083786ff1ab12572e3bfccdad45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172830800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bbafcfaf3b38d7c0b6f72225a0f73c47dfff3985d3b1b0aa68eaac7d4c96fc`
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
ARG VERSION=24.11.5.49
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38b1d7c103d7b5a292806606b345258025dfaf42f24afe7fab258b0fbbd83e7`  
		Last Modified: Fri, 21 Feb 2025 01:49:34 GMT  
		Size: 137.5 MB (137481252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30664c01679a5f303c69e4d09b7030eb43dcc19cdaa69430ca9fd868ed73fe9`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ef3c6e210d8b67059892f694add04d787d6cfc755faff4363ec84f4a9764a2`  
		Last Modified: Fri, 21 Feb 2025 00:29:47 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2402f861630dae9bd2e0306473fcb81e5dc141177a88962209da7cd1756af5d0`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4722ef588abac0138c3c18910e7ba10133a1513e2eea4823ae62d5d965b97c84`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c91d1d98721e7b9b3f2a96e03db7fcacdc8be02e66d836ae571a15ac384a457`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11.5.49` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9415f0f2ac3ed0c5ee5a9c0a268405675bba1fbf41e4dfdbfe4c4ca877f549de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5405bf9684cb592321437c06b3e69b76c4b41df2e96c87ae3934cd9162eff8`

```dockerfile
```

-	Layers:
	-	`sha256:8166745ce9a7c30b043d88de3aacfd861044ec563854f95b4011e7a9c8ad0d14`  
		Last Modified: Fri, 21 Feb 2025 01:49:20 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.11.5.49-jammy`

```console
$ docker pull clickhouse@sha256:3dccb899860a6cd822a4c2dc1f457977ef0b5f75efeba6047f3ba23c07a1bcab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.11.5.49-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:014c816e9e0488282fbc49842afbe1f08394b2be0cb7e857a928d6375b98302d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182686948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3168a9c6008e067f0ad6a7aac4f08a2d0496880832e6ea4e8a8c02385cb76552`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=24.11.5.49
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8852b147a6a6ef05f7fbb688d43041f989faddaf213706299702061b9c1a833a`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 7.1 MB (7146943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62b93ef7ef69d6a1e836f48bb520d4a32a8f1034e59a5ee6c67b30a4d8b9b0c`  
		Last Modified: Fri, 21 Feb 2025 01:49:35 GMT  
		Size: 145.1 MB (145133815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6c23cecae3529689b2c25fab8859b814b9deeba81875aff630c909c8c772e87`  
		Last Modified: Fri, 21 Feb 2025 00:28:08 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e92360d8a55339c582ecba579430f51257faa9d8730841ac6304299b324855d`  
		Last Modified: Fri, 21 Feb 2025 00:28:14 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e139406f3f76bc007e615d3431c9497e89bd06371e586272b2c95090cff32120`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867d70103d6a9286f35639eb41c2219b8530ef84b952ddac2818f7c52d84925f`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a03910549fb062456c9f198daf13ceb06e99a13060decf015e10eee2c6bd3a`  
		Last Modified: Fri, 21 Feb 2025 00:28:09 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11.5.49-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d3466db8f7409947584badd4941e4e62655bf82feaffb8a4a132ca2e9ad88508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8241e7e4c9a3163f0d45134f6c20ef2cbb142dbb126f72c765811f5f94490f`

```dockerfile
```

-	Layers:
	-	`sha256:8884cee8b3587e5fd73b56cc53c2da0537b22158c6b3e443ef80872824cb23ec`  
		Last Modified: Fri, 21 Feb 2025 01:49:19 GMT  
		Size: 25.3 KB (25281 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.11.5.49-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:5b3f252ff69e35e149340cc31925403e3cdb5083786ff1ab12572e3bfccdad45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.8 MB (172830800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89bbafcfaf3b38d7c0b6f72225a0f73c47dfff3985d3b1b0aa68eaac7d4c96fc`
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
ARG VERSION=24.11.5.49
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.11.5.49 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38b1d7c103d7b5a292806606b345258025dfaf42f24afe7fab258b0fbbd83e7`  
		Last Modified: Fri, 21 Feb 2025 01:49:34 GMT  
		Size: 137.5 MB (137481252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30664c01679a5f303c69e4d09b7030eb43dcc19cdaa69430ca9fd868ed73fe9`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ef3c6e210d8b67059892f694add04d787d6cfc755faff4363ec84f4a9764a2`  
		Last Modified: Fri, 21 Feb 2025 00:29:47 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2402f861630dae9bd2e0306473fcb81e5dc141177a88962209da7cd1756af5d0`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4722ef588abac0138c3c18910e7ba10133a1513e2eea4823ae62d5d965b97c84`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c91d1d98721e7b9b3f2a96e03db7fcacdc8be02e66d836ae571a15ac384a457`  
		Last Modified: Fri, 21 Feb 2025 00:29:42 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.11.5.49-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9415f0f2ac3ed0c5ee5a9c0a268405675bba1fbf41e4dfdbfe4c4ca877f549de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5405bf9684cb592321437c06b3e69b76c4b41df2e96c87ae3934cd9162eff8`

```dockerfile
```

-	Layers:
	-	`sha256:8166745ce9a7c30b043d88de3aacfd861044ec563854f95b4011e7a9c8ad0d14`  
		Last Modified: Fri, 21 Feb 2025 01:49:20 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.12`

```console
$ docker pull clickhouse@sha256:4d92acbc95bf9dae47aed3a23816b930b8b5e91f598c572a44dc7993ada409b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.12` - linux; amd64

```console
$ docker pull clickhouse@sha256:d3adfa7aed1b7335ae82605b943ccc904009effd00517c829d9892c0d8f30da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185897023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9436c271c13b969b10a73c71a021687f9a710570865b6611416d8d12da16287`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=24.12.5.81
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed85509f193d049d0d8771d0e908bd6f68c48bc84da56516de41f6d4eacabb46`  
		Last Modified: Fri, 21 Feb 2025 00:28:37 GMT  
		Size: 7.1 MB (7146946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2634cedca4ec4d6ec49e3dbec5936c936ca00826c1d74f083f67e3885fc3a244`  
		Last Modified: Fri, 21 Feb 2025 01:49:45 GMT  
		Size: 148.3 MB (148343885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493cb809608d009c4d9d795438a9a9c602df95021026e91ece800f6069fb7aa1`  
		Last Modified: Fri, 21 Feb 2025 00:28:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fddacb910bf5f9e99271264a54d143298d3f1b1d9f1cab68930b140a790c558`  
		Last Modified: Fri, 21 Feb 2025 00:28:33 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff15984359130f2898de1cf61ee9023691697cbacdceb5a6043c454f80c3079`  
		Last Modified: Fri, 21 Feb 2025 00:28:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bcf41e381db3a1b11c02096d88f39da331f6d474b30bf8917e1ff24e73012a`  
		Last Modified: Fri, 21 Feb 2025 00:28:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd2c7305b82a0e2578f0228d091a5eaa696107bef46cae5710eea53b71660f5`  
		Last Modified: Fri, 21 Feb 2025 00:28:17 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a06f219eecc842356ff61b4a33ce095bdb1fd00d95bc1c0bff428762d9b27cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b776e5de84a69c5b9b2ac04b602d2eb2d45975e39709fc1333f42153fcf922b4`

```dockerfile
```

-	Layers:
	-	`sha256:9ff01b4e93f3228e643a15b9fda3754f658ebfa6e9db482ef1c337fe1caaa019`  
		Last Modified: Fri, 21 Feb 2025 01:49:32 GMT  
		Size: 25.3 KB (25282 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.12` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f247a4cc744d1e3c7ea938b9c5dccd013eb329efd806c1e4043c01a259bc8e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176099156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173b3db67b1661109bb72c5ce669783a00113d61290399aa851c80aeea159ca7`
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
ARG VERSION=24.12.5.81
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fca808cd2b3e3c039a2be80438a8d5bf8517e926c822530b261199385f5f87`  
		Last Modified: Fri, 21 Feb 2025 01:49:50 GMT  
		Size: 140.7 MB (140749605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f175e0bf612a3de3fe3e62a432d0ca03d006be2e98ef7955bfb414c73d880e`  
		Last Modified: Fri, 21 Feb 2025 00:29:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e175d47455d0b91d52335bd6a97ad5840f9228567ddfea2add16d013ef773f62`  
		Last Modified: Fri, 21 Feb 2025 00:29:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b471638593d43d23a8462d518021881932725d6f5026ec821fe29aafb9cfb9d`  
		Last Modified: Fri, 21 Feb 2025 00:29:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298ad3b52107baec77c12974233b4e0595804d5e37029dc5bee25a1b15163174`  
		Last Modified: Fri, 21 Feb 2025 00:29:05 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9f5c8c2d7263b88d7fcf9f9e93636186e9988eb88b54ee101e5abbeb692429`  
		Last Modified: Fri, 21 Feb 2025 00:29:05 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:875ca0f48cedb659437b124cf1d6a754ca81c91e8b72ca8247b5122805eec7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9da86a81c06609f831c0fc789e3255df38f7b67d6fe47e91358b355efdfd7e`

```dockerfile
```

-	Layers:
	-	`sha256:ee727a18d2989639daea3005b755c208849f3d2caf468d0bf85e979222730009`  
		Last Modified: Fri, 21 Feb 2025 01:49:33 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.12-jammy`

```console
$ docker pull clickhouse@sha256:4d92acbc95bf9dae47aed3a23816b930b8b5e91f598c572a44dc7993ada409b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.12-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:d3adfa7aed1b7335ae82605b943ccc904009effd00517c829d9892c0d8f30da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185897023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9436c271c13b969b10a73c71a021687f9a710570865b6611416d8d12da16287`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=24.12.5.81
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed85509f193d049d0d8771d0e908bd6f68c48bc84da56516de41f6d4eacabb46`  
		Last Modified: Fri, 21 Feb 2025 00:28:37 GMT  
		Size: 7.1 MB (7146946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2634cedca4ec4d6ec49e3dbec5936c936ca00826c1d74f083f67e3885fc3a244`  
		Last Modified: Fri, 21 Feb 2025 01:49:45 GMT  
		Size: 148.3 MB (148343885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493cb809608d009c4d9d795438a9a9c602df95021026e91ece800f6069fb7aa1`  
		Last Modified: Fri, 21 Feb 2025 00:28:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fddacb910bf5f9e99271264a54d143298d3f1b1d9f1cab68930b140a790c558`  
		Last Modified: Fri, 21 Feb 2025 00:28:33 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff15984359130f2898de1cf61ee9023691697cbacdceb5a6043c454f80c3079`  
		Last Modified: Fri, 21 Feb 2025 00:28:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bcf41e381db3a1b11c02096d88f39da331f6d474b30bf8917e1ff24e73012a`  
		Last Modified: Fri, 21 Feb 2025 00:28:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd2c7305b82a0e2578f0228d091a5eaa696107bef46cae5710eea53b71660f5`  
		Last Modified: Fri, 21 Feb 2025 00:28:17 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a06f219eecc842356ff61b4a33ce095bdb1fd00d95bc1c0bff428762d9b27cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b776e5de84a69c5b9b2ac04b602d2eb2d45975e39709fc1333f42153fcf922b4`

```dockerfile
```

-	Layers:
	-	`sha256:9ff01b4e93f3228e643a15b9fda3754f658ebfa6e9db482ef1c337fe1caaa019`  
		Last Modified: Fri, 21 Feb 2025 01:49:32 GMT  
		Size: 25.3 KB (25282 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.12-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f247a4cc744d1e3c7ea938b9c5dccd013eb329efd806c1e4043c01a259bc8e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176099156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173b3db67b1661109bb72c5ce669783a00113d61290399aa851c80aeea159ca7`
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
ARG VERSION=24.12.5.81
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fca808cd2b3e3c039a2be80438a8d5bf8517e926c822530b261199385f5f87`  
		Last Modified: Fri, 21 Feb 2025 01:49:50 GMT  
		Size: 140.7 MB (140749605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f175e0bf612a3de3fe3e62a432d0ca03d006be2e98ef7955bfb414c73d880e`  
		Last Modified: Fri, 21 Feb 2025 00:29:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e175d47455d0b91d52335bd6a97ad5840f9228567ddfea2add16d013ef773f62`  
		Last Modified: Fri, 21 Feb 2025 00:29:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b471638593d43d23a8462d518021881932725d6f5026ec821fe29aafb9cfb9d`  
		Last Modified: Fri, 21 Feb 2025 00:29:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298ad3b52107baec77c12974233b4e0595804d5e37029dc5bee25a1b15163174`  
		Last Modified: Fri, 21 Feb 2025 00:29:05 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9f5c8c2d7263b88d7fcf9f9e93636186e9988eb88b54ee101e5abbeb692429`  
		Last Modified: Fri, 21 Feb 2025 00:29:05 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:875ca0f48cedb659437b124cf1d6a754ca81c91e8b72ca8247b5122805eec7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9da86a81c06609f831c0fc789e3255df38f7b67d6fe47e91358b355efdfd7e`

```dockerfile
```

-	Layers:
	-	`sha256:ee727a18d2989639daea3005b755c208849f3d2caf468d0bf85e979222730009`  
		Last Modified: Fri, 21 Feb 2025 01:49:33 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.12.5`

```console
$ docker pull clickhouse@sha256:4d92acbc95bf9dae47aed3a23816b930b8b5e91f598c572a44dc7993ada409b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.12.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:d3adfa7aed1b7335ae82605b943ccc904009effd00517c829d9892c0d8f30da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185897023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9436c271c13b969b10a73c71a021687f9a710570865b6611416d8d12da16287`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=24.12.5.81
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed85509f193d049d0d8771d0e908bd6f68c48bc84da56516de41f6d4eacabb46`  
		Last Modified: Fri, 21 Feb 2025 00:28:37 GMT  
		Size: 7.1 MB (7146946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2634cedca4ec4d6ec49e3dbec5936c936ca00826c1d74f083f67e3885fc3a244`  
		Last Modified: Fri, 21 Feb 2025 01:49:45 GMT  
		Size: 148.3 MB (148343885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493cb809608d009c4d9d795438a9a9c602df95021026e91ece800f6069fb7aa1`  
		Last Modified: Fri, 21 Feb 2025 00:28:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fddacb910bf5f9e99271264a54d143298d3f1b1d9f1cab68930b140a790c558`  
		Last Modified: Fri, 21 Feb 2025 00:28:33 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff15984359130f2898de1cf61ee9023691697cbacdceb5a6043c454f80c3079`  
		Last Modified: Fri, 21 Feb 2025 00:28:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bcf41e381db3a1b11c02096d88f39da331f6d474b30bf8917e1ff24e73012a`  
		Last Modified: Fri, 21 Feb 2025 00:28:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd2c7305b82a0e2578f0228d091a5eaa696107bef46cae5710eea53b71660f5`  
		Last Modified: Fri, 21 Feb 2025 00:28:17 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a06f219eecc842356ff61b4a33ce095bdb1fd00d95bc1c0bff428762d9b27cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b776e5de84a69c5b9b2ac04b602d2eb2d45975e39709fc1333f42153fcf922b4`

```dockerfile
```

-	Layers:
	-	`sha256:9ff01b4e93f3228e643a15b9fda3754f658ebfa6e9db482ef1c337fe1caaa019`  
		Last Modified: Fri, 21 Feb 2025 01:49:32 GMT  
		Size: 25.3 KB (25282 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.12.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f247a4cc744d1e3c7ea938b9c5dccd013eb329efd806c1e4043c01a259bc8e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176099156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173b3db67b1661109bb72c5ce669783a00113d61290399aa851c80aeea159ca7`
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
ARG VERSION=24.12.5.81
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fca808cd2b3e3c039a2be80438a8d5bf8517e926c822530b261199385f5f87`  
		Last Modified: Fri, 21 Feb 2025 01:49:50 GMT  
		Size: 140.7 MB (140749605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f175e0bf612a3de3fe3e62a432d0ca03d006be2e98ef7955bfb414c73d880e`  
		Last Modified: Fri, 21 Feb 2025 00:29:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e175d47455d0b91d52335bd6a97ad5840f9228567ddfea2add16d013ef773f62`  
		Last Modified: Fri, 21 Feb 2025 00:29:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b471638593d43d23a8462d518021881932725d6f5026ec821fe29aafb9cfb9d`  
		Last Modified: Fri, 21 Feb 2025 00:29:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298ad3b52107baec77c12974233b4e0595804d5e37029dc5bee25a1b15163174`  
		Last Modified: Fri, 21 Feb 2025 00:29:05 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9f5c8c2d7263b88d7fcf9f9e93636186e9988eb88b54ee101e5abbeb692429`  
		Last Modified: Fri, 21 Feb 2025 00:29:05 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:875ca0f48cedb659437b124cf1d6a754ca81c91e8b72ca8247b5122805eec7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9da86a81c06609f831c0fc789e3255df38f7b67d6fe47e91358b355efdfd7e`

```dockerfile
```

-	Layers:
	-	`sha256:ee727a18d2989639daea3005b755c208849f3d2caf468d0bf85e979222730009`  
		Last Modified: Fri, 21 Feb 2025 01:49:33 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.12.5-jammy`

```console
$ docker pull clickhouse@sha256:4d92acbc95bf9dae47aed3a23816b930b8b5e91f598c572a44dc7993ada409b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.12.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:d3adfa7aed1b7335ae82605b943ccc904009effd00517c829d9892c0d8f30da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185897023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9436c271c13b969b10a73c71a021687f9a710570865b6611416d8d12da16287`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=24.12.5.81
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed85509f193d049d0d8771d0e908bd6f68c48bc84da56516de41f6d4eacabb46`  
		Last Modified: Fri, 21 Feb 2025 00:28:37 GMT  
		Size: 7.1 MB (7146946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2634cedca4ec4d6ec49e3dbec5936c936ca00826c1d74f083f67e3885fc3a244`  
		Last Modified: Fri, 21 Feb 2025 01:49:45 GMT  
		Size: 148.3 MB (148343885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493cb809608d009c4d9d795438a9a9c602df95021026e91ece800f6069fb7aa1`  
		Last Modified: Fri, 21 Feb 2025 00:28:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fddacb910bf5f9e99271264a54d143298d3f1b1d9f1cab68930b140a790c558`  
		Last Modified: Fri, 21 Feb 2025 00:28:33 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff15984359130f2898de1cf61ee9023691697cbacdceb5a6043c454f80c3079`  
		Last Modified: Fri, 21 Feb 2025 00:28:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bcf41e381db3a1b11c02096d88f39da331f6d474b30bf8917e1ff24e73012a`  
		Last Modified: Fri, 21 Feb 2025 00:28:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd2c7305b82a0e2578f0228d091a5eaa696107bef46cae5710eea53b71660f5`  
		Last Modified: Fri, 21 Feb 2025 00:28:17 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a06f219eecc842356ff61b4a33ce095bdb1fd00d95bc1c0bff428762d9b27cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b776e5de84a69c5b9b2ac04b602d2eb2d45975e39709fc1333f42153fcf922b4`

```dockerfile
```

-	Layers:
	-	`sha256:9ff01b4e93f3228e643a15b9fda3754f658ebfa6e9db482ef1c337fe1caaa019`  
		Last Modified: Fri, 21 Feb 2025 01:49:32 GMT  
		Size: 25.3 KB (25282 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.12.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f247a4cc744d1e3c7ea938b9c5dccd013eb329efd806c1e4043c01a259bc8e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176099156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173b3db67b1661109bb72c5ce669783a00113d61290399aa851c80aeea159ca7`
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
ARG VERSION=24.12.5.81
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fca808cd2b3e3c039a2be80438a8d5bf8517e926c822530b261199385f5f87`  
		Last Modified: Fri, 21 Feb 2025 01:49:50 GMT  
		Size: 140.7 MB (140749605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f175e0bf612a3de3fe3e62a432d0ca03d006be2e98ef7955bfb414c73d880e`  
		Last Modified: Fri, 21 Feb 2025 00:29:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e175d47455d0b91d52335bd6a97ad5840f9228567ddfea2add16d013ef773f62`  
		Last Modified: Fri, 21 Feb 2025 00:29:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b471638593d43d23a8462d518021881932725d6f5026ec821fe29aafb9cfb9d`  
		Last Modified: Fri, 21 Feb 2025 00:29:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298ad3b52107baec77c12974233b4e0595804d5e37029dc5bee25a1b15163174`  
		Last Modified: Fri, 21 Feb 2025 00:29:05 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9f5c8c2d7263b88d7fcf9f9e93636186e9988eb88b54ee101e5abbeb692429`  
		Last Modified: Fri, 21 Feb 2025 00:29:05 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:875ca0f48cedb659437b124cf1d6a754ca81c91e8b72ca8247b5122805eec7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9da86a81c06609f831c0fc789e3255df38f7b67d6fe47e91358b355efdfd7e`

```dockerfile
```

-	Layers:
	-	`sha256:ee727a18d2989639daea3005b755c208849f3d2caf468d0bf85e979222730009`  
		Last Modified: Fri, 21 Feb 2025 01:49:33 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.12.5.81`

```console
$ docker pull clickhouse@sha256:4d92acbc95bf9dae47aed3a23816b930b8b5e91f598c572a44dc7993ada409b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.12.5.81` - linux; amd64

```console
$ docker pull clickhouse@sha256:d3adfa7aed1b7335ae82605b943ccc904009effd00517c829d9892c0d8f30da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185897023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9436c271c13b969b10a73c71a021687f9a710570865b6611416d8d12da16287`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=24.12.5.81
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed85509f193d049d0d8771d0e908bd6f68c48bc84da56516de41f6d4eacabb46`  
		Last Modified: Fri, 21 Feb 2025 00:28:37 GMT  
		Size: 7.1 MB (7146946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2634cedca4ec4d6ec49e3dbec5936c936ca00826c1d74f083f67e3885fc3a244`  
		Last Modified: Fri, 21 Feb 2025 01:49:45 GMT  
		Size: 148.3 MB (148343885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493cb809608d009c4d9d795438a9a9c602df95021026e91ece800f6069fb7aa1`  
		Last Modified: Fri, 21 Feb 2025 00:28:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fddacb910bf5f9e99271264a54d143298d3f1b1d9f1cab68930b140a790c558`  
		Last Modified: Fri, 21 Feb 2025 00:28:33 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff15984359130f2898de1cf61ee9023691697cbacdceb5a6043c454f80c3079`  
		Last Modified: Fri, 21 Feb 2025 00:28:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bcf41e381db3a1b11c02096d88f39da331f6d474b30bf8917e1ff24e73012a`  
		Last Modified: Fri, 21 Feb 2025 00:28:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd2c7305b82a0e2578f0228d091a5eaa696107bef46cae5710eea53b71660f5`  
		Last Modified: Fri, 21 Feb 2025 00:28:17 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12.5.81` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a06f219eecc842356ff61b4a33ce095bdb1fd00d95bc1c0bff428762d9b27cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b776e5de84a69c5b9b2ac04b602d2eb2d45975e39709fc1333f42153fcf922b4`

```dockerfile
```

-	Layers:
	-	`sha256:9ff01b4e93f3228e643a15b9fda3754f658ebfa6e9db482ef1c337fe1caaa019`  
		Last Modified: Fri, 21 Feb 2025 01:49:32 GMT  
		Size: 25.3 KB (25282 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.12.5.81` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f247a4cc744d1e3c7ea938b9c5dccd013eb329efd806c1e4043c01a259bc8e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176099156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173b3db67b1661109bb72c5ce669783a00113d61290399aa851c80aeea159ca7`
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
ARG VERSION=24.12.5.81
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fca808cd2b3e3c039a2be80438a8d5bf8517e926c822530b261199385f5f87`  
		Last Modified: Fri, 21 Feb 2025 01:49:50 GMT  
		Size: 140.7 MB (140749605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f175e0bf612a3de3fe3e62a432d0ca03d006be2e98ef7955bfb414c73d880e`  
		Last Modified: Fri, 21 Feb 2025 00:29:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e175d47455d0b91d52335bd6a97ad5840f9228567ddfea2add16d013ef773f62`  
		Last Modified: Fri, 21 Feb 2025 00:29:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b471638593d43d23a8462d518021881932725d6f5026ec821fe29aafb9cfb9d`  
		Last Modified: Fri, 21 Feb 2025 00:29:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298ad3b52107baec77c12974233b4e0595804d5e37029dc5bee25a1b15163174`  
		Last Modified: Fri, 21 Feb 2025 00:29:05 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9f5c8c2d7263b88d7fcf9f9e93636186e9988eb88b54ee101e5abbeb692429`  
		Last Modified: Fri, 21 Feb 2025 00:29:05 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12.5.81` - unknown; unknown

```console
$ docker pull clickhouse@sha256:875ca0f48cedb659437b124cf1d6a754ca81c91e8b72ca8247b5122805eec7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9da86a81c06609f831c0fc789e3255df38f7b67d6fe47e91358b355efdfd7e`

```dockerfile
```

-	Layers:
	-	`sha256:ee727a18d2989639daea3005b755c208849f3d2caf468d0bf85e979222730009`  
		Last Modified: Fri, 21 Feb 2025 01:49:33 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.12.5.81-jammy`

```console
$ docker pull clickhouse@sha256:4d92acbc95bf9dae47aed3a23816b930b8b5e91f598c572a44dc7993ada409b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.12.5.81-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:d3adfa7aed1b7335ae82605b943ccc904009effd00517c829d9892c0d8f30da7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.9 MB (185897023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9436c271c13b969b10a73c71a021687f9a710570865b6611416d8d12da16287`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=24.12.5.81
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed85509f193d049d0d8771d0e908bd6f68c48bc84da56516de41f6d4eacabb46`  
		Last Modified: Fri, 21 Feb 2025 00:28:37 GMT  
		Size: 7.1 MB (7146946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2634cedca4ec4d6ec49e3dbec5936c936ca00826c1d74f083f67e3885fc3a244`  
		Last Modified: Fri, 21 Feb 2025 01:49:45 GMT  
		Size: 148.3 MB (148343885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493cb809608d009c4d9d795438a9a9c602df95021026e91ece800f6069fb7aa1`  
		Last Modified: Fri, 21 Feb 2025 00:28:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fddacb910bf5f9e99271264a54d143298d3f1b1d9f1cab68930b140a790c558`  
		Last Modified: Fri, 21 Feb 2025 00:28:33 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff15984359130f2898de1cf61ee9023691697cbacdceb5a6043c454f80c3079`  
		Last Modified: Fri, 21 Feb 2025 00:28:30 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26bcf41e381db3a1b11c02096d88f39da331f6d474b30bf8917e1ff24e73012a`  
		Last Modified: Fri, 21 Feb 2025 00:28:14 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd2c7305b82a0e2578f0228d091a5eaa696107bef46cae5710eea53b71660f5`  
		Last Modified: Fri, 21 Feb 2025 00:28:17 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12.5.81-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:a06f219eecc842356ff61b4a33ce095bdb1fd00d95bc1c0bff428762d9b27cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b776e5de84a69c5b9b2ac04b602d2eb2d45975e39709fc1333f42153fcf922b4`

```dockerfile
```

-	Layers:
	-	`sha256:9ff01b4e93f3228e643a15b9fda3754f658ebfa6e9db482ef1c337fe1caaa019`  
		Last Modified: Fri, 21 Feb 2025 01:49:32 GMT  
		Size: 25.3 KB (25282 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.12.5.81-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f247a4cc744d1e3c7ea938b9c5dccd013eb329efd806c1e4043c01a259bc8e06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176099156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173b3db67b1661109bb72c5ce669783a00113d61290399aa851c80aeea159ca7`
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
ARG VERSION=24.12.5.81
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.12.5.81 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fca808cd2b3e3c039a2be80438a8d5bf8517e926c822530b261199385f5f87`  
		Last Modified: Fri, 21 Feb 2025 01:49:50 GMT  
		Size: 140.7 MB (140749605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f175e0bf612a3de3fe3e62a432d0ca03d006be2e98ef7955bfb414c73d880e`  
		Last Modified: Fri, 21 Feb 2025 00:29:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e175d47455d0b91d52335bd6a97ad5840f9228567ddfea2add16d013ef773f62`  
		Last Modified: Fri, 21 Feb 2025 00:29:09 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b471638593d43d23a8462d518021881932725d6f5026ec821fe29aafb9cfb9d`  
		Last Modified: Fri, 21 Feb 2025 00:29:04 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298ad3b52107baec77c12974233b4e0595804d5e37029dc5bee25a1b15163174`  
		Last Modified: Fri, 21 Feb 2025 00:29:05 GMT  
		Size: 365.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9f5c8c2d7263b88d7fcf9f9e93636186e9988eb88b54ee101e5abbeb692429`  
		Last Modified: Fri, 21 Feb 2025 00:29:05 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.12.5.81-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:875ca0f48cedb659437b124cf1d6a754ca81c91e8b72ca8247b5122805eec7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe9da86a81c06609f831c0fc789e3255df38f7b67d6fe47e91358b355efdfd7e`

```dockerfile
```

-	Layers:
	-	`sha256:ee727a18d2989639daea3005b755c208849f3d2caf468d0bf85e979222730009`  
		Last Modified: Fri, 21 Feb 2025 01:49:33 GMT  
		Size: 25.5 KB (25470 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3`

```console
$ docker pull clickhouse@sha256:931da3d04f827b3247445c02dc113b5f9d8b314f08445dd4a2517981ae513a8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:79b655d08e8257a96eb49e1bc684ce6d41edf50836976f11084c30966d6e1e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297480764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3119fb517cea45933eccaba6f5b584771a023bfae17614580858f19bc0f26066`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
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
ARG VERSION=24.3.18.7
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2d240efd4abf3bbe50ec6591036ca5847e891b7488d2a4db1965a1b9639f9`  
		Last Modified: Fri, 21 Feb 2025 00:28:47 GMT  
		Size: 8.8 MB (8796741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44b39c9abaf866f35c5b66a1e2458d4a761978510023041d968e7a22d7fa5ec`  
		Last Modified: Fri, 21 Feb 2025 01:50:01 GMT  
		Size: 260.3 MB (260304827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79380e4eaaa63da2a56630e698af0536264eb92916b2779a37717de30669827`  
		Last Modified: Fri, 21 Feb 2025 00:28:36 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4538dff674e32f86553a20532c8d3d54946d2c6a3e91d6465a97853e092952`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805acd6c91fdee35f35c0a9f1546e2b562e8b5453c42d735c1ca83d8811df194`  
		Last Modified: Fri, 21 Feb 2025 00:28:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6867a158a62c923d1df880e3ec00ac515224d13f73a2c2514adad76408245d`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffe30c260941df3ddc17bdf88840d7776812356665cb7e4ea54361ed41e4355`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3733e5465e7f8630103a541aa920dad395ced628c3ac701adb1b5d583ca35c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62a9ea0bb3e9360c5b3f3c5584b93081eeacad320167c11abde70aab34f3463`

```dockerfile
```

-	Layers:
	-	`sha256:b611ecd85f5ff874461c01f0e3e9a26c7576e6e3bb43effb9045d20bf4f1ec36`  
		Last Modified: Fri, 21 Feb 2025 01:49:42 GMT  
		Size: 25.3 KB (25267 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f86f3ad223e9e2138c1f3b97140c4c632f35dcb370ab0f7efdc099eca12f05fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286052551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732d4b968f118c37645155e527efc539dcb6d5c201b5d40f10eaf1c5fd0bf6b1`
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
ARG VERSION=24.3.18.7
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdf5cd267dcedb2f36ac0df5347aeaa46de4ca107c1946d1239bb4cdf542f66`  
		Last Modified: Fri, 21 Feb 2025 01:50:02 GMT  
		Size: 250.6 MB (250555557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fd802368a331e6469fce1983422f4083b26753c7899866de077e03b3e4ee21`  
		Last Modified: Fri, 21 Feb 2025 00:32:15 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b26d94a6f6151c2fde8d42914df708614842eff5318679056d4d38044b4cdab`  
		Last Modified: Fri, 21 Feb 2025 00:32:21 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da3d3b40ad96709e141622f1683a990d2fd1de14a82d623c91139a7cbbb1d0d`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7798e287ff17fc7bf2e9cee64cbfcdf5d9d779c1a7ec243cce8273150a011abe`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b24d7aa46a20120594e644e87525dcad29ec84fb0ddef8e05475766df1af933`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1df45f3fe8993b6c4b0d897c12eb5b859cfe9bd2b11261307d726f26ad3ff85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474c57aa8eeacd28ca284336ed351d8340a06655e622c821e033933754efb3a6`

```dockerfile
```

-	Layers:
	-	`sha256:dfd4b6b7c98afe5bf1be3c749d0976ef69ab33d9f1cb12aa5bf599b183e595c7`  
		Last Modified: Fri, 21 Feb 2025 01:49:43 GMT  
		Size: 25.5 KB (25455 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3-focal`

```console
$ docker pull clickhouse@sha256:931da3d04f827b3247445c02dc113b5f9d8b314f08445dd4a2517981ae513a8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:79b655d08e8257a96eb49e1bc684ce6d41edf50836976f11084c30966d6e1e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297480764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3119fb517cea45933eccaba6f5b584771a023bfae17614580858f19bc0f26066`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
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
ARG VERSION=24.3.18.7
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2d240efd4abf3bbe50ec6591036ca5847e891b7488d2a4db1965a1b9639f9`  
		Last Modified: Fri, 21 Feb 2025 00:28:47 GMT  
		Size: 8.8 MB (8796741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44b39c9abaf866f35c5b66a1e2458d4a761978510023041d968e7a22d7fa5ec`  
		Last Modified: Fri, 21 Feb 2025 01:50:01 GMT  
		Size: 260.3 MB (260304827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79380e4eaaa63da2a56630e698af0536264eb92916b2779a37717de30669827`  
		Last Modified: Fri, 21 Feb 2025 00:28:36 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4538dff674e32f86553a20532c8d3d54946d2c6a3e91d6465a97853e092952`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805acd6c91fdee35f35c0a9f1546e2b562e8b5453c42d735c1ca83d8811df194`  
		Last Modified: Fri, 21 Feb 2025 00:28:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6867a158a62c923d1df880e3ec00ac515224d13f73a2c2514adad76408245d`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffe30c260941df3ddc17bdf88840d7776812356665cb7e4ea54361ed41e4355`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3733e5465e7f8630103a541aa920dad395ced628c3ac701adb1b5d583ca35c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62a9ea0bb3e9360c5b3f3c5584b93081eeacad320167c11abde70aab34f3463`

```dockerfile
```

-	Layers:
	-	`sha256:b611ecd85f5ff874461c01f0e3e9a26c7576e6e3bb43effb9045d20bf4f1ec36`  
		Last Modified: Fri, 21 Feb 2025 01:49:42 GMT  
		Size: 25.3 KB (25267 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f86f3ad223e9e2138c1f3b97140c4c632f35dcb370ab0f7efdc099eca12f05fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286052551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732d4b968f118c37645155e527efc539dcb6d5c201b5d40f10eaf1c5fd0bf6b1`
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
ARG VERSION=24.3.18.7
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdf5cd267dcedb2f36ac0df5347aeaa46de4ca107c1946d1239bb4cdf542f66`  
		Last Modified: Fri, 21 Feb 2025 01:50:02 GMT  
		Size: 250.6 MB (250555557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fd802368a331e6469fce1983422f4083b26753c7899866de077e03b3e4ee21`  
		Last Modified: Fri, 21 Feb 2025 00:32:15 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b26d94a6f6151c2fde8d42914df708614842eff5318679056d4d38044b4cdab`  
		Last Modified: Fri, 21 Feb 2025 00:32:21 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da3d3b40ad96709e141622f1683a990d2fd1de14a82d623c91139a7cbbb1d0d`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7798e287ff17fc7bf2e9cee64cbfcdf5d9d779c1a7ec243cce8273150a011abe`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b24d7aa46a20120594e644e87525dcad29ec84fb0ddef8e05475766df1af933`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1df45f3fe8993b6c4b0d897c12eb5b859cfe9bd2b11261307d726f26ad3ff85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474c57aa8eeacd28ca284336ed351d8340a06655e622c821e033933754efb3a6`

```dockerfile
```

-	Layers:
	-	`sha256:dfd4b6b7c98afe5bf1be3c749d0976ef69ab33d9f1cb12aa5bf599b183e595c7`  
		Last Modified: Fri, 21 Feb 2025 01:49:43 GMT  
		Size: 25.5 KB (25455 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3.18`

```console
$ docker pull clickhouse@sha256:931da3d04f827b3247445c02dc113b5f9d8b314f08445dd4a2517981ae513a8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3.18` - linux; amd64

```console
$ docker pull clickhouse@sha256:79b655d08e8257a96eb49e1bc684ce6d41edf50836976f11084c30966d6e1e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297480764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3119fb517cea45933eccaba6f5b584771a023bfae17614580858f19bc0f26066`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
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
ARG VERSION=24.3.18.7
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2d240efd4abf3bbe50ec6591036ca5847e891b7488d2a4db1965a1b9639f9`  
		Last Modified: Fri, 21 Feb 2025 00:28:47 GMT  
		Size: 8.8 MB (8796741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44b39c9abaf866f35c5b66a1e2458d4a761978510023041d968e7a22d7fa5ec`  
		Last Modified: Fri, 21 Feb 2025 01:50:01 GMT  
		Size: 260.3 MB (260304827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79380e4eaaa63da2a56630e698af0536264eb92916b2779a37717de30669827`  
		Last Modified: Fri, 21 Feb 2025 00:28:36 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4538dff674e32f86553a20532c8d3d54946d2c6a3e91d6465a97853e092952`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805acd6c91fdee35f35c0a9f1546e2b562e8b5453c42d735c1ca83d8811df194`  
		Last Modified: Fri, 21 Feb 2025 00:28:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6867a158a62c923d1df880e3ec00ac515224d13f73a2c2514adad76408245d`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffe30c260941df3ddc17bdf88840d7776812356665cb7e4ea54361ed41e4355`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.18` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3733e5465e7f8630103a541aa920dad395ced628c3ac701adb1b5d583ca35c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62a9ea0bb3e9360c5b3f3c5584b93081eeacad320167c11abde70aab34f3463`

```dockerfile
```

-	Layers:
	-	`sha256:b611ecd85f5ff874461c01f0e3e9a26c7576e6e3bb43effb9045d20bf4f1ec36`  
		Last Modified: Fri, 21 Feb 2025 01:49:42 GMT  
		Size: 25.3 KB (25267 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3.18` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f86f3ad223e9e2138c1f3b97140c4c632f35dcb370ab0f7efdc099eca12f05fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286052551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732d4b968f118c37645155e527efc539dcb6d5c201b5d40f10eaf1c5fd0bf6b1`
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
ARG VERSION=24.3.18.7
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdf5cd267dcedb2f36ac0df5347aeaa46de4ca107c1946d1239bb4cdf542f66`  
		Last Modified: Fri, 21 Feb 2025 01:50:02 GMT  
		Size: 250.6 MB (250555557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fd802368a331e6469fce1983422f4083b26753c7899866de077e03b3e4ee21`  
		Last Modified: Fri, 21 Feb 2025 00:32:15 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b26d94a6f6151c2fde8d42914df708614842eff5318679056d4d38044b4cdab`  
		Last Modified: Fri, 21 Feb 2025 00:32:21 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da3d3b40ad96709e141622f1683a990d2fd1de14a82d623c91139a7cbbb1d0d`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7798e287ff17fc7bf2e9cee64cbfcdf5d9d779c1a7ec243cce8273150a011abe`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b24d7aa46a20120594e644e87525dcad29ec84fb0ddef8e05475766df1af933`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.18` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1df45f3fe8993b6c4b0d897c12eb5b859cfe9bd2b11261307d726f26ad3ff85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474c57aa8eeacd28ca284336ed351d8340a06655e622c821e033933754efb3a6`

```dockerfile
```

-	Layers:
	-	`sha256:dfd4b6b7c98afe5bf1be3c749d0976ef69ab33d9f1cb12aa5bf599b183e595c7`  
		Last Modified: Fri, 21 Feb 2025 01:49:43 GMT  
		Size: 25.5 KB (25455 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3.18-focal`

```console
$ docker pull clickhouse@sha256:931da3d04f827b3247445c02dc113b5f9d8b314f08445dd4a2517981ae513a8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3.18-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:79b655d08e8257a96eb49e1bc684ce6d41edf50836976f11084c30966d6e1e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297480764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3119fb517cea45933eccaba6f5b584771a023bfae17614580858f19bc0f26066`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
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
ARG VERSION=24.3.18.7
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2d240efd4abf3bbe50ec6591036ca5847e891b7488d2a4db1965a1b9639f9`  
		Last Modified: Fri, 21 Feb 2025 00:28:47 GMT  
		Size: 8.8 MB (8796741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44b39c9abaf866f35c5b66a1e2458d4a761978510023041d968e7a22d7fa5ec`  
		Last Modified: Fri, 21 Feb 2025 01:50:01 GMT  
		Size: 260.3 MB (260304827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79380e4eaaa63da2a56630e698af0536264eb92916b2779a37717de30669827`  
		Last Modified: Fri, 21 Feb 2025 00:28:36 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4538dff674e32f86553a20532c8d3d54946d2c6a3e91d6465a97853e092952`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805acd6c91fdee35f35c0a9f1546e2b562e8b5453c42d735c1ca83d8811df194`  
		Last Modified: Fri, 21 Feb 2025 00:28:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6867a158a62c923d1df880e3ec00ac515224d13f73a2c2514adad76408245d`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffe30c260941df3ddc17bdf88840d7776812356665cb7e4ea54361ed41e4355`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.18-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3733e5465e7f8630103a541aa920dad395ced628c3ac701adb1b5d583ca35c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62a9ea0bb3e9360c5b3f3c5584b93081eeacad320167c11abde70aab34f3463`

```dockerfile
```

-	Layers:
	-	`sha256:b611ecd85f5ff874461c01f0e3e9a26c7576e6e3bb43effb9045d20bf4f1ec36`  
		Last Modified: Fri, 21 Feb 2025 01:49:42 GMT  
		Size: 25.3 KB (25267 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3.18-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f86f3ad223e9e2138c1f3b97140c4c632f35dcb370ab0f7efdc099eca12f05fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286052551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732d4b968f118c37645155e527efc539dcb6d5c201b5d40f10eaf1c5fd0bf6b1`
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
ARG VERSION=24.3.18.7
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdf5cd267dcedb2f36ac0df5347aeaa46de4ca107c1946d1239bb4cdf542f66`  
		Last Modified: Fri, 21 Feb 2025 01:50:02 GMT  
		Size: 250.6 MB (250555557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fd802368a331e6469fce1983422f4083b26753c7899866de077e03b3e4ee21`  
		Last Modified: Fri, 21 Feb 2025 00:32:15 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b26d94a6f6151c2fde8d42914df708614842eff5318679056d4d38044b4cdab`  
		Last Modified: Fri, 21 Feb 2025 00:32:21 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da3d3b40ad96709e141622f1683a990d2fd1de14a82d623c91139a7cbbb1d0d`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7798e287ff17fc7bf2e9cee64cbfcdf5d9d779c1a7ec243cce8273150a011abe`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b24d7aa46a20120594e644e87525dcad29ec84fb0ddef8e05475766df1af933`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.18-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1df45f3fe8993b6c4b0d897c12eb5b859cfe9bd2b11261307d726f26ad3ff85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474c57aa8eeacd28ca284336ed351d8340a06655e622c821e033933754efb3a6`

```dockerfile
```

-	Layers:
	-	`sha256:dfd4b6b7c98afe5bf1be3c749d0976ef69ab33d9f1cb12aa5bf599b183e595c7`  
		Last Modified: Fri, 21 Feb 2025 01:49:43 GMT  
		Size: 25.5 KB (25455 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3.18.7`

```console
$ docker pull clickhouse@sha256:931da3d04f827b3247445c02dc113b5f9d8b314f08445dd4a2517981ae513a8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3.18.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:79b655d08e8257a96eb49e1bc684ce6d41edf50836976f11084c30966d6e1e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297480764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3119fb517cea45933eccaba6f5b584771a023bfae17614580858f19bc0f26066`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
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
ARG VERSION=24.3.18.7
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2d240efd4abf3bbe50ec6591036ca5847e891b7488d2a4db1965a1b9639f9`  
		Last Modified: Fri, 21 Feb 2025 00:28:47 GMT  
		Size: 8.8 MB (8796741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44b39c9abaf866f35c5b66a1e2458d4a761978510023041d968e7a22d7fa5ec`  
		Last Modified: Fri, 21 Feb 2025 01:50:01 GMT  
		Size: 260.3 MB (260304827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79380e4eaaa63da2a56630e698af0536264eb92916b2779a37717de30669827`  
		Last Modified: Fri, 21 Feb 2025 00:28:36 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4538dff674e32f86553a20532c8d3d54946d2c6a3e91d6465a97853e092952`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805acd6c91fdee35f35c0a9f1546e2b562e8b5453c42d735c1ca83d8811df194`  
		Last Modified: Fri, 21 Feb 2025 00:28:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6867a158a62c923d1df880e3ec00ac515224d13f73a2c2514adad76408245d`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffe30c260941df3ddc17bdf88840d7776812356665cb7e4ea54361ed41e4355`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.18.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3733e5465e7f8630103a541aa920dad395ced628c3ac701adb1b5d583ca35c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62a9ea0bb3e9360c5b3f3c5584b93081eeacad320167c11abde70aab34f3463`

```dockerfile
```

-	Layers:
	-	`sha256:b611ecd85f5ff874461c01f0e3e9a26c7576e6e3bb43effb9045d20bf4f1ec36`  
		Last Modified: Fri, 21 Feb 2025 01:49:42 GMT  
		Size: 25.3 KB (25267 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3.18.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f86f3ad223e9e2138c1f3b97140c4c632f35dcb370ab0f7efdc099eca12f05fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286052551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732d4b968f118c37645155e527efc539dcb6d5c201b5d40f10eaf1c5fd0bf6b1`
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
ARG VERSION=24.3.18.7
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdf5cd267dcedb2f36ac0df5347aeaa46de4ca107c1946d1239bb4cdf542f66`  
		Last Modified: Fri, 21 Feb 2025 01:50:02 GMT  
		Size: 250.6 MB (250555557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fd802368a331e6469fce1983422f4083b26753c7899866de077e03b3e4ee21`  
		Last Modified: Fri, 21 Feb 2025 00:32:15 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b26d94a6f6151c2fde8d42914df708614842eff5318679056d4d38044b4cdab`  
		Last Modified: Fri, 21 Feb 2025 00:32:21 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da3d3b40ad96709e141622f1683a990d2fd1de14a82d623c91139a7cbbb1d0d`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7798e287ff17fc7bf2e9cee64cbfcdf5d9d779c1a7ec243cce8273150a011abe`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b24d7aa46a20120594e644e87525dcad29ec84fb0ddef8e05475766df1af933`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.18.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1df45f3fe8993b6c4b0d897c12eb5b859cfe9bd2b11261307d726f26ad3ff85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474c57aa8eeacd28ca284336ed351d8340a06655e622c821e033933754efb3a6`

```dockerfile
```

-	Layers:
	-	`sha256:dfd4b6b7c98afe5bf1be3c749d0976ef69ab33d9f1cb12aa5bf599b183e595c7`  
		Last Modified: Fri, 21 Feb 2025 01:49:43 GMT  
		Size: 25.5 KB (25455 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.3.18.7-focal`

```console
$ docker pull clickhouse@sha256:931da3d04f827b3247445c02dc113b5f9d8b314f08445dd4a2517981ae513a8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.3.18.7-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:79b655d08e8257a96eb49e1bc684ce6d41edf50836976f11084c30966d6e1e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297480764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3119fb517cea45933eccaba6f5b584771a023bfae17614580858f19bc0f26066`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
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
ARG VERSION=24.3.18.7
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f2d240efd4abf3bbe50ec6591036ca5847e891b7488d2a4db1965a1b9639f9`  
		Last Modified: Fri, 21 Feb 2025 00:28:47 GMT  
		Size: 8.8 MB (8796741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44b39c9abaf866f35c5b66a1e2458d4a761978510023041d968e7a22d7fa5ec`  
		Last Modified: Fri, 21 Feb 2025 01:50:01 GMT  
		Size: 260.3 MB (260304827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79380e4eaaa63da2a56630e698af0536264eb92916b2779a37717de30669827`  
		Last Modified: Fri, 21 Feb 2025 00:28:36 GMT  
		Size: 350.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4538dff674e32f86553a20532c8d3d54946d2c6a3e91d6465a97853e092952`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 863.5 KB (863472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805acd6c91fdee35f35c0a9f1546e2b562e8b5453c42d735c1ca83d8811df194`  
		Last Modified: Fri, 21 Feb 2025 00:28:37 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d6867a158a62c923d1df880e3ec00ac515224d13f73a2c2514adad76408245d`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffe30c260941df3ddc17bdf88840d7776812356665cb7e4ea54361ed41e4355`  
		Last Modified: Fri, 21 Feb 2025 00:28:38 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.18.7-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3733e5465e7f8630103a541aa920dad395ced628c3ac701adb1b5d583ca35c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e62a9ea0bb3e9360c5b3f3c5584b93081eeacad320167c11abde70aab34f3463`

```dockerfile
```

-	Layers:
	-	`sha256:b611ecd85f5ff874461c01f0e3e9a26c7576e6e3bb43effb9045d20bf4f1ec36`  
		Last Modified: Fri, 21 Feb 2025 01:49:42 GMT  
		Size: 25.3 KB (25267 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:24.3.18.7-focal` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f86f3ad223e9e2138c1f3b97140c4c632f35dcb370ab0f7efdc099eca12f05fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.1 MB (286052551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732d4b968f118c37645155e527efc539dcb6d5c201b5d40f10eaf1c5fd0bf6b1`
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
ARG VERSION=24.3.18.7
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=24.3.18.7 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdf5cd267dcedb2f36ac0df5347aeaa46de4ca107c1946d1239bb4cdf542f66`  
		Last Modified: Fri, 21 Feb 2025 01:50:02 GMT  
		Size: 250.6 MB (250555557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fd802368a331e6469fce1983422f4083b26753c7899866de077e03b3e4ee21`  
		Last Modified: Fri, 21 Feb 2025 00:32:15 GMT  
		Size: 349.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b26d94a6f6151c2fde8d42914df708614842eff5318679056d4d38044b4cdab`  
		Last Modified: Fri, 21 Feb 2025 00:32:21 GMT  
		Size: 863.5 KB (863478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da3d3b40ad96709e141622f1683a990d2fd1de14a82d623c91139a7cbbb1d0d`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7798e287ff17fc7bf2e9cee64cbfcdf5d9d779c1a7ec243cce8273150a011abe`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b24d7aa46a20120594e644e87525dcad29ec84fb0ddef8e05475766df1af933`  
		Last Modified: Fri, 21 Feb 2025 00:32:16 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.3.18.7-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:1df45f3fe8993b6c4b0d897c12eb5b859cfe9bd2b11261307d726f26ad3ff85a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474c57aa8eeacd28ca284336ed351d8340a06655e622c821e033933754efb3a6`

```dockerfile
```

-	Layers:
	-	`sha256:dfd4b6b7c98afe5bf1be3c749d0976ef69ab33d9f1cb12aa5bf599b183e595c7`  
		Last Modified: Fri, 21 Feb 2025 01:49:43 GMT  
		Size: 25.5 KB (25455 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8`

```console
$ docker pull clickhouse@sha256:69255ecc8de97843649e35089c68ff8eb61668f14754ec614c189a23717d632b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:fecaf7b88964f3d39aadf9dee40f4a18ff85406f349cac5a966dabd7ce28ee13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178872609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6374f8f3e1a7253bafa4eea700d16e2ebf691f0e614e028173fbb38e80fc1f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5517f3eb5548b7c503d1d73b118d8b8fe212ff5b2089ddccabf2a9735602cc8`  
		Last Modified: Fri, 21 Feb 2025 00:28:10 GMT  
		Size: 8.8 MB (8796697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291cb7d6e97379312fae3fe1ab1b7297dc1beb52d157f9fce22c4fc4cc837428`  
		Last Modified: Fri, 21 Feb 2025 01:50:09 GMT  
		Size: 141.7 MB (141696883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed8b3fd82a250925f55b946f2bdd746a082ecd2970a4bf9a2418176501081e1`  
		Last Modified: Fri, 21 Feb 2025 00:28:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7ce34b821ae068e160f65aa3febf4c17101d2a9daf8a4b4e7a26208bb7d22`  
		Last Modified: Fri, 21 Feb 2025 00:28:13 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b523b9e65cb5720ce8ae73e538ef230e761b8f43cffd492d3639cb0e622d0ff`  
		Last Modified: Fri, 21 Feb 2025 00:28:03 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635515f670f0e003d2b90593b19485fe69078d7eb5b47b2aa4304f93edafae3`  
		Last Modified: Fri, 21 Feb 2025 00:28:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ea67607234d720e0dd13aadfa57cb3f7803ecc3a0a6062e3676e977603769`  
		Last Modified: Fri, 21 Feb 2025 00:28:05 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eae752361b103a1dc25497f73110e35700aa80da08967d88b3c09fff56c1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bcf5d320bb0d9db63bf594c65b311aa2e9516d59d323663096fcb3c613552e`

```dockerfile
```

-	Layers:
	-	`sha256:91f7615237ca92acd05b32c4c4d97429dbf495bfa5945c497eca59bd41e3131e`  
		Last Modified: Fri, 21 Feb 2025 01:49:53 GMT  
		Size: 25.9 KB (25890 bytes)  
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
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 01:50:10 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:31:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:31:13 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:31:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
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
		Last Modified: Fri, 21 Feb 2025 01:49:55 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8-focal`

```console
$ docker pull clickhouse@sha256:69255ecc8de97843649e35089c68ff8eb61668f14754ec614c189a23717d632b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:fecaf7b88964f3d39aadf9dee40f4a18ff85406f349cac5a966dabd7ce28ee13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178872609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6374f8f3e1a7253bafa4eea700d16e2ebf691f0e614e028173fbb38e80fc1f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5517f3eb5548b7c503d1d73b118d8b8fe212ff5b2089ddccabf2a9735602cc8`  
		Last Modified: Fri, 21 Feb 2025 00:28:10 GMT  
		Size: 8.8 MB (8796697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291cb7d6e97379312fae3fe1ab1b7297dc1beb52d157f9fce22c4fc4cc837428`  
		Last Modified: Fri, 21 Feb 2025 01:50:09 GMT  
		Size: 141.7 MB (141696883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed8b3fd82a250925f55b946f2bdd746a082ecd2970a4bf9a2418176501081e1`  
		Last Modified: Fri, 21 Feb 2025 00:28:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7ce34b821ae068e160f65aa3febf4c17101d2a9daf8a4b4e7a26208bb7d22`  
		Last Modified: Fri, 21 Feb 2025 00:28:13 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b523b9e65cb5720ce8ae73e538ef230e761b8f43cffd492d3639cb0e622d0ff`  
		Last Modified: Fri, 21 Feb 2025 00:28:03 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635515f670f0e003d2b90593b19485fe69078d7eb5b47b2aa4304f93edafae3`  
		Last Modified: Fri, 21 Feb 2025 00:28:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ea67607234d720e0dd13aadfa57cb3f7803ecc3a0a6062e3676e977603769`  
		Last Modified: Fri, 21 Feb 2025 00:28:05 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eae752361b103a1dc25497f73110e35700aa80da08967d88b3c09fff56c1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bcf5d320bb0d9db63bf594c65b311aa2e9516d59d323663096fcb3c613552e`

```dockerfile
```

-	Layers:
	-	`sha256:91f7615237ca92acd05b32c4c4d97429dbf495bfa5945c497eca59bd41e3131e`  
		Last Modified: Fri, 21 Feb 2025 01:49:53 GMT  
		Size: 25.9 KB (25890 bytes)  
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
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 01:50:10 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:31:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:31:13 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:31:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
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
		Last Modified: Fri, 21 Feb 2025 01:49:55 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.14`

```console
$ docker pull clickhouse@sha256:69255ecc8de97843649e35089c68ff8eb61668f14754ec614c189a23717d632b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.14` - linux; amd64

```console
$ docker pull clickhouse@sha256:fecaf7b88964f3d39aadf9dee40f4a18ff85406f349cac5a966dabd7ce28ee13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178872609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6374f8f3e1a7253bafa4eea700d16e2ebf691f0e614e028173fbb38e80fc1f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5517f3eb5548b7c503d1d73b118d8b8fe212ff5b2089ddccabf2a9735602cc8`  
		Last Modified: Fri, 21 Feb 2025 00:28:10 GMT  
		Size: 8.8 MB (8796697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291cb7d6e97379312fae3fe1ab1b7297dc1beb52d157f9fce22c4fc4cc837428`  
		Last Modified: Fri, 21 Feb 2025 01:50:09 GMT  
		Size: 141.7 MB (141696883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed8b3fd82a250925f55b946f2bdd746a082ecd2970a4bf9a2418176501081e1`  
		Last Modified: Fri, 21 Feb 2025 00:28:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7ce34b821ae068e160f65aa3febf4c17101d2a9daf8a4b4e7a26208bb7d22`  
		Last Modified: Fri, 21 Feb 2025 00:28:13 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b523b9e65cb5720ce8ae73e538ef230e761b8f43cffd492d3639cb0e622d0ff`  
		Last Modified: Fri, 21 Feb 2025 00:28:03 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635515f670f0e003d2b90593b19485fe69078d7eb5b47b2aa4304f93edafae3`  
		Last Modified: Fri, 21 Feb 2025 00:28:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ea67607234d720e0dd13aadfa57cb3f7803ecc3a0a6062e3676e977603769`  
		Last Modified: Fri, 21 Feb 2025 00:28:05 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eae752361b103a1dc25497f73110e35700aa80da08967d88b3c09fff56c1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bcf5d320bb0d9db63bf594c65b311aa2e9516d59d323663096fcb3c613552e`

```dockerfile
```

-	Layers:
	-	`sha256:91f7615237ca92acd05b32c4c4d97429dbf495bfa5945c497eca59bd41e3131e`  
		Last Modified: Fri, 21 Feb 2025 01:49:53 GMT  
		Size: 25.9 KB (25890 bytes)  
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
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 01:50:10 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:31:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:31:13 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:31:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
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
		Last Modified: Fri, 21 Feb 2025 01:49:55 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.14-focal`

```console
$ docker pull clickhouse@sha256:69255ecc8de97843649e35089c68ff8eb61668f14754ec614c189a23717d632b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.14-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:fecaf7b88964f3d39aadf9dee40f4a18ff85406f349cac5a966dabd7ce28ee13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178872609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6374f8f3e1a7253bafa4eea700d16e2ebf691f0e614e028173fbb38e80fc1f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5517f3eb5548b7c503d1d73b118d8b8fe212ff5b2089ddccabf2a9735602cc8`  
		Last Modified: Fri, 21 Feb 2025 00:28:10 GMT  
		Size: 8.8 MB (8796697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291cb7d6e97379312fae3fe1ab1b7297dc1beb52d157f9fce22c4fc4cc837428`  
		Last Modified: Fri, 21 Feb 2025 01:50:09 GMT  
		Size: 141.7 MB (141696883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed8b3fd82a250925f55b946f2bdd746a082ecd2970a4bf9a2418176501081e1`  
		Last Modified: Fri, 21 Feb 2025 00:28:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7ce34b821ae068e160f65aa3febf4c17101d2a9daf8a4b4e7a26208bb7d22`  
		Last Modified: Fri, 21 Feb 2025 00:28:13 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b523b9e65cb5720ce8ae73e538ef230e761b8f43cffd492d3639cb0e622d0ff`  
		Last Modified: Fri, 21 Feb 2025 00:28:03 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635515f670f0e003d2b90593b19485fe69078d7eb5b47b2aa4304f93edafae3`  
		Last Modified: Fri, 21 Feb 2025 00:28:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ea67607234d720e0dd13aadfa57cb3f7803ecc3a0a6062e3676e977603769`  
		Last Modified: Fri, 21 Feb 2025 00:28:05 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eae752361b103a1dc25497f73110e35700aa80da08967d88b3c09fff56c1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bcf5d320bb0d9db63bf594c65b311aa2e9516d59d323663096fcb3c613552e`

```dockerfile
```

-	Layers:
	-	`sha256:91f7615237ca92acd05b32c4c4d97429dbf495bfa5945c497eca59bd41e3131e`  
		Last Modified: Fri, 21 Feb 2025 01:49:53 GMT  
		Size: 25.9 KB (25890 bytes)  
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
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 01:50:10 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:31:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:31:13 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:31:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
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
		Last Modified: Fri, 21 Feb 2025 01:49:55 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.14.39`

```console
$ docker pull clickhouse@sha256:69255ecc8de97843649e35089c68ff8eb61668f14754ec614c189a23717d632b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.14.39` - linux; amd64

```console
$ docker pull clickhouse@sha256:fecaf7b88964f3d39aadf9dee40f4a18ff85406f349cac5a966dabd7ce28ee13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178872609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6374f8f3e1a7253bafa4eea700d16e2ebf691f0e614e028173fbb38e80fc1f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5517f3eb5548b7c503d1d73b118d8b8fe212ff5b2089ddccabf2a9735602cc8`  
		Last Modified: Fri, 21 Feb 2025 00:28:10 GMT  
		Size: 8.8 MB (8796697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291cb7d6e97379312fae3fe1ab1b7297dc1beb52d157f9fce22c4fc4cc837428`  
		Last Modified: Fri, 21 Feb 2025 01:50:09 GMT  
		Size: 141.7 MB (141696883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed8b3fd82a250925f55b946f2bdd746a082ecd2970a4bf9a2418176501081e1`  
		Last Modified: Fri, 21 Feb 2025 00:28:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7ce34b821ae068e160f65aa3febf4c17101d2a9daf8a4b4e7a26208bb7d22`  
		Last Modified: Fri, 21 Feb 2025 00:28:13 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b523b9e65cb5720ce8ae73e538ef230e761b8f43cffd492d3639cb0e622d0ff`  
		Last Modified: Fri, 21 Feb 2025 00:28:03 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635515f670f0e003d2b90593b19485fe69078d7eb5b47b2aa4304f93edafae3`  
		Last Modified: Fri, 21 Feb 2025 00:28:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ea67607234d720e0dd13aadfa57cb3f7803ecc3a0a6062e3676e977603769`  
		Last Modified: Fri, 21 Feb 2025 00:28:05 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14.39` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eae752361b103a1dc25497f73110e35700aa80da08967d88b3c09fff56c1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bcf5d320bb0d9db63bf594c65b311aa2e9516d59d323663096fcb3c613552e`

```dockerfile
```

-	Layers:
	-	`sha256:91f7615237ca92acd05b32c4c4d97429dbf495bfa5945c497eca59bd41e3131e`  
		Last Modified: Fri, 21 Feb 2025 01:49:53 GMT  
		Size: 25.9 KB (25890 bytes)  
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
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 01:50:10 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:31:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:31:13 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:31:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
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
		Last Modified: Fri, 21 Feb 2025 01:49:55 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:24.8.14.39-focal`

```console
$ docker pull clickhouse@sha256:69255ecc8de97843649e35089c68ff8eb61668f14754ec614c189a23717d632b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:24.8.14.39-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:fecaf7b88964f3d39aadf9dee40f4a18ff85406f349cac5a966dabd7ce28ee13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178872609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6374f8f3e1a7253bafa4eea700d16e2ebf691f0e614e028173fbb38e80fc1f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5517f3eb5548b7c503d1d73b118d8b8fe212ff5b2089ddccabf2a9735602cc8`  
		Last Modified: Fri, 21 Feb 2025 00:28:10 GMT  
		Size: 8.8 MB (8796697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291cb7d6e97379312fae3fe1ab1b7297dc1beb52d157f9fce22c4fc4cc837428`  
		Last Modified: Fri, 21 Feb 2025 01:50:09 GMT  
		Size: 141.7 MB (141696883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed8b3fd82a250925f55b946f2bdd746a082ecd2970a4bf9a2418176501081e1`  
		Last Modified: Fri, 21 Feb 2025 00:28:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7ce34b821ae068e160f65aa3febf4c17101d2a9daf8a4b4e7a26208bb7d22`  
		Last Modified: Fri, 21 Feb 2025 00:28:13 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b523b9e65cb5720ce8ae73e538ef230e761b8f43cffd492d3639cb0e622d0ff`  
		Last Modified: Fri, 21 Feb 2025 00:28:03 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635515f670f0e003d2b90593b19485fe69078d7eb5b47b2aa4304f93edafae3`  
		Last Modified: Fri, 21 Feb 2025 00:28:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ea67607234d720e0dd13aadfa57cb3f7803ecc3a0a6062e3676e977603769`  
		Last Modified: Fri, 21 Feb 2025 00:28:05 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:24.8.14.39-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eae752361b103a1dc25497f73110e35700aa80da08967d88b3c09fff56c1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bcf5d320bb0d9db63bf594c65b311aa2e9516d59d323663096fcb3c613552e`

```dockerfile
```

-	Layers:
	-	`sha256:91f7615237ca92acd05b32c4c4d97429dbf495bfa5945c497eca59bd41e3131e`  
		Last Modified: Fri, 21 Feb 2025 01:49:53 GMT  
		Size: 25.9 KB (25890 bytes)  
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
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 01:50:10 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:31:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:31:13 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:31:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
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
		Last Modified: Fri, 21 Feb 2025 01:49:55 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1`

```console
$ docker pull clickhouse@sha256:6618b5cdf93e5a3a7d2baebf5759c6ba8460959af0945426db456a97054efc32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:dc0d025b1c629a71f2132ab0f451864f6f9dc2d89426813a720c785cc067f382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191063269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729d0a50d4622d07694e43055f21abff52bc972a5f5bbf9a71364e52e6835bfa`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=25.1.5.31
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611eb8fc1452bb5caf49a3fedef7e6c8d4c2b1cf5fb5ddea4cd5eac8bf62fce7`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 7.1 MB (7146926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5455fd9277bd671b3bfc9ed6a52f3faecd6fe313fd14d8dd741cfc6064ef252e`  
		Last Modified: Fri, 21 Feb 2025 01:50:23 GMT  
		Size: 153.5 MB (153510154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da4c20e68e45c9a2fdafd9d09b8810d34ecc0db6c0b3f0c081d0ab2cc5789df`  
		Last Modified: Fri, 21 Feb 2025 00:28:15 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2d5203ea1f6f8cad4fccfa6864a1e1853e0732c208e6acbf68333cc6d9dac4`  
		Last Modified: Fri, 21 Feb 2025 00:28:22 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8599b5287d9cf5ece644a985661386651f7d31c6aaa6d17ef14ac5c1bfa7d20`  
		Last Modified: Fri, 21 Feb 2025 00:28:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cbb8410d09337f5272492267bc0ebab74cd1b0ef22c08d51fbedf31105c204`  
		Last Modified: Fri, 21 Feb 2025 00:28:17 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a34072a4f26c8da787630f091670af80f2a523b58c92aae12312d52236813c8`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:664f507723aaf347f1eb635211f190dd08947906a42a363c782ae0eb51fa9c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac8819ef9fcfdc6e346a7bde2464cc1a32aee10c686986c79ca9a708edae278`

```dockerfile
```

-	Layers:
	-	`sha256:18c285e60898313b36e3debd1a7b5defeb20541d349c1c2c1ab66daa4a1e775a`  
		Last Modified: Fri, 21 Feb 2025 01:50:04 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7da4be1eecc4bb0488c55ed50cae8603657b76f0812d2f2ff09d1b3dfbffe977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181563657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1470aceae9ab975fc97bca0491a77e28b5ce57426a12eeb53fcdac9e4a4f002a`
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
ARG VERSION=25.1.5.31
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f17303849b5f6ef91a06db67ab5a688bc6e9e9758e8d7e21fbfb8b2b53bd3f0`  
		Last Modified: Fri, 21 Feb 2025 01:50:26 GMT  
		Size: 146.2 MB (146214108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5aa5203b3644850c67fc35c256e0536276676333aaaa289e794e000214284e2`  
		Last Modified: Fri, 21 Feb 2025 00:28:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931b66cf9c723e464d19e82be9d6196f1e44ca83c300f9e9ef70ebfcafe5d15f`  
		Last Modified: Fri, 21 Feb 2025 00:28:22 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4193b90ba1e907ecd904ecff18bf296bea7a431405e890d0c2386a5fe3a87c`  
		Last Modified: Fri, 21 Feb 2025 00:28:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e72b2c3c09db74cf74430b93c3e1eb28f3be37fb5852a134bfa80d7fed0f88`  
		Last Modified: Fri, 21 Feb 2025 00:28:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31776de2896bc0f20a8da32f0d3af8b97e58c784756d7841d4b4e4e6792ff0b`  
		Last Modified: Fri, 21 Feb 2025 00:28:16 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:23463a2ccac8ed93e84b83191b3cb8497b0a3a08525c17093a7555916ff13116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0089e9092a9db6205c66489ba4537a090d34c8f260e5810f264ec893175c7d9d`

```dockerfile
```

-	Layers:
	-	`sha256:b59c27d50bdde44451566a2250239b97eb017332815985bda56a7a456173d702`  
		Last Modified: Fri, 21 Feb 2025 01:50:05 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1-jammy`

```console
$ docker pull clickhouse@sha256:6618b5cdf93e5a3a7d2baebf5759c6ba8460959af0945426db456a97054efc32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:dc0d025b1c629a71f2132ab0f451864f6f9dc2d89426813a720c785cc067f382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191063269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729d0a50d4622d07694e43055f21abff52bc972a5f5bbf9a71364e52e6835bfa`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=25.1.5.31
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611eb8fc1452bb5caf49a3fedef7e6c8d4c2b1cf5fb5ddea4cd5eac8bf62fce7`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 7.1 MB (7146926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5455fd9277bd671b3bfc9ed6a52f3faecd6fe313fd14d8dd741cfc6064ef252e`  
		Last Modified: Fri, 21 Feb 2025 01:50:23 GMT  
		Size: 153.5 MB (153510154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da4c20e68e45c9a2fdafd9d09b8810d34ecc0db6c0b3f0c081d0ab2cc5789df`  
		Last Modified: Fri, 21 Feb 2025 00:28:15 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2d5203ea1f6f8cad4fccfa6864a1e1853e0732c208e6acbf68333cc6d9dac4`  
		Last Modified: Fri, 21 Feb 2025 00:28:22 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8599b5287d9cf5ece644a985661386651f7d31c6aaa6d17ef14ac5c1bfa7d20`  
		Last Modified: Fri, 21 Feb 2025 00:28:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cbb8410d09337f5272492267bc0ebab74cd1b0ef22c08d51fbedf31105c204`  
		Last Modified: Fri, 21 Feb 2025 00:28:17 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a34072a4f26c8da787630f091670af80f2a523b58c92aae12312d52236813c8`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:664f507723aaf347f1eb635211f190dd08947906a42a363c782ae0eb51fa9c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac8819ef9fcfdc6e346a7bde2464cc1a32aee10c686986c79ca9a708edae278`

```dockerfile
```

-	Layers:
	-	`sha256:18c285e60898313b36e3debd1a7b5defeb20541d349c1c2c1ab66daa4a1e775a`  
		Last Modified: Fri, 21 Feb 2025 01:50:04 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7da4be1eecc4bb0488c55ed50cae8603657b76f0812d2f2ff09d1b3dfbffe977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181563657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1470aceae9ab975fc97bca0491a77e28b5ce57426a12eeb53fcdac9e4a4f002a`
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
ARG VERSION=25.1.5.31
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f17303849b5f6ef91a06db67ab5a688bc6e9e9758e8d7e21fbfb8b2b53bd3f0`  
		Last Modified: Fri, 21 Feb 2025 01:50:26 GMT  
		Size: 146.2 MB (146214108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5aa5203b3644850c67fc35c256e0536276676333aaaa289e794e000214284e2`  
		Last Modified: Fri, 21 Feb 2025 00:28:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931b66cf9c723e464d19e82be9d6196f1e44ca83c300f9e9ef70ebfcafe5d15f`  
		Last Modified: Fri, 21 Feb 2025 00:28:22 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4193b90ba1e907ecd904ecff18bf296bea7a431405e890d0c2386a5fe3a87c`  
		Last Modified: Fri, 21 Feb 2025 00:28:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e72b2c3c09db74cf74430b93c3e1eb28f3be37fb5852a134bfa80d7fed0f88`  
		Last Modified: Fri, 21 Feb 2025 00:28:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31776de2896bc0f20a8da32f0d3af8b97e58c784756d7841d4b4e4e6792ff0b`  
		Last Modified: Fri, 21 Feb 2025 00:28:16 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:23463a2ccac8ed93e84b83191b3cb8497b0a3a08525c17093a7555916ff13116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0089e9092a9db6205c66489ba4537a090d34c8f260e5810f264ec893175c7d9d`

```dockerfile
```

-	Layers:
	-	`sha256:b59c27d50bdde44451566a2250239b97eb017332815985bda56a7a456173d702`  
		Last Modified: Fri, 21 Feb 2025 01:50:05 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1.5`

```console
$ docker pull clickhouse@sha256:6618b5cdf93e5a3a7d2baebf5759c6ba8460959af0945426db456a97054efc32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:dc0d025b1c629a71f2132ab0f451864f6f9dc2d89426813a720c785cc067f382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191063269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729d0a50d4622d07694e43055f21abff52bc972a5f5bbf9a71364e52e6835bfa`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=25.1.5.31
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611eb8fc1452bb5caf49a3fedef7e6c8d4c2b1cf5fb5ddea4cd5eac8bf62fce7`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 7.1 MB (7146926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5455fd9277bd671b3bfc9ed6a52f3faecd6fe313fd14d8dd741cfc6064ef252e`  
		Last Modified: Fri, 21 Feb 2025 01:50:23 GMT  
		Size: 153.5 MB (153510154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da4c20e68e45c9a2fdafd9d09b8810d34ecc0db6c0b3f0c081d0ab2cc5789df`  
		Last Modified: Fri, 21 Feb 2025 00:28:15 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2d5203ea1f6f8cad4fccfa6864a1e1853e0732c208e6acbf68333cc6d9dac4`  
		Last Modified: Fri, 21 Feb 2025 00:28:22 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8599b5287d9cf5ece644a985661386651f7d31c6aaa6d17ef14ac5c1bfa7d20`  
		Last Modified: Fri, 21 Feb 2025 00:28:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cbb8410d09337f5272492267bc0ebab74cd1b0ef22c08d51fbedf31105c204`  
		Last Modified: Fri, 21 Feb 2025 00:28:17 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a34072a4f26c8da787630f091670af80f2a523b58c92aae12312d52236813c8`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:664f507723aaf347f1eb635211f190dd08947906a42a363c782ae0eb51fa9c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac8819ef9fcfdc6e346a7bde2464cc1a32aee10c686986c79ca9a708edae278`

```dockerfile
```

-	Layers:
	-	`sha256:18c285e60898313b36e3debd1a7b5defeb20541d349c1c2c1ab66daa4a1e775a`  
		Last Modified: Fri, 21 Feb 2025 01:50:04 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7da4be1eecc4bb0488c55ed50cae8603657b76f0812d2f2ff09d1b3dfbffe977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181563657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1470aceae9ab975fc97bca0491a77e28b5ce57426a12eeb53fcdac9e4a4f002a`
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
ARG VERSION=25.1.5.31
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f17303849b5f6ef91a06db67ab5a688bc6e9e9758e8d7e21fbfb8b2b53bd3f0`  
		Last Modified: Fri, 21 Feb 2025 01:50:26 GMT  
		Size: 146.2 MB (146214108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5aa5203b3644850c67fc35c256e0536276676333aaaa289e794e000214284e2`  
		Last Modified: Fri, 21 Feb 2025 00:28:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931b66cf9c723e464d19e82be9d6196f1e44ca83c300f9e9ef70ebfcafe5d15f`  
		Last Modified: Fri, 21 Feb 2025 00:28:22 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4193b90ba1e907ecd904ecff18bf296bea7a431405e890d0c2386a5fe3a87c`  
		Last Modified: Fri, 21 Feb 2025 00:28:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e72b2c3c09db74cf74430b93c3e1eb28f3be37fb5852a134bfa80d7fed0f88`  
		Last Modified: Fri, 21 Feb 2025 00:28:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31776de2896bc0f20a8da32f0d3af8b97e58c784756d7841d4b4e4e6792ff0b`  
		Last Modified: Fri, 21 Feb 2025 00:28:16 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:23463a2ccac8ed93e84b83191b3cb8497b0a3a08525c17093a7555916ff13116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0089e9092a9db6205c66489ba4537a090d34c8f260e5810f264ec893175c7d9d`

```dockerfile
```

-	Layers:
	-	`sha256:b59c27d50bdde44451566a2250239b97eb017332815985bda56a7a456173d702`  
		Last Modified: Fri, 21 Feb 2025 01:50:05 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1.5-jammy`

```console
$ docker pull clickhouse@sha256:6618b5cdf93e5a3a7d2baebf5759c6ba8460959af0945426db456a97054efc32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:dc0d025b1c629a71f2132ab0f451864f6f9dc2d89426813a720c785cc067f382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191063269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729d0a50d4622d07694e43055f21abff52bc972a5f5bbf9a71364e52e6835bfa`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=25.1.5.31
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611eb8fc1452bb5caf49a3fedef7e6c8d4c2b1cf5fb5ddea4cd5eac8bf62fce7`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 7.1 MB (7146926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5455fd9277bd671b3bfc9ed6a52f3faecd6fe313fd14d8dd741cfc6064ef252e`  
		Last Modified: Fri, 21 Feb 2025 01:50:23 GMT  
		Size: 153.5 MB (153510154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da4c20e68e45c9a2fdafd9d09b8810d34ecc0db6c0b3f0c081d0ab2cc5789df`  
		Last Modified: Fri, 21 Feb 2025 00:28:15 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2d5203ea1f6f8cad4fccfa6864a1e1853e0732c208e6acbf68333cc6d9dac4`  
		Last Modified: Fri, 21 Feb 2025 00:28:22 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8599b5287d9cf5ece644a985661386651f7d31c6aaa6d17ef14ac5c1bfa7d20`  
		Last Modified: Fri, 21 Feb 2025 00:28:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cbb8410d09337f5272492267bc0ebab74cd1b0ef22c08d51fbedf31105c204`  
		Last Modified: Fri, 21 Feb 2025 00:28:17 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a34072a4f26c8da787630f091670af80f2a523b58c92aae12312d52236813c8`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:664f507723aaf347f1eb635211f190dd08947906a42a363c782ae0eb51fa9c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac8819ef9fcfdc6e346a7bde2464cc1a32aee10c686986c79ca9a708edae278`

```dockerfile
```

-	Layers:
	-	`sha256:18c285e60898313b36e3debd1a7b5defeb20541d349c1c2c1ab66daa4a1e775a`  
		Last Modified: Fri, 21 Feb 2025 01:50:04 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7da4be1eecc4bb0488c55ed50cae8603657b76f0812d2f2ff09d1b3dfbffe977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181563657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1470aceae9ab975fc97bca0491a77e28b5ce57426a12eeb53fcdac9e4a4f002a`
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
ARG VERSION=25.1.5.31
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f17303849b5f6ef91a06db67ab5a688bc6e9e9758e8d7e21fbfb8b2b53bd3f0`  
		Last Modified: Fri, 21 Feb 2025 01:50:26 GMT  
		Size: 146.2 MB (146214108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5aa5203b3644850c67fc35c256e0536276676333aaaa289e794e000214284e2`  
		Last Modified: Fri, 21 Feb 2025 00:28:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931b66cf9c723e464d19e82be9d6196f1e44ca83c300f9e9ef70ebfcafe5d15f`  
		Last Modified: Fri, 21 Feb 2025 00:28:22 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4193b90ba1e907ecd904ecff18bf296bea7a431405e890d0c2386a5fe3a87c`  
		Last Modified: Fri, 21 Feb 2025 00:28:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e72b2c3c09db74cf74430b93c3e1eb28f3be37fb5852a134bfa80d7fed0f88`  
		Last Modified: Fri, 21 Feb 2025 00:28:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31776de2896bc0f20a8da32f0d3af8b97e58c784756d7841d4b4e4e6792ff0b`  
		Last Modified: Fri, 21 Feb 2025 00:28:16 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:23463a2ccac8ed93e84b83191b3cb8497b0a3a08525c17093a7555916ff13116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0089e9092a9db6205c66489ba4537a090d34c8f260e5810f264ec893175c7d9d`

```dockerfile
```

-	Layers:
	-	`sha256:b59c27d50bdde44451566a2250239b97eb017332815985bda56a7a456173d702`  
		Last Modified: Fri, 21 Feb 2025 01:50:05 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1.5.31`

```console
$ docker pull clickhouse@sha256:6618b5cdf93e5a3a7d2baebf5759c6ba8460959af0945426db456a97054efc32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1.5.31` - linux; amd64

```console
$ docker pull clickhouse@sha256:dc0d025b1c629a71f2132ab0f451864f6f9dc2d89426813a720c785cc067f382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191063269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729d0a50d4622d07694e43055f21abff52bc972a5f5bbf9a71364e52e6835bfa`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=25.1.5.31
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611eb8fc1452bb5caf49a3fedef7e6c8d4c2b1cf5fb5ddea4cd5eac8bf62fce7`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 7.1 MB (7146926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5455fd9277bd671b3bfc9ed6a52f3faecd6fe313fd14d8dd741cfc6064ef252e`  
		Last Modified: Fri, 21 Feb 2025 01:50:23 GMT  
		Size: 153.5 MB (153510154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da4c20e68e45c9a2fdafd9d09b8810d34ecc0db6c0b3f0c081d0ab2cc5789df`  
		Last Modified: Fri, 21 Feb 2025 00:28:15 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2d5203ea1f6f8cad4fccfa6864a1e1853e0732c208e6acbf68333cc6d9dac4`  
		Last Modified: Fri, 21 Feb 2025 00:28:22 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8599b5287d9cf5ece644a985661386651f7d31c6aaa6d17ef14ac5c1bfa7d20`  
		Last Modified: Fri, 21 Feb 2025 00:28:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cbb8410d09337f5272492267bc0ebab74cd1b0ef22c08d51fbedf31105c204`  
		Last Modified: Fri, 21 Feb 2025 00:28:17 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a34072a4f26c8da787630f091670af80f2a523b58c92aae12312d52236813c8`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.5.31` - unknown; unknown

```console
$ docker pull clickhouse@sha256:664f507723aaf347f1eb635211f190dd08947906a42a363c782ae0eb51fa9c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac8819ef9fcfdc6e346a7bde2464cc1a32aee10c686986c79ca9a708edae278`

```dockerfile
```

-	Layers:
	-	`sha256:18c285e60898313b36e3debd1a7b5defeb20541d349c1c2c1ab66daa4a1e775a`  
		Last Modified: Fri, 21 Feb 2025 01:50:04 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1.5.31` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7da4be1eecc4bb0488c55ed50cae8603657b76f0812d2f2ff09d1b3dfbffe977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181563657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1470aceae9ab975fc97bca0491a77e28b5ce57426a12eeb53fcdac9e4a4f002a`
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
ARG VERSION=25.1.5.31
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f17303849b5f6ef91a06db67ab5a688bc6e9e9758e8d7e21fbfb8b2b53bd3f0`  
		Last Modified: Fri, 21 Feb 2025 01:50:26 GMT  
		Size: 146.2 MB (146214108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5aa5203b3644850c67fc35c256e0536276676333aaaa289e794e000214284e2`  
		Last Modified: Fri, 21 Feb 2025 00:28:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931b66cf9c723e464d19e82be9d6196f1e44ca83c300f9e9ef70ebfcafe5d15f`  
		Last Modified: Fri, 21 Feb 2025 00:28:22 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4193b90ba1e907ecd904ecff18bf296bea7a431405e890d0c2386a5fe3a87c`  
		Last Modified: Fri, 21 Feb 2025 00:28:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e72b2c3c09db74cf74430b93c3e1eb28f3be37fb5852a134bfa80d7fed0f88`  
		Last Modified: Fri, 21 Feb 2025 00:28:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31776de2896bc0f20a8da32f0d3af8b97e58c784756d7841d4b4e4e6792ff0b`  
		Last Modified: Fri, 21 Feb 2025 00:28:16 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.5.31` - unknown; unknown

```console
$ docker pull clickhouse@sha256:23463a2ccac8ed93e84b83191b3cb8497b0a3a08525c17093a7555916ff13116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0089e9092a9db6205c66489ba4537a090d34c8f260e5810f264ec893175c7d9d`

```dockerfile
```

-	Layers:
	-	`sha256:b59c27d50bdde44451566a2250239b97eb017332815985bda56a7a456173d702`  
		Last Modified: Fri, 21 Feb 2025 01:50:05 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.1.5.31-jammy`

```console
$ docker pull clickhouse@sha256:6618b5cdf93e5a3a7d2baebf5759c6ba8460959af0945426db456a97054efc32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.1.5.31-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:dc0d025b1c629a71f2132ab0f451864f6f9dc2d89426813a720c785cc067f382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191063269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729d0a50d4622d07694e43055f21abff52bc972a5f5bbf9a71364e52e6835bfa`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=25.1.5.31
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611eb8fc1452bb5caf49a3fedef7e6c8d4c2b1cf5fb5ddea4cd5eac8bf62fce7`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 7.1 MB (7146926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5455fd9277bd671b3bfc9ed6a52f3faecd6fe313fd14d8dd741cfc6064ef252e`  
		Last Modified: Fri, 21 Feb 2025 01:50:23 GMT  
		Size: 153.5 MB (153510154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da4c20e68e45c9a2fdafd9d09b8810d34ecc0db6c0b3f0c081d0ab2cc5789df`  
		Last Modified: Fri, 21 Feb 2025 00:28:15 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2d5203ea1f6f8cad4fccfa6864a1e1853e0732c208e6acbf68333cc6d9dac4`  
		Last Modified: Fri, 21 Feb 2025 00:28:22 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8599b5287d9cf5ece644a985661386651f7d31c6aaa6d17ef14ac5c1bfa7d20`  
		Last Modified: Fri, 21 Feb 2025 00:28:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cbb8410d09337f5272492267bc0ebab74cd1b0ef22c08d51fbedf31105c204`  
		Last Modified: Fri, 21 Feb 2025 00:28:17 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a34072a4f26c8da787630f091670af80f2a523b58c92aae12312d52236813c8`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.5.31-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:664f507723aaf347f1eb635211f190dd08947906a42a363c782ae0eb51fa9c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac8819ef9fcfdc6e346a7bde2464cc1a32aee10c686986c79ca9a708edae278`

```dockerfile
```

-	Layers:
	-	`sha256:18c285e60898313b36e3debd1a7b5defeb20541d349c1c2c1ab66daa4a1e775a`  
		Last Modified: Fri, 21 Feb 2025 01:50:04 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.1.5.31-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7da4be1eecc4bb0488c55ed50cae8603657b76f0812d2f2ff09d1b3dfbffe977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181563657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1470aceae9ab975fc97bca0491a77e28b5ce57426a12eeb53fcdac9e4a4f002a`
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
ARG VERSION=25.1.5.31
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f17303849b5f6ef91a06db67ab5a688bc6e9e9758e8d7e21fbfb8b2b53bd3f0`  
		Last Modified: Fri, 21 Feb 2025 01:50:26 GMT  
		Size: 146.2 MB (146214108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5aa5203b3644850c67fc35c256e0536276676333aaaa289e794e000214284e2`  
		Last Modified: Fri, 21 Feb 2025 00:28:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931b66cf9c723e464d19e82be9d6196f1e44ca83c300f9e9ef70ebfcafe5d15f`  
		Last Modified: Fri, 21 Feb 2025 00:28:22 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4193b90ba1e907ecd904ecff18bf296bea7a431405e890d0c2386a5fe3a87c`  
		Last Modified: Fri, 21 Feb 2025 00:28:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e72b2c3c09db74cf74430b93c3e1eb28f3be37fb5852a134bfa80d7fed0f88`  
		Last Modified: Fri, 21 Feb 2025 00:28:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31776de2896bc0f20a8da32f0d3af8b97e58c784756d7841d4b4e4e6792ff0b`  
		Last Modified: Fri, 21 Feb 2025 00:28:16 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.1.5.31-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:23463a2ccac8ed93e84b83191b3cb8497b0a3a08525c17093a7555916ff13116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0089e9092a9db6205c66489ba4537a090d34c8f260e5810f264ec893175c7d9d`

```dockerfile
```

-	Layers:
	-	`sha256:b59c27d50bdde44451566a2250239b97eb017332815985bda56a7a456173d702`  
		Last Modified: Fri, 21 Feb 2025 01:50:05 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:6618b5cdf93e5a3a7d2baebf5759c6ba8460959af0945426db456a97054efc32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:dc0d025b1c629a71f2132ab0f451864f6f9dc2d89426813a720c785cc067f382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191063269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729d0a50d4622d07694e43055f21abff52bc972a5f5bbf9a71364e52e6835bfa`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=25.1.5.31
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611eb8fc1452bb5caf49a3fedef7e6c8d4c2b1cf5fb5ddea4cd5eac8bf62fce7`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 7.1 MB (7146926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5455fd9277bd671b3bfc9ed6a52f3faecd6fe313fd14d8dd741cfc6064ef252e`  
		Last Modified: Fri, 21 Feb 2025 01:50:23 GMT  
		Size: 153.5 MB (153510154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da4c20e68e45c9a2fdafd9d09b8810d34ecc0db6c0b3f0c081d0ab2cc5789df`  
		Last Modified: Fri, 21 Feb 2025 00:28:15 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2d5203ea1f6f8cad4fccfa6864a1e1853e0732c208e6acbf68333cc6d9dac4`  
		Last Modified: Fri, 21 Feb 2025 00:28:22 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8599b5287d9cf5ece644a985661386651f7d31c6aaa6d17ef14ac5c1bfa7d20`  
		Last Modified: Fri, 21 Feb 2025 00:28:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cbb8410d09337f5272492267bc0ebab74cd1b0ef22c08d51fbedf31105c204`  
		Last Modified: Fri, 21 Feb 2025 00:28:17 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a34072a4f26c8da787630f091670af80f2a523b58c92aae12312d52236813c8`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:664f507723aaf347f1eb635211f190dd08947906a42a363c782ae0eb51fa9c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac8819ef9fcfdc6e346a7bde2464cc1a32aee10c686986c79ca9a708edae278`

```dockerfile
```

-	Layers:
	-	`sha256:18c285e60898313b36e3debd1a7b5defeb20541d349c1c2c1ab66daa4a1e775a`  
		Last Modified: Fri, 21 Feb 2025 01:50:04 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7da4be1eecc4bb0488c55ed50cae8603657b76f0812d2f2ff09d1b3dfbffe977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181563657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1470aceae9ab975fc97bca0491a77e28b5ce57426a12eeb53fcdac9e4a4f002a`
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
ARG VERSION=25.1.5.31
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f17303849b5f6ef91a06db67ab5a688bc6e9e9758e8d7e21fbfb8b2b53bd3f0`  
		Last Modified: Fri, 21 Feb 2025 01:50:26 GMT  
		Size: 146.2 MB (146214108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5aa5203b3644850c67fc35c256e0536276676333aaaa289e794e000214284e2`  
		Last Modified: Fri, 21 Feb 2025 00:28:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931b66cf9c723e464d19e82be9d6196f1e44ca83c300f9e9ef70ebfcafe5d15f`  
		Last Modified: Fri, 21 Feb 2025 00:28:22 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4193b90ba1e907ecd904ecff18bf296bea7a431405e890d0c2386a5fe3a87c`  
		Last Modified: Fri, 21 Feb 2025 00:28:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e72b2c3c09db74cf74430b93c3e1eb28f3be37fb5852a134bfa80d7fed0f88`  
		Last Modified: Fri, 21 Feb 2025 00:28:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31776de2896bc0f20a8da32f0d3af8b97e58c784756d7841d4b4e4e6792ff0b`  
		Last Modified: Fri, 21 Feb 2025 00:28:16 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:23463a2ccac8ed93e84b83191b3cb8497b0a3a08525c17093a7555916ff13116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0089e9092a9db6205c66489ba4537a090d34c8f260e5810f264ec893175c7d9d`

```dockerfile
```

-	Layers:
	-	`sha256:b59c27d50bdde44451566a2250239b97eb017332815985bda56a7a456173d702`  
		Last Modified: Fri, 21 Feb 2025 01:50:05 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:6618b5cdf93e5a3a7d2baebf5759c6ba8460959af0945426db456a97054efc32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:dc0d025b1c629a71f2132ab0f451864f6f9dc2d89426813a720c785cc067f382
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.1 MB (191063269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729d0a50d4622d07694e43055f21abff52bc972a5f5bbf9a71364e52e6835bfa`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sun, 26 Jan 2025 05:31:07 GMT
ARG RELEASE
# Sun, 26 Jan 2025 05:31:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 26 Jan 2025 05:31:07 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 26 Jan 2025 05:31:10 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Sun, 26 Jan 2025 05:31:11 GMT
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
ARG VERSION=25.1.5.31
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611eb8fc1452bb5caf49a3fedef7e6c8d4c2b1cf5fb5ddea4cd5eac8bf62fce7`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 7.1 MB (7146926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5455fd9277bd671b3bfc9ed6a52f3faecd6fe313fd14d8dd741cfc6064ef252e`  
		Last Modified: Fri, 21 Feb 2025 01:50:23 GMT  
		Size: 153.5 MB (153510154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da4c20e68e45c9a2fdafd9d09b8810d34ecc0db6c0b3f0c081d0ab2cc5789df`  
		Last Modified: Fri, 21 Feb 2025 00:28:15 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa2d5203ea1f6f8cad4fccfa6864a1e1853e0732c208e6acbf68333cc6d9dac4`  
		Last Modified: Fri, 21 Feb 2025 00:28:22 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8599b5287d9cf5ece644a985661386651f7d31c6aaa6d17ef14ac5c1bfa7d20`  
		Last Modified: Fri, 21 Feb 2025 00:28:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cbb8410d09337f5272492267bc0ebab74cd1b0ef22c08d51fbedf31105c204`  
		Last Modified: Fri, 21 Feb 2025 00:28:17 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a34072a4f26c8da787630f091670af80f2a523b58c92aae12312d52236813c8`  
		Last Modified: Fri, 21 Feb 2025 00:28:18 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:664f507723aaf347f1eb635211f190dd08947906a42a363c782ae0eb51fa9c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac8819ef9fcfdc6e346a7bde2464cc1a32aee10c686986c79ca9a708edae278`

```dockerfile
```

-	Layers:
	-	`sha256:18c285e60898313b36e3debd1a7b5defeb20541d349c1c2c1ab66daa4a1e775a`  
		Last Modified: Fri, 21 Feb 2025 01:50:04 GMT  
		Size: 25.9 KB (25873 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7da4be1eecc4bb0488c55ed50cae8603657b76f0812d2f2ff09d1b3dfbffe977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.6 MB (181563657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1470aceae9ab975fc97bca0491a77e28b5ce57426a12eeb53fcdac9e4a4f002a`
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
ARG VERSION=25.1.5.31
# Thu, 20 Feb 2025 13:03:00 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 20 Feb 2025 13:03:00 GMT
ENV LANG=en_US.UTF-8
# Thu, 20 Feb 2025 13:03:00 GMT
ENV TZ=UTC
# Thu, 20 Feb 2025 13:03:00 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.1.5.31 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
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
	-	`sha256:0d1c17d4e593cf07e0f9e907017f6edbe7e32dd2b7f8e3f026c74bbaf3466561`  
		Last Modified: Tue, 04 Feb 2025 06:04:46 GMT  
		Size: 27.4 MB (27358182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac97404a5b766497f96574f380686c48e39cf3536849c8ce090307d7b3137d1b`  
		Last Modified: Fri, 21 Feb 2025 00:28:29 GMT  
		Size: 7.1 MB (7121114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f17303849b5f6ef91a06db67ab5a688bc6e9e9758e8d7e21fbfb8b2b53bd3f0`  
		Last Modified: Fri, 21 Feb 2025 01:50:26 GMT  
		Size: 146.2 MB (146214108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5aa5203b3644850c67fc35c256e0536276676333aaaa289e794e000214284e2`  
		Last Modified: Fri, 21 Feb 2025 00:28:21 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931b66cf9c723e464d19e82be9d6196f1e44ca83c300f9e9ef70ebfcafe5d15f`  
		Last Modified: Fri, 21 Feb 2025 00:28:22 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4193b90ba1e907ecd904ecff18bf296bea7a431405e890d0c2386a5fe3a87c`  
		Last Modified: Fri, 21 Feb 2025 00:28:21 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e72b2c3c09db74cf74430b93c3e1eb28f3be37fb5852a134bfa80d7fed0f88`  
		Last Modified: Fri, 21 Feb 2025 00:28:15 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31776de2896bc0f20a8da32f0d3af8b97e58c784756d7841d4b4e4e6792ff0b`  
		Last Modified: Fri, 21 Feb 2025 00:28:16 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:23463a2ccac8ed93e84b83191b3cb8497b0a3a08525c17093a7555916ff13116
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 KB (26084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0089e9092a9db6205c66489ba4537a090d34c8f260e5810f264ec893175c7d9d`

```dockerfile
```

-	Layers:
	-	`sha256:b59c27d50bdde44451566a2250239b97eb017332815985bda56a7a456173d702`  
		Last Modified: Fri, 21 Feb 2025 01:50:05 GMT  
		Size: 26.1 KB (26084 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:69255ecc8de97843649e35089c68ff8eb61668f14754ec614c189a23717d632b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:fecaf7b88964f3d39aadf9dee40f4a18ff85406f349cac5a966dabd7ce28ee13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178872609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6374f8f3e1a7253bafa4eea700d16e2ebf691f0e614e028173fbb38e80fc1f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5517f3eb5548b7c503d1d73b118d8b8fe212ff5b2089ddccabf2a9735602cc8`  
		Last Modified: Fri, 21 Feb 2025 00:28:10 GMT  
		Size: 8.8 MB (8796697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291cb7d6e97379312fae3fe1ab1b7297dc1beb52d157f9fce22c4fc4cc837428`  
		Last Modified: Fri, 21 Feb 2025 01:50:09 GMT  
		Size: 141.7 MB (141696883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed8b3fd82a250925f55b946f2bdd746a082ecd2970a4bf9a2418176501081e1`  
		Last Modified: Fri, 21 Feb 2025 00:28:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7ce34b821ae068e160f65aa3febf4c17101d2a9daf8a4b4e7a26208bb7d22`  
		Last Modified: Fri, 21 Feb 2025 00:28:13 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b523b9e65cb5720ce8ae73e538ef230e761b8f43cffd492d3639cb0e622d0ff`  
		Last Modified: Fri, 21 Feb 2025 00:28:03 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635515f670f0e003d2b90593b19485fe69078d7eb5b47b2aa4304f93edafae3`  
		Last Modified: Fri, 21 Feb 2025 00:28:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ea67607234d720e0dd13aadfa57cb3f7803ecc3a0a6062e3676e977603769`  
		Last Modified: Fri, 21 Feb 2025 00:28:05 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eae752361b103a1dc25497f73110e35700aa80da08967d88b3c09fff56c1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bcf5d320bb0d9db63bf594c65b311aa2e9516d59d323663096fcb3c613552e`

```dockerfile
```

-	Layers:
	-	`sha256:91f7615237ca92acd05b32c4c4d97429dbf495bfa5945c497eca59bd41e3131e`  
		Last Modified: Fri, 21 Feb 2025 01:49:53 GMT  
		Size: 25.9 KB (25890 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

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
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 01:50:10 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:31:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:31:13 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:31:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

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
		Last Modified: Fri, 21 Feb 2025 01:49:55 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-focal`

```console
$ docker pull clickhouse@sha256:69255ecc8de97843649e35089c68ff8eb61668f14754ec614c189a23717d632b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-focal` - linux; amd64

```console
$ docker pull clickhouse@sha256:fecaf7b88964f3d39aadf9dee40f4a18ff85406f349cac5a966dabd7ce28ee13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.9 MB (178872609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6374f8f3e1a7253bafa4eea700d16e2ebf691f0e614e028173fbb38e80fc1f0`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 11 Oct 2024 03:38:25 GMT
ARG RELEASE
# Fri, 11 Oct 2024 03:38:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Oct 2024 03:38:25 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 11 Oct 2024 03:38:27 GMT
ADD file:7486147a645d8835a5181c79f00a3606c6b714c83bcbfcd8862221eb14690f9e in / 
# Fri, 11 Oct 2024 03:38:27 GMT
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
	-	`sha256:d9802f032d6798e2086607424bfe88cb8ec1d6f116e11cd99592dcaf261e9cd2`  
		Last Modified: Fri, 13 Dec 2024 13:08:34 GMT  
		Size: 27.5 MB (27511060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5517f3eb5548b7c503d1d73b118d8b8fe212ff5b2089ddccabf2a9735602cc8`  
		Last Modified: Fri, 21 Feb 2025 00:28:10 GMT  
		Size: 8.8 MB (8796697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291cb7d6e97379312fae3fe1ab1b7297dc1beb52d157f9fce22c4fc4cc837428`  
		Last Modified: Fri, 21 Feb 2025 01:50:09 GMT  
		Size: 141.7 MB (141696883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed8b3fd82a250925f55b946f2bdd746a082ecd2970a4bf9a2418176501081e1`  
		Last Modified: Fri, 21 Feb 2025 00:28:08 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ced7ce34b821ae068e160f65aa3febf4c17101d2a9daf8a4b4e7a26208bb7d22`  
		Last Modified: Fri, 21 Feb 2025 00:28:13 GMT  
		Size: 863.5 KB (863476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b523b9e65cb5720ce8ae73e538ef230e761b8f43cffd492d3639cb0e622d0ff`  
		Last Modified: Fri, 21 Feb 2025 00:28:03 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6635515f670f0e003d2b90593b19485fe69078d7eb5b47b2aa4304f93edafae3`  
		Last Modified: Fri, 21 Feb 2025 00:28:05 GMT  
		Size: 360.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487ea67607234d720e0dd13aadfa57cb3f7803ecc3a0a6062e3676e977603769`  
		Last Modified: Fri, 21 Feb 2025 00:28:05 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-focal` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6eae752361b103a1dc25497f73110e35700aa80da08967d88b3c09fff56c1920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bcf5d320bb0d9db63bf594c65b311aa2e9516d59d323663096fcb3c613552e`

```dockerfile
```

-	Layers:
	-	`sha256:91f7615237ca92acd05b32c4c4d97429dbf495bfa5945c497eca59bd41e3131e`  
		Last Modified: Fri, 21 Feb 2025 01:49:53 GMT  
		Size: 25.9 KB (25890 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-focal` - linux; arm64 variant v8

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
		Last Modified: Fri, 13 Dec 2024 13:25:16 GMT  
		Size: 26.0 MB (25973828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c01fcf3ee97465322372ef2b740317197df0efca5a2e2ae77dab692a26dd5`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 8.7 MB (8655025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6814ac006b516e90a922fa50af52115e3ee787580e656c69d5a7f4995c5a76f7`  
		Last Modified: Fri, 21 Feb 2025 01:50:10 GMT  
		Size: 136.8 MB (136750575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5deb15cedd8e25720e3dcc7124459f6401e9f3c2825532055f014943c9ea8f`  
		Last Modified: Fri, 21 Feb 2025 00:31:07 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce857883714fb1f56b78cd8bee76c9e932502d2d35c19a43a14fad71c4caadf6`  
		Last Modified: Fri, 21 Feb 2025 00:31:13 GMT  
		Size: 863.5 KB (863473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785ee37a6fe5bddab5ff5da289ce99b378d62ab5eac1fb5035802273e8edf50a`  
		Last Modified: Fri, 21 Feb 2025 00:31:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f108fe3884ee172ac6a7b64da00d2918b3077c0adedcca289e93311d81c4dd`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e98405840413a72b6c4d114c9dbf7af32ab71cd543be62a9af6bad54f9066cd9`  
		Last Modified: Fri, 21 Feb 2025 00:31:09 GMT  
		Size: 3.8 KB (3837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-focal` - unknown; unknown

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
		Last Modified: Fri, 21 Feb 2025 01:49:55 GMT  
		Size: 26.1 KB (26101 bytes)  
		MIME: application/vnd.in-toto+json
