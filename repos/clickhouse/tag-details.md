<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.6`](#clickhouse2536)
-	[`clickhouse:25.3.6-jammy`](#clickhouse2536-jammy)
-	[`clickhouse:25.3.6.56`](#clickhouse253656)
-	[`clickhouse:25.3.6.56-jammy`](#clickhouse253656-jammy)
-	[`clickhouse:25.6`](#clickhouse256)
-	[`clickhouse:25.6-jammy`](#clickhouse256-jammy)
-	[`clickhouse:25.6.12`](#clickhouse25612)
-	[`clickhouse:25.6.12-jammy`](#clickhouse25612-jammy)
-	[`clickhouse:25.6.12.10`](#clickhouse2561210)
-	[`clickhouse:25.6.12.10-jammy`](#clickhouse2561210-jammy)
-	[`clickhouse:25.7`](#clickhouse257)
-	[`clickhouse:25.7-jammy`](#clickhouse257-jammy)
-	[`clickhouse:25.7.7`](#clickhouse2577)
-	[`clickhouse:25.7.7-jammy`](#clickhouse2577-jammy)
-	[`clickhouse:25.7.7.68`](#clickhouse257768)
-	[`clickhouse:25.7.7.68-jammy`](#clickhouse257768-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.7`](#clickhouse2587)
-	[`clickhouse:25.8.7-jammy`](#clickhouse2587-jammy)
-	[`clickhouse:25.8.7.3`](#clickhouse25873)
-	[`clickhouse:25.8.7.3-jammy`](#clickhouse25873-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:5775d1b0250370902ea04bf37d37583d8db744761aa81223ce648196f3bbc369
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:79c0f0ba61b5a5f7284a10e9f671ccfeab8e445cca58929d14d9b5c30de86d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db22b7ed486ee977ad64ddca75012fb3118be31681443b2941bb0c0809c3fb5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.3.6.56
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b8b64bfc3c006da3dbdc8315726047223dc83bf809ec568a01a6282bb7c6d`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3063f406083ccf1f853493cc1903b17828299758cc838c0ae3ff5a1ab038e53a`  
		Last Modified: Tue, 02 Sep 2025 00:49:44 GMT  
		Size: 167.9 MB (167873557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068524848a39bc20273deb9c815010922e604f57cae4d762fe4a110be010b7cc`  
		Last Modified: Mon, 01 Sep 2025 23:09:01 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbfcd3b5b7985fa5315ff6a50d0e8302ff1ef18dc6ebe4087c197fd26b8483`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce48062e0dad3ffc672b574bd49b5254c21bc836e2cd928d35697d45107fa99`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239040b253b9101ca6a52d9fdf17f703d4d539ea63f832e9295ac84a2eeecb0`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ef3f7692f6964082a0ebad321915d0eab0f8f6e4c8c320b008376823e6fd63`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50a83551816610e25f1c81d2c2b78c69e6ab1bffca8651469526761dce29669a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759649216f9edd7c53fc693d5297c37eb1089638406f26eb7694ea6961951a21`

```dockerfile
```

-	Layers:
	-	`sha256:c307d95fe108fe4572dfab6fbe5f75fa0d6ac491733f5cb90e7aaaab019461b2`  
		Last Modified: Tue, 02 Sep 2025 00:49:19 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e84618e2358bd900c2570a689c36b2616724390957829645328363d01f73b68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192935452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49c271763f7ebf803294a10c094a4c86f81880afc11f606e54012e89e2c71ee`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121c7ad3ac83b048884c02adca98157abf994fbb1d74705e59750f5995867c55`  
		Last Modified: Thu, 02 Oct 2025 03:49:28 GMT  
		Size: 7.1 MB (7127188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb81e8ce1c0e3bf764f862fa23dffef8b1771e96ddf366e04d8ed686e171d3ca`  
		Last Modified: Thu, 02 Oct 2025 03:49:38 GMT  
		Size: 157.6 MB (157554913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7a2398c1a8a3864d86081e87c48b95784089b1a3333ce835fbb2732f05256c`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d36473197c8e3f1fb7591d0e070152bb411e8a08823f3b5741de1d41b3d556`  
		Last Modified: Thu, 02 Oct 2025 01:54:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5b841c9bd049a592566d3d82f67bc63c24fcb26517737c19c47439096587f8`  
		Last Modified: Thu, 02 Oct 2025 01:54:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a8344b3fa142ebf1cec3a97c905b3ce9c76af46368c88cbb4011287a0cdfd7`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed403f5f13fcdb3851b9a45a3ca11d06ede3aa1ae3c9343c2c6947c7286069`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b408decd5cd308f231858854ce60a464f8dd9bcd988ab560b792cf2a54127cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc6173b2bbb09f0d3858408badb7b9ce14ac911992f16645bb321c7d3427c5c`

```dockerfile
```

-	Layers:
	-	`sha256:161974e701e67229efe4ca238bfa8c9e01cd184158efaf956c6ddc1901452e5a`  
		Last Modified: Thu, 02 Oct 2025 03:49:20 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:5775d1b0250370902ea04bf37d37583d8db744761aa81223ce648196f3bbc369
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:79c0f0ba61b5a5f7284a10e9f671ccfeab8e445cca58929d14d9b5c30de86d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db22b7ed486ee977ad64ddca75012fb3118be31681443b2941bb0c0809c3fb5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.3.6.56
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b8b64bfc3c006da3dbdc8315726047223dc83bf809ec568a01a6282bb7c6d`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3063f406083ccf1f853493cc1903b17828299758cc838c0ae3ff5a1ab038e53a`  
		Last Modified: Tue, 02 Sep 2025 00:49:44 GMT  
		Size: 167.9 MB (167873557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068524848a39bc20273deb9c815010922e604f57cae4d762fe4a110be010b7cc`  
		Last Modified: Mon, 01 Sep 2025 23:09:01 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbfcd3b5b7985fa5315ff6a50d0e8302ff1ef18dc6ebe4087c197fd26b8483`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce48062e0dad3ffc672b574bd49b5254c21bc836e2cd928d35697d45107fa99`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239040b253b9101ca6a52d9fdf17f703d4d539ea63f832e9295ac84a2eeecb0`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ef3f7692f6964082a0ebad321915d0eab0f8f6e4c8c320b008376823e6fd63`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50a83551816610e25f1c81d2c2b78c69e6ab1bffca8651469526761dce29669a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759649216f9edd7c53fc693d5297c37eb1089638406f26eb7694ea6961951a21`

```dockerfile
```

-	Layers:
	-	`sha256:c307d95fe108fe4572dfab6fbe5f75fa0d6ac491733f5cb90e7aaaab019461b2`  
		Last Modified: Tue, 02 Sep 2025 00:49:19 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e84618e2358bd900c2570a689c36b2616724390957829645328363d01f73b68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192935452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49c271763f7ebf803294a10c094a4c86f81880afc11f606e54012e89e2c71ee`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121c7ad3ac83b048884c02adca98157abf994fbb1d74705e59750f5995867c55`  
		Last Modified: Thu, 02 Oct 2025 03:49:28 GMT  
		Size: 7.1 MB (7127188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb81e8ce1c0e3bf764f862fa23dffef8b1771e96ddf366e04d8ed686e171d3ca`  
		Last Modified: Thu, 02 Oct 2025 03:49:38 GMT  
		Size: 157.6 MB (157554913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7a2398c1a8a3864d86081e87c48b95784089b1a3333ce835fbb2732f05256c`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d36473197c8e3f1fb7591d0e070152bb411e8a08823f3b5741de1d41b3d556`  
		Last Modified: Thu, 02 Oct 2025 01:54:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5b841c9bd049a592566d3d82f67bc63c24fcb26517737c19c47439096587f8`  
		Last Modified: Thu, 02 Oct 2025 01:54:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a8344b3fa142ebf1cec3a97c905b3ce9c76af46368c88cbb4011287a0cdfd7`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed403f5f13fcdb3851b9a45a3ca11d06ede3aa1ae3c9343c2c6947c7286069`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b408decd5cd308f231858854ce60a464f8dd9bcd988ab560b792cf2a54127cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc6173b2bbb09f0d3858408badb7b9ce14ac911992f16645bb321c7d3427c5c`

```dockerfile
```

-	Layers:
	-	`sha256:161974e701e67229efe4ca238bfa8c9e01cd184158efaf956c6ddc1901452e5a`  
		Last Modified: Thu, 02 Oct 2025 03:49:20 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.6`

```console
$ docker pull clickhouse@sha256:5775d1b0250370902ea04bf37d37583d8db744761aa81223ce648196f3bbc369
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:79c0f0ba61b5a5f7284a10e9f671ccfeab8e445cca58929d14d9b5c30de86d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db22b7ed486ee977ad64ddca75012fb3118be31681443b2941bb0c0809c3fb5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.3.6.56
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b8b64bfc3c006da3dbdc8315726047223dc83bf809ec568a01a6282bb7c6d`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3063f406083ccf1f853493cc1903b17828299758cc838c0ae3ff5a1ab038e53a`  
		Last Modified: Tue, 02 Sep 2025 00:49:44 GMT  
		Size: 167.9 MB (167873557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068524848a39bc20273deb9c815010922e604f57cae4d762fe4a110be010b7cc`  
		Last Modified: Mon, 01 Sep 2025 23:09:01 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbfcd3b5b7985fa5315ff6a50d0e8302ff1ef18dc6ebe4087c197fd26b8483`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce48062e0dad3ffc672b574bd49b5254c21bc836e2cd928d35697d45107fa99`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239040b253b9101ca6a52d9fdf17f703d4d539ea63f832e9295ac84a2eeecb0`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ef3f7692f6964082a0ebad321915d0eab0f8f6e4c8c320b008376823e6fd63`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50a83551816610e25f1c81d2c2b78c69e6ab1bffca8651469526761dce29669a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759649216f9edd7c53fc693d5297c37eb1089638406f26eb7694ea6961951a21`

```dockerfile
```

-	Layers:
	-	`sha256:c307d95fe108fe4572dfab6fbe5f75fa0d6ac491733f5cb90e7aaaab019461b2`  
		Last Modified: Tue, 02 Sep 2025 00:49:19 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e84618e2358bd900c2570a689c36b2616724390957829645328363d01f73b68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192935452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49c271763f7ebf803294a10c094a4c86f81880afc11f606e54012e89e2c71ee`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121c7ad3ac83b048884c02adca98157abf994fbb1d74705e59750f5995867c55`  
		Last Modified: Thu, 02 Oct 2025 03:49:28 GMT  
		Size: 7.1 MB (7127188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb81e8ce1c0e3bf764f862fa23dffef8b1771e96ddf366e04d8ed686e171d3ca`  
		Last Modified: Thu, 02 Oct 2025 03:49:38 GMT  
		Size: 157.6 MB (157554913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7a2398c1a8a3864d86081e87c48b95784089b1a3333ce835fbb2732f05256c`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d36473197c8e3f1fb7591d0e070152bb411e8a08823f3b5741de1d41b3d556`  
		Last Modified: Thu, 02 Oct 2025 01:54:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5b841c9bd049a592566d3d82f67bc63c24fcb26517737c19c47439096587f8`  
		Last Modified: Thu, 02 Oct 2025 01:54:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a8344b3fa142ebf1cec3a97c905b3ce9c76af46368c88cbb4011287a0cdfd7`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed403f5f13fcdb3851b9a45a3ca11d06ede3aa1ae3c9343c2c6947c7286069`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b408decd5cd308f231858854ce60a464f8dd9bcd988ab560b792cf2a54127cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc6173b2bbb09f0d3858408badb7b9ce14ac911992f16645bb321c7d3427c5c`

```dockerfile
```

-	Layers:
	-	`sha256:161974e701e67229efe4ca238bfa8c9e01cd184158efaf956c6ddc1901452e5a`  
		Last Modified: Thu, 02 Oct 2025 03:49:20 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.6-jammy`

```console
$ docker pull clickhouse@sha256:5775d1b0250370902ea04bf37d37583d8db744761aa81223ce648196f3bbc369
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:79c0f0ba61b5a5f7284a10e9f671ccfeab8e445cca58929d14d9b5c30de86d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db22b7ed486ee977ad64ddca75012fb3118be31681443b2941bb0c0809c3fb5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.3.6.56
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b8b64bfc3c006da3dbdc8315726047223dc83bf809ec568a01a6282bb7c6d`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3063f406083ccf1f853493cc1903b17828299758cc838c0ae3ff5a1ab038e53a`  
		Last Modified: Tue, 02 Sep 2025 00:49:44 GMT  
		Size: 167.9 MB (167873557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068524848a39bc20273deb9c815010922e604f57cae4d762fe4a110be010b7cc`  
		Last Modified: Mon, 01 Sep 2025 23:09:01 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbfcd3b5b7985fa5315ff6a50d0e8302ff1ef18dc6ebe4087c197fd26b8483`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce48062e0dad3ffc672b574bd49b5254c21bc836e2cd928d35697d45107fa99`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239040b253b9101ca6a52d9fdf17f703d4d539ea63f832e9295ac84a2eeecb0`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ef3f7692f6964082a0ebad321915d0eab0f8f6e4c8c320b008376823e6fd63`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50a83551816610e25f1c81d2c2b78c69e6ab1bffca8651469526761dce29669a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759649216f9edd7c53fc693d5297c37eb1089638406f26eb7694ea6961951a21`

```dockerfile
```

-	Layers:
	-	`sha256:c307d95fe108fe4572dfab6fbe5f75fa0d6ac491733f5cb90e7aaaab019461b2`  
		Last Modified: Tue, 02 Sep 2025 00:49:19 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e84618e2358bd900c2570a689c36b2616724390957829645328363d01f73b68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192935452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49c271763f7ebf803294a10c094a4c86f81880afc11f606e54012e89e2c71ee`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121c7ad3ac83b048884c02adca98157abf994fbb1d74705e59750f5995867c55`  
		Last Modified: Thu, 02 Oct 2025 03:49:28 GMT  
		Size: 7.1 MB (7127188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb81e8ce1c0e3bf764f862fa23dffef8b1771e96ddf366e04d8ed686e171d3ca`  
		Last Modified: Thu, 02 Oct 2025 03:49:38 GMT  
		Size: 157.6 MB (157554913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7a2398c1a8a3864d86081e87c48b95784089b1a3333ce835fbb2732f05256c`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d36473197c8e3f1fb7591d0e070152bb411e8a08823f3b5741de1d41b3d556`  
		Last Modified: Thu, 02 Oct 2025 01:54:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5b841c9bd049a592566d3d82f67bc63c24fcb26517737c19c47439096587f8`  
		Last Modified: Thu, 02 Oct 2025 01:54:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a8344b3fa142ebf1cec3a97c905b3ce9c76af46368c88cbb4011287a0cdfd7`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed403f5f13fcdb3851b9a45a3ca11d06ede3aa1ae3c9343c2c6947c7286069`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b408decd5cd308f231858854ce60a464f8dd9bcd988ab560b792cf2a54127cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc6173b2bbb09f0d3858408badb7b9ce14ac911992f16645bb321c7d3427c5c`

```dockerfile
```

-	Layers:
	-	`sha256:161974e701e67229efe4ca238bfa8c9e01cd184158efaf956c6ddc1901452e5a`  
		Last Modified: Thu, 02 Oct 2025 03:49:20 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.6.56`

```console
$ docker pull clickhouse@sha256:5775d1b0250370902ea04bf37d37583d8db744761aa81223ce648196f3bbc369
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.6.56` - linux; amd64

```console
$ docker pull clickhouse@sha256:79c0f0ba61b5a5f7284a10e9f671ccfeab8e445cca58929d14d9b5c30de86d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db22b7ed486ee977ad64ddca75012fb3118be31681443b2941bb0c0809c3fb5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.3.6.56
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b8b64bfc3c006da3dbdc8315726047223dc83bf809ec568a01a6282bb7c6d`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3063f406083ccf1f853493cc1903b17828299758cc838c0ae3ff5a1ab038e53a`  
		Last Modified: Tue, 02 Sep 2025 00:49:44 GMT  
		Size: 167.9 MB (167873557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068524848a39bc20273deb9c815010922e604f57cae4d762fe4a110be010b7cc`  
		Last Modified: Mon, 01 Sep 2025 23:09:01 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbfcd3b5b7985fa5315ff6a50d0e8302ff1ef18dc6ebe4087c197fd26b8483`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce48062e0dad3ffc672b574bd49b5254c21bc836e2cd928d35697d45107fa99`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239040b253b9101ca6a52d9fdf17f703d4d539ea63f832e9295ac84a2eeecb0`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ef3f7692f6964082a0ebad321915d0eab0f8f6e4c8c320b008376823e6fd63`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6.56` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50a83551816610e25f1c81d2c2b78c69e6ab1bffca8651469526761dce29669a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759649216f9edd7c53fc693d5297c37eb1089638406f26eb7694ea6961951a21`

```dockerfile
```

-	Layers:
	-	`sha256:c307d95fe108fe4572dfab6fbe5f75fa0d6ac491733f5cb90e7aaaab019461b2`  
		Last Modified: Tue, 02 Sep 2025 00:49:19 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.6.56` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e84618e2358bd900c2570a689c36b2616724390957829645328363d01f73b68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192935452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49c271763f7ebf803294a10c094a4c86f81880afc11f606e54012e89e2c71ee`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121c7ad3ac83b048884c02adca98157abf994fbb1d74705e59750f5995867c55`  
		Last Modified: Thu, 02 Oct 2025 03:49:28 GMT  
		Size: 7.1 MB (7127188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb81e8ce1c0e3bf764f862fa23dffef8b1771e96ddf366e04d8ed686e171d3ca`  
		Last Modified: Thu, 02 Oct 2025 03:49:38 GMT  
		Size: 157.6 MB (157554913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7a2398c1a8a3864d86081e87c48b95784089b1a3333ce835fbb2732f05256c`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d36473197c8e3f1fb7591d0e070152bb411e8a08823f3b5741de1d41b3d556`  
		Last Modified: Thu, 02 Oct 2025 01:54:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5b841c9bd049a592566d3d82f67bc63c24fcb26517737c19c47439096587f8`  
		Last Modified: Thu, 02 Oct 2025 01:54:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a8344b3fa142ebf1cec3a97c905b3ce9c76af46368c88cbb4011287a0cdfd7`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed403f5f13fcdb3851b9a45a3ca11d06ede3aa1ae3c9343c2c6947c7286069`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6.56` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b408decd5cd308f231858854ce60a464f8dd9bcd988ab560b792cf2a54127cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc6173b2bbb09f0d3858408badb7b9ce14ac911992f16645bb321c7d3427c5c`

```dockerfile
```

-	Layers:
	-	`sha256:161974e701e67229efe4ca238bfa8c9e01cd184158efaf956c6ddc1901452e5a`  
		Last Modified: Thu, 02 Oct 2025 03:49:20 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.6.56-jammy`

```console
$ docker pull clickhouse@sha256:5775d1b0250370902ea04bf37d37583d8db744761aa81223ce648196f3bbc369
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.6.56-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:79c0f0ba61b5a5f7284a10e9f671ccfeab8e445cca58929d14d9b5c30de86d20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.4 MB (205432385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db22b7ed486ee977ad64ddca75012fb3118be31681443b2941bb0c0809c3fb5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 28 Aug 2025 16:05:59 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 28 Aug 2025 16:05:59 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPO_CHANNEL=stable
# Thu, 28 Aug 2025 16:05:59 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 28 Aug 2025 16:05:59 GMT
ARG VERSION=25.3.6.56
# Thu, 28 Aug 2025 16:05:59 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
ENV LANG=en_US.UTF-8
# Thu, 28 Aug 2025 16:05:59 GMT
ENV TZ=UTC
# Thu, 28 Aug 2025 16:05:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 28 Aug 2025 16:05:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 28 Aug 2025 16:05:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 28 Aug 2025 16:05:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 28 Aug 2025 16:05:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28b8b64bfc3c006da3dbdc8315726047223dc83bf809ec568a01a6282bb7c6d`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 7.2 MB (7151643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3063f406083ccf1f853493cc1903b17828299758cc838c0ae3ff5a1ab038e53a`  
		Last Modified: Tue, 02 Sep 2025 00:49:44 GMT  
		Size: 167.9 MB (167873557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068524848a39bc20273deb9c815010922e604f57cae4d762fe4a110be010b7cc`  
		Last Modified: Mon, 01 Sep 2025 23:09:01 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bbfcd3b5b7985fa5315ff6a50d0e8302ff1ef18dc6ebe4087c197fd26b8483`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce48062e0dad3ffc672b574bd49b5254c21bc836e2cd928d35697d45107fa99`  
		Last Modified: Mon, 01 Sep 2025 23:09:02 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a239040b253b9101ca6a52d9fdf17f703d4d539ea63f832e9295ac84a2eeecb0`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ef3f7692f6964082a0ebad321915d0eab0f8f6e4c8c320b008376823e6fd63`  
		Last Modified: Mon, 01 Sep 2025 23:09:03 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6.56-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:50a83551816610e25f1c81d2c2b78c69e6ab1bffca8651469526761dce29669a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 KB (25875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759649216f9edd7c53fc693d5297c37eb1089638406f26eb7694ea6961951a21`

```dockerfile
```

-	Layers:
	-	`sha256:c307d95fe108fe4572dfab6fbe5f75fa0d6ac491733f5cb90e7aaaab019461b2`  
		Last Modified: Tue, 02 Sep 2025 00:49:19 GMT  
		Size: 25.9 KB (25875 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.6.56-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e84618e2358bd900c2570a689c36b2616724390957829645328363d01f73b68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.9 MB (192935452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49c271763f7ebf803294a10c094a4c86f81880afc11f606e54012e89e2c71ee`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.3.6.56
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.6.56 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121c7ad3ac83b048884c02adca98157abf994fbb1d74705e59750f5995867c55`  
		Last Modified: Thu, 02 Oct 2025 03:49:28 GMT  
		Size: 7.1 MB (7127188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb81e8ce1c0e3bf764f862fa23dffef8b1771e96ddf366e04d8ed686e171d3ca`  
		Last Modified: Thu, 02 Oct 2025 03:49:38 GMT  
		Size: 157.6 MB (157554913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7a2398c1a8a3864d86081e87c48b95784089b1a3333ce835fbb2732f05256c`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d36473197c8e3f1fb7591d0e070152bb411e8a08823f3b5741de1d41b3d556`  
		Last Modified: Thu, 02 Oct 2025 01:54:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5b841c9bd049a592566d3d82f67bc63c24fcb26517737c19c47439096587f8`  
		Last Modified: Thu, 02 Oct 2025 01:54:43 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a8344b3fa142ebf1cec3a97c905b3ce9c76af46368c88cbb4011287a0cdfd7`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ed403f5f13fcdb3851b9a45a3ca11d06ede3aa1ae3c9343c2c6947c7286069`  
		Last Modified: Thu, 02 Oct 2025 01:54:44 GMT  
		Size: 3.8 KB (3832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.6.56-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b408decd5cd308f231858854ce60a464f8dd9bcd988ab560b792cf2a54127cc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dc6173b2bbb09f0d3858408badb7b9ce14ac911992f16645bb321c7d3427c5c`

```dockerfile
```

-	Layers:
	-	`sha256:161974e701e67229efe4ca238bfa8c9e01cd184158efaf956c6ddc1901452e5a`  
		Last Modified: Thu, 02 Oct 2025 03:49:20 GMT  
		Size: 25.5 KB (25451 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6`

```console
$ docker pull clickhouse@sha256:cfb498dcf58a9c02f06423348315ac373b56c9f03a7871478f97469f3b687bfa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6` - linux; amd64

```console
$ docker pull clickhouse@sha256:e6e9df30da3b21e48f4059d0f60e98e4e9e88ef02b380789c5147597e71c0af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212107087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4289aa0834f0ca8d2260d14f874b9ed19df7aa3baa1df830c493238eb91b62f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce6346c3366f193d14d4e8075d749fa6fae7c27cf17debba55c640de6de214e`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 7.2 MB (7151606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ed3e49c1e9f332aa2ca092062811bf88d39810972fcce313242544cad8a449`  
		Last Modified: Thu, 18 Sep 2025 21:49:49 GMT  
		Size: 174.5 MB (174548520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9502f88569554c8eef0d2b14a41bcfc4aad686c6672551a8db9f65f26af39f42`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda514c12021b1f0e31c16cb0dd1c52bed5b03ea6629c3c232d2089d8cbef01`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b920a490da86c608609246454fb43df932f8558930408cec43a07cf2b6113a6`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b8785a807e8cc35a1c11672027702e500999c329bcb4d5b4cac504c54a448f`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e65c3600304b8a467921d36fa5e5346eb0396162dfb403b6f88110053e9174`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:269cb78b9eee5a609ab20b2c5977bd75a17443f7c5d7b0540af5b056c141d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ae60f6c19fae6eafefbeada71100b27b9293432fd6455e2da034bf1b8f55fb`

```dockerfile
```

-	Layers:
	-	`sha256:7b8b5f589470f5c47cadc70cdca67e4d73826144c94f1a56156022cace97d8ed`  
		Last Modified: Thu, 18 Sep 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f7c8af0e7a03bf58d6f667409a1f9cf2b3f31f964438676c6963683674753b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198268873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d89b1a4171e1b5113f1f5d297ff4c2ae97b0ec67fb6445ef19ecf50bbfd045`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.6.12.10
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367ec5f43992c60b09c17ee33e7e12761f084cc06e77a3da47fab947b920b042`  
		Last Modified: Thu, 02 Oct 2025 03:49:43 GMT  
		Size: 7.1 MB (7127243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91285ba2899cb4123c76379a914a7e0d5838a0f03a0c3c23f45cf50833a6544`  
		Last Modified: Thu, 02 Oct 2025 03:49:54 GMT  
		Size: 162.9 MB (162888501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdc606dba5ef56a78a5583d44ebb1494499931ad32268a4b7a0d24ad05615c3`  
		Last Modified: Thu, 02 Oct 2025 01:17:29 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcfc1f2e769ba5ae693feffd9d7de80c7f8a396a6f4249700c051e96a485992`  
		Last Modified: Thu, 02 Oct 2025 01:17:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e391b1713fe929ff58f3bddca94996c949ecdd2d171643328bf917d80edbbf05`  
		Last Modified: Thu, 02 Oct 2025 01:17:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b99642908f32326654663107bd4697c88c41390d94ddbc37174cbd32c8668e`  
		Last Modified: Thu, 02 Oct 2025 01:17:39 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385bb8fe0bd0f4d44e3a5e5874ac102c792d6da98a5737380ad2a2a7de4184e8`  
		Last Modified: Thu, 02 Oct 2025 01:17:42 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6` - unknown; unknown

```console
$ docker pull clickhouse@sha256:86515ffb351f3b1c29e92542e47984b7c936448cec4302043b59a8812c44ff70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1acc16935a07a80fdf772e8998e59721c23a25be776c5f3ea8384baa99b1d1c7`

```dockerfile
```

-	Layers:
	-	`sha256:5a98e04df1c902453ae7a938b4044e9b9c586d3f465c73328b8bf8bf7034e3aa`  
		Last Modified: Thu, 02 Oct 2025 03:49:35 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6-jammy`

```console
$ docker pull clickhouse@sha256:cfb498dcf58a9c02f06423348315ac373b56c9f03a7871478f97469f3b687bfa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e6e9df30da3b21e48f4059d0f60e98e4e9e88ef02b380789c5147597e71c0af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212107087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4289aa0834f0ca8d2260d14f874b9ed19df7aa3baa1df830c493238eb91b62f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce6346c3366f193d14d4e8075d749fa6fae7c27cf17debba55c640de6de214e`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 7.2 MB (7151606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ed3e49c1e9f332aa2ca092062811bf88d39810972fcce313242544cad8a449`  
		Last Modified: Thu, 18 Sep 2025 21:49:49 GMT  
		Size: 174.5 MB (174548520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9502f88569554c8eef0d2b14a41bcfc4aad686c6672551a8db9f65f26af39f42`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda514c12021b1f0e31c16cb0dd1c52bed5b03ea6629c3c232d2089d8cbef01`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b920a490da86c608609246454fb43df932f8558930408cec43a07cf2b6113a6`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b8785a807e8cc35a1c11672027702e500999c329bcb4d5b4cac504c54a448f`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e65c3600304b8a467921d36fa5e5346eb0396162dfb403b6f88110053e9174`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:269cb78b9eee5a609ab20b2c5977bd75a17443f7c5d7b0540af5b056c141d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ae60f6c19fae6eafefbeada71100b27b9293432fd6455e2da034bf1b8f55fb`

```dockerfile
```

-	Layers:
	-	`sha256:7b8b5f589470f5c47cadc70cdca67e4d73826144c94f1a56156022cace97d8ed`  
		Last Modified: Thu, 18 Sep 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f7c8af0e7a03bf58d6f667409a1f9cf2b3f31f964438676c6963683674753b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198268873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d89b1a4171e1b5113f1f5d297ff4c2ae97b0ec67fb6445ef19ecf50bbfd045`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.6.12.10
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367ec5f43992c60b09c17ee33e7e12761f084cc06e77a3da47fab947b920b042`  
		Last Modified: Thu, 02 Oct 2025 03:49:43 GMT  
		Size: 7.1 MB (7127243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91285ba2899cb4123c76379a914a7e0d5838a0f03a0c3c23f45cf50833a6544`  
		Last Modified: Thu, 02 Oct 2025 03:49:54 GMT  
		Size: 162.9 MB (162888501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdc606dba5ef56a78a5583d44ebb1494499931ad32268a4b7a0d24ad05615c3`  
		Last Modified: Thu, 02 Oct 2025 01:17:29 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcfc1f2e769ba5ae693feffd9d7de80c7f8a396a6f4249700c051e96a485992`  
		Last Modified: Thu, 02 Oct 2025 01:17:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e391b1713fe929ff58f3bddca94996c949ecdd2d171643328bf917d80edbbf05`  
		Last Modified: Thu, 02 Oct 2025 01:17:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b99642908f32326654663107bd4697c88c41390d94ddbc37174cbd32c8668e`  
		Last Modified: Thu, 02 Oct 2025 01:17:39 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385bb8fe0bd0f4d44e3a5e5874ac102c792d6da98a5737380ad2a2a7de4184e8`  
		Last Modified: Thu, 02 Oct 2025 01:17:42 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:86515ffb351f3b1c29e92542e47984b7c936448cec4302043b59a8812c44ff70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1acc16935a07a80fdf772e8998e59721c23a25be776c5f3ea8384baa99b1d1c7`

```dockerfile
```

-	Layers:
	-	`sha256:5a98e04df1c902453ae7a938b4044e9b9c586d3f465c73328b8bf8bf7034e3aa`  
		Last Modified: Thu, 02 Oct 2025 03:49:35 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.12`

```console
$ docker pull clickhouse@sha256:cfb498dcf58a9c02f06423348315ac373b56c9f03a7871478f97469f3b687bfa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.12` - linux; amd64

```console
$ docker pull clickhouse@sha256:e6e9df30da3b21e48f4059d0f60e98e4e9e88ef02b380789c5147597e71c0af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212107087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4289aa0834f0ca8d2260d14f874b9ed19df7aa3baa1df830c493238eb91b62f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce6346c3366f193d14d4e8075d749fa6fae7c27cf17debba55c640de6de214e`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 7.2 MB (7151606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ed3e49c1e9f332aa2ca092062811bf88d39810972fcce313242544cad8a449`  
		Last Modified: Thu, 18 Sep 2025 21:49:49 GMT  
		Size: 174.5 MB (174548520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9502f88569554c8eef0d2b14a41bcfc4aad686c6672551a8db9f65f26af39f42`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda514c12021b1f0e31c16cb0dd1c52bed5b03ea6629c3c232d2089d8cbef01`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b920a490da86c608609246454fb43df932f8558930408cec43a07cf2b6113a6`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b8785a807e8cc35a1c11672027702e500999c329bcb4d5b4cac504c54a448f`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e65c3600304b8a467921d36fa5e5346eb0396162dfb403b6f88110053e9174`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:269cb78b9eee5a609ab20b2c5977bd75a17443f7c5d7b0540af5b056c141d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ae60f6c19fae6eafefbeada71100b27b9293432fd6455e2da034bf1b8f55fb`

```dockerfile
```

-	Layers:
	-	`sha256:7b8b5f589470f5c47cadc70cdca67e4d73826144c94f1a56156022cace97d8ed`  
		Last Modified: Thu, 18 Sep 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.12` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f7c8af0e7a03bf58d6f667409a1f9cf2b3f31f964438676c6963683674753b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198268873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d89b1a4171e1b5113f1f5d297ff4c2ae97b0ec67fb6445ef19ecf50bbfd045`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.6.12.10
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367ec5f43992c60b09c17ee33e7e12761f084cc06e77a3da47fab947b920b042`  
		Last Modified: Thu, 02 Oct 2025 03:49:43 GMT  
		Size: 7.1 MB (7127243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91285ba2899cb4123c76379a914a7e0d5838a0f03a0c3c23f45cf50833a6544`  
		Last Modified: Thu, 02 Oct 2025 03:49:54 GMT  
		Size: 162.9 MB (162888501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdc606dba5ef56a78a5583d44ebb1494499931ad32268a4b7a0d24ad05615c3`  
		Last Modified: Thu, 02 Oct 2025 01:17:29 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcfc1f2e769ba5ae693feffd9d7de80c7f8a396a6f4249700c051e96a485992`  
		Last Modified: Thu, 02 Oct 2025 01:17:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e391b1713fe929ff58f3bddca94996c949ecdd2d171643328bf917d80edbbf05`  
		Last Modified: Thu, 02 Oct 2025 01:17:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b99642908f32326654663107bd4697c88c41390d94ddbc37174cbd32c8668e`  
		Last Modified: Thu, 02 Oct 2025 01:17:39 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385bb8fe0bd0f4d44e3a5e5874ac102c792d6da98a5737380ad2a2a7de4184e8`  
		Last Modified: Thu, 02 Oct 2025 01:17:42 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:86515ffb351f3b1c29e92542e47984b7c936448cec4302043b59a8812c44ff70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1acc16935a07a80fdf772e8998e59721c23a25be776c5f3ea8384baa99b1d1c7`

```dockerfile
```

-	Layers:
	-	`sha256:5a98e04df1c902453ae7a938b4044e9b9c586d3f465c73328b8bf8bf7034e3aa`  
		Last Modified: Thu, 02 Oct 2025 03:49:35 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.12-jammy`

```console
$ docker pull clickhouse@sha256:cfb498dcf58a9c02f06423348315ac373b56c9f03a7871478f97469f3b687bfa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.12-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e6e9df30da3b21e48f4059d0f60e98e4e9e88ef02b380789c5147597e71c0af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212107087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4289aa0834f0ca8d2260d14f874b9ed19df7aa3baa1df830c493238eb91b62f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce6346c3366f193d14d4e8075d749fa6fae7c27cf17debba55c640de6de214e`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 7.2 MB (7151606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ed3e49c1e9f332aa2ca092062811bf88d39810972fcce313242544cad8a449`  
		Last Modified: Thu, 18 Sep 2025 21:49:49 GMT  
		Size: 174.5 MB (174548520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9502f88569554c8eef0d2b14a41bcfc4aad686c6672551a8db9f65f26af39f42`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda514c12021b1f0e31c16cb0dd1c52bed5b03ea6629c3c232d2089d8cbef01`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b920a490da86c608609246454fb43df932f8558930408cec43a07cf2b6113a6`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b8785a807e8cc35a1c11672027702e500999c329bcb4d5b4cac504c54a448f`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e65c3600304b8a467921d36fa5e5346eb0396162dfb403b6f88110053e9174`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:269cb78b9eee5a609ab20b2c5977bd75a17443f7c5d7b0540af5b056c141d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ae60f6c19fae6eafefbeada71100b27b9293432fd6455e2da034bf1b8f55fb`

```dockerfile
```

-	Layers:
	-	`sha256:7b8b5f589470f5c47cadc70cdca67e4d73826144c94f1a56156022cace97d8ed`  
		Last Modified: Thu, 18 Sep 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.12-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f7c8af0e7a03bf58d6f667409a1f9cf2b3f31f964438676c6963683674753b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198268873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d89b1a4171e1b5113f1f5d297ff4c2ae97b0ec67fb6445ef19ecf50bbfd045`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.6.12.10
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367ec5f43992c60b09c17ee33e7e12761f084cc06e77a3da47fab947b920b042`  
		Last Modified: Thu, 02 Oct 2025 03:49:43 GMT  
		Size: 7.1 MB (7127243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91285ba2899cb4123c76379a914a7e0d5838a0f03a0c3c23f45cf50833a6544`  
		Last Modified: Thu, 02 Oct 2025 03:49:54 GMT  
		Size: 162.9 MB (162888501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdc606dba5ef56a78a5583d44ebb1494499931ad32268a4b7a0d24ad05615c3`  
		Last Modified: Thu, 02 Oct 2025 01:17:29 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcfc1f2e769ba5ae693feffd9d7de80c7f8a396a6f4249700c051e96a485992`  
		Last Modified: Thu, 02 Oct 2025 01:17:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e391b1713fe929ff58f3bddca94996c949ecdd2d171643328bf917d80edbbf05`  
		Last Modified: Thu, 02 Oct 2025 01:17:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b99642908f32326654663107bd4697c88c41390d94ddbc37174cbd32c8668e`  
		Last Modified: Thu, 02 Oct 2025 01:17:39 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385bb8fe0bd0f4d44e3a5e5874ac102c792d6da98a5737380ad2a2a7de4184e8`  
		Last Modified: Thu, 02 Oct 2025 01:17:42 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:86515ffb351f3b1c29e92542e47984b7c936448cec4302043b59a8812c44ff70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1acc16935a07a80fdf772e8998e59721c23a25be776c5f3ea8384baa99b1d1c7`

```dockerfile
```

-	Layers:
	-	`sha256:5a98e04df1c902453ae7a938b4044e9b9c586d3f465c73328b8bf8bf7034e3aa`  
		Last Modified: Thu, 02 Oct 2025 03:49:35 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.12.10`

```console
$ docker pull clickhouse@sha256:cfb498dcf58a9c02f06423348315ac373b56c9f03a7871478f97469f3b687bfa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.12.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:e6e9df30da3b21e48f4059d0f60e98e4e9e88ef02b380789c5147597e71c0af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212107087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4289aa0834f0ca8d2260d14f874b9ed19df7aa3baa1df830c493238eb91b62f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce6346c3366f193d14d4e8075d749fa6fae7c27cf17debba55c640de6de214e`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 7.2 MB (7151606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ed3e49c1e9f332aa2ca092062811bf88d39810972fcce313242544cad8a449`  
		Last Modified: Thu, 18 Sep 2025 21:49:49 GMT  
		Size: 174.5 MB (174548520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9502f88569554c8eef0d2b14a41bcfc4aad686c6672551a8db9f65f26af39f42`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda514c12021b1f0e31c16cb0dd1c52bed5b03ea6629c3c232d2089d8cbef01`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b920a490da86c608609246454fb43df932f8558930408cec43a07cf2b6113a6`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b8785a807e8cc35a1c11672027702e500999c329bcb4d5b4cac504c54a448f`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e65c3600304b8a467921d36fa5e5346eb0396162dfb403b6f88110053e9174`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.12.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:269cb78b9eee5a609ab20b2c5977bd75a17443f7c5d7b0540af5b056c141d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ae60f6c19fae6eafefbeada71100b27b9293432fd6455e2da034bf1b8f55fb`

```dockerfile
```

-	Layers:
	-	`sha256:7b8b5f589470f5c47cadc70cdca67e4d73826144c94f1a56156022cace97d8ed`  
		Last Modified: Thu, 18 Sep 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.12.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f7c8af0e7a03bf58d6f667409a1f9cf2b3f31f964438676c6963683674753b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198268873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d89b1a4171e1b5113f1f5d297ff4c2ae97b0ec67fb6445ef19ecf50bbfd045`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.6.12.10
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367ec5f43992c60b09c17ee33e7e12761f084cc06e77a3da47fab947b920b042`  
		Last Modified: Thu, 02 Oct 2025 03:49:43 GMT  
		Size: 7.1 MB (7127243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91285ba2899cb4123c76379a914a7e0d5838a0f03a0c3c23f45cf50833a6544`  
		Last Modified: Thu, 02 Oct 2025 03:49:54 GMT  
		Size: 162.9 MB (162888501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdc606dba5ef56a78a5583d44ebb1494499931ad32268a4b7a0d24ad05615c3`  
		Last Modified: Thu, 02 Oct 2025 01:17:29 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcfc1f2e769ba5ae693feffd9d7de80c7f8a396a6f4249700c051e96a485992`  
		Last Modified: Thu, 02 Oct 2025 01:17:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e391b1713fe929ff58f3bddca94996c949ecdd2d171643328bf917d80edbbf05`  
		Last Modified: Thu, 02 Oct 2025 01:17:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b99642908f32326654663107bd4697c88c41390d94ddbc37174cbd32c8668e`  
		Last Modified: Thu, 02 Oct 2025 01:17:39 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385bb8fe0bd0f4d44e3a5e5874ac102c792d6da98a5737380ad2a2a7de4184e8`  
		Last Modified: Thu, 02 Oct 2025 01:17:42 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.12.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:86515ffb351f3b1c29e92542e47984b7c936448cec4302043b59a8812c44ff70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1acc16935a07a80fdf772e8998e59721c23a25be776c5f3ea8384baa99b1d1c7`

```dockerfile
```

-	Layers:
	-	`sha256:5a98e04df1c902453ae7a938b4044e9b9c586d3f465c73328b8bf8bf7034e3aa`  
		Last Modified: Thu, 02 Oct 2025 03:49:35 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.6.12.10-jammy`

```console
$ docker pull clickhouse@sha256:cfb498dcf58a9c02f06423348315ac373b56c9f03a7871478f97469f3b687bfa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.6.12.10-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:e6e9df30da3b21e48f4059d0f60e98e4e9e88ef02b380789c5147597e71c0af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212107087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4289aa0834f0ca8d2260d14f874b9ed19df7aa3baa1df830c493238eb91b62f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 18 Sep 2025 16:06:29 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 18 Sep 2025 16:06:29 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPO_CHANNEL=stable
# Thu, 18 Sep 2025 16:06:29 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 18 Sep 2025 16:06:29 GMT
ARG VERSION=25.6.12.10
# Thu, 18 Sep 2025 16:06:29 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
ENV LANG=en_US.UTF-8
# Thu, 18 Sep 2025 16:06:29 GMT
ENV TZ=UTC
# Thu, 18 Sep 2025 16:06:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 18 Sep 2025 16:06:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 18 Sep 2025 16:06:29 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 18 Sep 2025 16:06:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 18 Sep 2025 16:06:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce6346c3366f193d14d4e8075d749fa6fae7c27cf17debba55c640de6de214e`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 7.2 MB (7151606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ed3e49c1e9f332aa2ca092062811bf88d39810972fcce313242544cad8a449`  
		Last Modified: Thu, 18 Sep 2025 21:49:49 GMT  
		Size: 174.5 MB (174548520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9502f88569554c8eef0d2b14a41bcfc4aad686c6672551a8db9f65f26af39f42`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bda514c12021b1f0e31c16cb0dd1c52bed5b03ea6629c3c232d2089d8cbef01`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b920a490da86c608609246454fb43df932f8558930408cec43a07cf2b6113a6`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b8785a807e8cc35a1c11672027702e500999c329bcb4d5b4cac504c54a448f`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e65c3600304b8a467921d36fa5e5346eb0396162dfb403b6f88110053e9174`  
		Last Modified: Thu, 18 Sep 2025 19:01:18 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.12.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:269cb78b9eee5a609ab20b2c5977bd75a17443f7c5d7b0540af5b056c141d1b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 KB (25278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5ae60f6c19fae6eafefbeada71100b27b9293432fd6455e2da034bf1b8f55fb`

```dockerfile
```

-	Layers:
	-	`sha256:7b8b5f589470f5c47cadc70cdca67e4d73826144c94f1a56156022cace97d8ed`  
		Last Modified: Thu, 18 Sep 2025 21:49:23 GMT  
		Size: 25.3 KB (25278 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.6.12.10-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f7c8af0e7a03bf58d6f667409a1f9cf2b3f31f964438676c6963683674753b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.3 MB (198268873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43d89b1a4171e1b5113f1f5d297ff4c2ae97b0ec67fb6445ef19ecf50bbfd045`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.6.12.10
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.6.12.10 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367ec5f43992c60b09c17ee33e7e12761f084cc06e77a3da47fab947b920b042`  
		Last Modified: Thu, 02 Oct 2025 03:49:43 GMT  
		Size: 7.1 MB (7127243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91285ba2899cb4123c76379a914a7e0d5838a0f03a0c3c23f45cf50833a6544`  
		Last Modified: Thu, 02 Oct 2025 03:49:54 GMT  
		Size: 162.9 MB (162888501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdc606dba5ef56a78a5583d44ebb1494499931ad32268a4b7a0d24ad05615c3`  
		Last Modified: Thu, 02 Oct 2025 01:17:29 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adcfc1f2e769ba5ae693feffd9d7de80c7f8a396a6f4249700c051e96a485992`  
		Last Modified: Thu, 02 Oct 2025 01:17:32 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e391b1713fe929ff58f3bddca94996c949ecdd2d171643328bf917d80edbbf05`  
		Last Modified: Thu, 02 Oct 2025 01:17:36 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b99642908f32326654663107bd4697c88c41390d94ddbc37174cbd32c8668e`  
		Last Modified: Thu, 02 Oct 2025 01:17:39 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385bb8fe0bd0f4d44e3a5e5874ac102c792d6da98a5737380ad2a2a7de4184e8`  
		Last Modified: Thu, 02 Oct 2025 01:17:42 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.6.12.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:86515ffb351f3b1c29e92542e47984b7c936448cec4302043b59a8812c44ff70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1acc16935a07a80fdf772e8998e59721c23a25be776c5f3ea8384baa99b1d1c7`

```dockerfile
```

-	Layers:
	-	`sha256:5a98e04df1c902453ae7a938b4044e9b9c586d3f465c73328b8bf8bf7034e3aa`  
		Last Modified: Thu, 02 Oct 2025 03:49:35 GMT  
		Size: 25.5 KB (25466 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7`

```console
$ docker pull clickhouse@sha256:54fcc60dc17f4cceb12b900fb796fe7c6a80fae74711230fdd8f405c27a177b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:6bb0972af794c51cd257cec37ff8fb2bc0585972398596bfe043dd74fc47c7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221873228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c844005318524dcde3dc199412ccc2b5987b7c6a398bb62356d055dfe63705`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcdcbe58c9000f60fbbd97b9c476d599cc9fb9a5b78995b368361badcb1194e`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 7.6 MB (7598481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0302f8ab0fa5c939b2444dd3b6169eda23d4dabef613fb0f4040607f16bd52a4`  
		Last Modified: Thu, 25 Sep 2025 18:50:02 GMT  
		Size: 183.9 MB (183867788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ed5371ab3e6289a59f3ba06e5ace31e101319cb4d0d80222540350f6d24426`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6c29ab3bd6eaefe7b6bb7cb0afd19b324b662f8cf01574c7a9d48e129ac57`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a663001f0e3ee3ded89f4dcea562b36ae70f5efabeeb84e4204ffd818f407c87`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2278ee103d75b0f3fff12c113541676a7bd3b6b95e772ff65f3e60eced55b3b`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1048cb093d408574524c2db35d765ccd67612b5a3199772c288aa09df4d96c76`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:de370f920364dd41bb6de3629a2af4a6b0778b13dae8987a092b7a3cb2585b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0b70ac8fe94c416eadc25a56dc6a1fc660887f6e47cd37ae26c97dfb36f53`

```dockerfile
```

-	Layers:
	-	`sha256:65340b8583184dd5fe44f052d3bf95890b4e2f552792c19f59382ce9240c7aec`  
		Last Modified: Thu, 25 Sep 2025 18:49:27 GMT  
		Size: 25.5 KB (25460 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:654f9f9792a490cf31b8faf092dd0196a1acebd74f9ff987b6108b37beacc595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207808212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bea0072278540189a4781d584a7921ece0d54d58d5c02a84aa34b7b072d333`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f94767786dd605041010b9d16653de707d91e62034e95623a17796da8185b2`  
		Last Modified: Thu, 02 Oct 2025 01:12:26 GMT  
		Size: 7.6 MB (7576770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd8cfb8284a935883ded63626c9a02613f38a6f1d72e24a0487bc8725e835c9`  
		Last Modified: Thu, 02 Oct 2025 03:50:04 GMT  
		Size: 172.0 MB (171978314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b798be5d225971c859628d094e0957d2abbb945f0113b2d8a98191455b56fa`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b80b1373027e5b7339e0c84585c86f0ed7781c65afed3f8fd7cf06b7db4a3ba`  
		Last Modified: Thu, 02 Oct 2025 01:12:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d58690354538fb0a70d4a5106b1341eac71c7c43859cf5ca8c1cddee95f880`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0e7fcee7279dd29c01faff2af14f1efb62774b342ee417b91dde2375649973`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af957979b178b1b8c4ed03ba8373db31657a1a88f924857fdee7437e2af1bfc`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0cc600df8da426fb45d86649d9350a4680b090ba14c3c65c3ad418fea36fcf1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abaab9efc046d1524a4b74c6557dc78d6a28688a6ea76b10198972b47b53904`

```dockerfile
```

-	Layers:
	-	`sha256:77191bebcc2e1327227c0cb0b905aede42a7f88f90087ceb3693e0e9b0b620be`  
		Last Modified: Thu, 02 Oct 2025 03:49:51 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7-jammy`

```console
$ docker pull clickhouse@sha256:54fcc60dc17f4cceb12b900fb796fe7c6a80fae74711230fdd8f405c27a177b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:6bb0972af794c51cd257cec37ff8fb2bc0585972398596bfe043dd74fc47c7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221873228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c844005318524dcde3dc199412ccc2b5987b7c6a398bb62356d055dfe63705`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcdcbe58c9000f60fbbd97b9c476d599cc9fb9a5b78995b368361badcb1194e`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 7.6 MB (7598481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0302f8ab0fa5c939b2444dd3b6169eda23d4dabef613fb0f4040607f16bd52a4`  
		Last Modified: Thu, 25 Sep 2025 18:50:02 GMT  
		Size: 183.9 MB (183867788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ed5371ab3e6289a59f3ba06e5ace31e101319cb4d0d80222540350f6d24426`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6c29ab3bd6eaefe7b6bb7cb0afd19b324b662f8cf01574c7a9d48e129ac57`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a663001f0e3ee3ded89f4dcea562b36ae70f5efabeeb84e4204ffd818f407c87`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2278ee103d75b0f3fff12c113541676a7bd3b6b95e772ff65f3e60eced55b3b`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1048cb093d408574524c2db35d765ccd67612b5a3199772c288aa09df4d96c76`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:de370f920364dd41bb6de3629a2af4a6b0778b13dae8987a092b7a3cb2585b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0b70ac8fe94c416eadc25a56dc6a1fc660887f6e47cd37ae26c97dfb36f53`

```dockerfile
```

-	Layers:
	-	`sha256:65340b8583184dd5fe44f052d3bf95890b4e2f552792c19f59382ce9240c7aec`  
		Last Modified: Thu, 25 Sep 2025 18:49:27 GMT  
		Size: 25.5 KB (25460 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:654f9f9792a490cf31b8faf092dd0196a1acebd74f9ff987b6108b37beacc595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207808212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bea0072278540189a4781d584a7921ece0d54d58d5c02a84aa34b7b072d333`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f94767786dd605041010b9d16653de707d91e62034e95623a17796da8185b2`  
		Last Modified: Thu, 02 Oct 2025 01:12:26 GMT  
		Size: 7.6 MB (7576770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd8cfb8284a935883ded63626c9a02613f38a6f1d72e24a0487bc8725e835c9`  
		Last Modified: Thu, 02 Oct 2025 03:50:04 GMT  
		Size: 172.0 MB (171978314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b798be5d225971c859628d094e0957d2abbb945f0113b2d8a98191455b56fa`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b80b1373027e5b7339e0c84585c86f0ed7781c65afed3f8fd7cf06b7db4a3ba`  
		Last Modified: Thu, 02 Oct 2025 01:12:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d58690354538fb0a70d4a5106b1341eac71c7c43859cf5ca8c1cddee95f880`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0e7fcee7279dd29c01faff2af14f1efb62774b342ee417b91dde2375649973`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af957979b178b1b8c4ed03ba8373db31657a1a88f924857fdee7437e2af1bfc`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0cc600df8da426fb45d86649d9350a4680b090ba14c3c65c3ad418fea36fcf1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abaab9efc046d1524a4b74c6557dc78d6a28688a6ea76b10198972b47b53904`

```dockerfile
```

-	Layers:
	-	`sha256:77191bebcc2e1327227c0cb0b905aede42a7f88f90087ceb3693e0e9b0b620be`  
		Last Modified: Thu, 02 Oct 2025 03:49:51 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.7`

```console
$ docker pull clickhouse@sha256:54fcc60dc17f4cceb12b900fb796fe7c6a80fae74711230fdd8f405c27a177b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:6bb0972af794c51cd257cec37ff8fb2bc0585972398596bfe043dd74fc47c7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221873228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c844005318524dcde3dc199412ccc2b5987b7c6a398bb62356d055dfe63705`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcdcbe58c9000f60fbbd97b9c476d599cc9fb9a5b78995b368361badcb1194e`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 7.6 MB (7598481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0302f8ab0fa5c939b2444dd3b6169eda23d4dabef613fb0f4040607f16bd52a4`  
		Last Modified: Thu, 25 Sep 2025 18:50:02 GMT  
		Size: 183.9 MB (183867788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ed5371ab3e6289a59f3ba06e5ace31e101319cb4d0d80222540350f6d24426`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6c29ab3bd6eaefe7b6bb7cb0afd19b324b662f8cf01574c7a9d48e129ac57`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a663001f0e3ee3ded89f4dcea562b36ae70f5efabeeb84e4204ffd818f407c87`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2278ee103d75b0f3fff12c113541676a7bd3b6b95e772ff65f3e60eced55b3b`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1048cb093d408574524c2db35d765ccd67612b5a3199772c288aa09df4d96c76`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:de370f920364dd41bb6de3629a2af4a6b0778b13dae8987a092b7a3cb2585b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0b70ac8fe94c416eadc25a56dc6a1fc660887f6e47cd37ae26c97dfb36f53`

```dockerfile
```

-	Layers:
	-	`sha256:65340b8583184dd5fe44f052d3bf95890b4e2f552792c19f59382ce9240c7aec`  
		Last Modified: Thu, 25 Sep 2025 18:49:27 GMT  
		Size: 25.5 KB (25460 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:654f9f9792a490cf31b8faf092dd0196a1acebd74f9ff987b6108b37beacc595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207808212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bea0072278540189a4781d584a7921ece0d54d58d5c02a84aa34b7b072d333`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f94767786dd605041010b9d16653de707d91e62034e95623a17796da8185b2`  
		Last Modified: Thu, 02 Oct 2025 01:12:26 GMT  
		Size: 7.6 MB (7576770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd8cfb8284a935883ded63626c9a02613f38a6f1d72e24a0487bc8725e835c9`  
		Last Modified: Thu, 02 Oct 2025 03:50:04 GMT  
		Size: 172.0 MB (171978314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b798be5d225971c859628d094e0957d2abbb945f0113b2d8a98191455b56fa`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b80b1373027e5b7339e0c84585c86f0ed7781c65afed3f8fd7cf06b7db4a3ba`  
		Last Modified: Thu, 02 Oct 2025 01:12:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d58690354538fb0a70d4a5106b1341eac71c7c43859cf5ca8c1cddee95f880`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0e7fcee7279dd29c01faff2af14f1efb62774b342ee417b91dde2375649973`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af957979b178b1b8c4ed03ba8373db31657a1a88f924857fdee7437e2af1bfc`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0cc600df8da426fb45d86649d9350a4680b090ba14c3c65c3ad418fea36fcf1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abaab9efc046d1524a4b74c6557dc78d6a28688a6ea76b10198972b47b53904`

```dockerfile
```

-	Layers:
	-	`sha256:77191bebcc2e1327227c0cb0b905aede42a7f88f90087ceb3693e0e9b0b620be`  
		Last Modified: Thu, 02 Oct 2025 03:49:51 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.7-jammy`

```console
$ docker pull clickhouse@sha256:54fcc60dc17f4cceb12b900fb796fe7c6a80fae74711230fdd8f405c27a177b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:6bb0972af794c51cd257cec37ff8fb2bc0585972398596bfe043dd74fc47c7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221873228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c844005318524dcde3dc199412ccc2b5987b7c6a398bb62356d055dfe63705`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcdcbe58c9000f60fbbd97b9c476d599cc9fb9a5b78995b368361badcb1194e`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 7.6 MB (7598481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0302f8ab0fa5c939b2444dd3b6169eda23d4dabef613fb0f4040607f16bd52a4`  
		Last Modified: Thu, 25 Sep 2025 18:50:02 GMT  
		Size: 183.9 MB (183867788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ed5371ab3e6289a59f3ba06e5ace31e101319cb4d0d80222540350f6d24426`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6c29ab3bd6eaefe7b6bb7cb0afd19b324b662f8cf01574c7a9d48e129ac57`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a663001f0e3ee3ded89f4dcea562b36ae70f5efabeeb84e4204ffd818f407c87`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2278ee103d75b0f3fff12c113541676a7bd3b6b95e772ff65f3e60eced55b3b`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1048cb093d408574524c2db35d765ccd67612b5a3199772c288aa09df4d96c76`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:de370f920364dd41bb6de3629a2af4a6b0778b13dae8987a092b7a3cb2585b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0b70ac8fe94c416eadc25a56dc6a1fc660887f6e47cd37ae26c97dfb36f53`

```dockerfile
```

-	Layers:
	-	`sha256:65340b8583184dd5fe44f052d3bf95890b4e2f552792c19f59382ce9240c7aec`  
		Last Modified: Thu, 25 Sep 2025 18:49:27 GMT  
		Size: 25.5 KB (25460 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:654f9f9792a490cf31b8faf092dd0196a1acebd74f9ff987b6108b37beacc595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207808212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bea0072278540189a4781d584a7921ece0d54d58d5c02a84aa34b7b072d333`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f94767786dd605041010b9d16653de707d91e62034e95623a17796da8185b2`  
		Last Modified: Thu, 02 Oct 2025 01:12:26 GMT  
		Size: 7.6 MB (7576770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd8cfb8284a935883ded63626c9a02613f38a6f1d72e24a0487bc8725e835c9`  
		Last Modified: Thu, 02 Oct 2025 03:50:04 GMT  
		Size: 172.0 MB (171978314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b798be5d225971c859628d094e0957d2abbb945f0113b2d8a98191455b56fa`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b80b1373027e5b7339e0c84585c86f0ed7781c65afed3f8fd7cf06b7db4a3ba`  
		Last Modified: Thu, 02 Oct 2025 01:12:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d58690354538fb0a70d4a5106b1341eac71c7c43859cf5ca8c1cddee95f880`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0e7fcee7279dd29c01faff2af14f1efb62774b342ee417b91dde2375649973`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af957979b178b1b8c4ed03ba8373db31657a1a88f924857fdee7437e2af1bfc`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0cc600df8da426fb45d86649d9350a4680b090ba14c3c65c3ad418fea36fcf1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abaab9efc046d1524a4b74c6557dc78d6a28688a6ea76b10198972b47b53904`

```dockerfile
```

-	Layers:
	-	`sha256:77191bebcc2e1327227c0cb0b905aede42a7f88f90087ceb3693e0e9b0b620be`  
		Last Modified: Thu, 02 Oct 2025 03:49:51 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.7.68`

```console
$ docker pull clickhouse@sha256:54fcc60dc17f4cceb12b900fb796fe7c6a80fae74711230fdd8f405c27a177b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.7.68` - linux; amd64

```console
$ docker pull clickhouse@sha256:6bb0972af794c51cd257cec37ff8fb2bc0585972398596bfe043dd74fc47c7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221873228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c844005318524dcde3dc199412ccc2b5987b7c6a398bb62356d055dfe63705`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcdcbe58c9000f60fbbd97b9c476d599cc9fb9a5b78995b368361badcb1194e`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 7.6 MB (7598481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0302f8ab0fa5c939b2444dd3b6169eda23d4dabef613fb0f4040607f16bd52a4`  
		Last Modified: Thu, 25 Sep 2025 18:50:02 GMT  
		Size: 183.9 MB (183867788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ed5371ab3e6289a59f3ba06e5ace31e101319cb4d0d80222540350f6d24426`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6c29ab3bd6eaefe7b6bb7cb0afd19b324b662f8cf01574c7a9d48e129ac57`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a663001f0e3ee3ded89f4dcea562b36ae70f5efabeeb84e4204ffd818f407c87`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2278ee103d75b0f3fff12c113541676a7bd3b6b95e772ff65f3e60eced55b3b`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1048cb093d408574524c2db35d765ccd67612b5a3199772c288aa09df4d96c76`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7.68` - unknown; unknown

```console
$ docker pull clickhouse@sha256:de370f920364dd41bb6de3629a2af4a6b0778b13dae8987a092b7a3cb2585b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0b70ac8fe94c416eadc25a56dc6a1fc660887f6e47cd37ae26c97dfb36f53`

```dockerfile
```

-	Layers:
	-	`sha256:65340b8583184dd5fe44f052d3bf95890b4e2f552792c19f59382ce9240c7aec`  
		Last Modified: Thu, 25 Sep 2025 18:49:27 GMT  
		Size: 25.5 KB (25460 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.7.68` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:654f9f9792a490cf31b8faf092dd0196a1acebd74f9ff987b6108b37beacc595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207808212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bea0072278540189a4781d584a7921ece0d54d58d5c02a84aa34b7b072d333`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f94767786dd605041010b9d16653de707d91e62034e95623a17796da8185b2`  
		Last Modified: Thu, 02 Oct 2025 01:12:26 GMT  
		Size: 7.6 MB (7576770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd8cfb8284a935883ded63626c9a02613f38a6f1d72e24a0487bc8725e835c9`  
		Last Modified: Thu, 02 Oct 2025 03:50:04 GMT  
		Size: 172.0 MB (171978314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b798be5d225971c859628d094e0957d2abbb945f0113b2d8a98191455b56fa`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b80b1373027e5b7339e0c84585c86f0ed7781c65afed3f8fd7cf06b7db4a3ba`  
		Last Modified: Thu, 02 Oct 2025 01:12:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d58690354538fb0a70d4a5106b1341eac71c7c43859cf5ca8c1cddee95f880`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0e7fcee7279dd29c01faff2af14f1efb62774b342ee417b91dde2375649973`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af957979b178b1b8c4ed03ba8373db31657a1a88f924857fdee7437e2af1bfc`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7.68` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0cc600df8da426fb45d86649d9350a4680b090ba14c3c65c3ad418fea36fcf1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abaab9efc046d1524a4b74c6557dc78d6a28688a6ea76b10198972b47b53904`

```dockerfile
```

-	Layers:
	-	`sha256:77191bebcc2e1327227c0cb0b905aede42a7f88f90087ceb3693e0e9b0b620be`  
		Last Modified: Thu, 02 Oct 2025 03:49:51 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.7.7.68-jammy`

```console
$ docker pull clickhouse@sha256:54fcc60dc17f4cceb12b900fb796fe7c6a80fae74711230fdd8f405c27a177b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.7.7.68-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:6bb0972af794c51cd257cec37ff8fb2bc0585972398596bfe043dd74fc47c7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221873228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c844005318524dcde3dc199412ccc2b5987b7c6a398bb62356d055dfe63705`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcdcbe58c9000f60fbbd97b9c476d599cc9fb9a5b78995b368361badcb1194e`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 7.6 MB (7598481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0302f8ab0fa5c939b2444dd3b6169eda23d4dabef613fb0f4040607f16bd52a4`  
		Last Modified: Thu, 25 Sep 2025 18:50:02 GMT  
		Size: 183.9 MB (183867788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ed5371ab3e6289a59f3ba06e5ace31e101319cb4d0d80222540350f6d24426`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6c29ab3bd6eaefe7b6bb7cb0afd19b324b662f8cf01574c7a9d48e129ac57`  
		Last Modified: Thu, 25 Sep 2025 17:40:25 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a663001f0e3ee3ded89f4dcea562b36ae70f5efabeeb84e4204ffd818f407c87`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2278ee103d75b0f3fff12c113541676a7bd3b6b95e772ff65f3e60eced55b3b`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1048cb093d408574524c2db35d765ccd67612b5a3199772c288aa09df4d96c76`  
		Last Modified: Thu, 25 Sep 2025 17:40:26 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7.68-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:de370f920364dd41bb6de3629a2af4a6b0778b13dae8987a092b7a3cb2585b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.5 KB (25460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ee0b70ac8fe94c416eadc25a56dc6a1fc660887f6e47cd37ae26c97dfb36f53`

```dockerfile
```

-	Layers:
	-	`sha256:65340b8583184dd5fe44f052d3bf95890b4e2f552792c19f59382ce9240c7aec`  
		Last Modified: Thu, 25 Sep 2025 18:49:27 GMT  
		Size: 25.5 KB (25460 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.7.7.68-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:654f9f9792a490cf31b8faf092dd0196a1acebd74f9ff987b6108b37beacc595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.8 MB (207808212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bea0072278540189a4781d584a7921ece0d54d58d5c02a84aa34b7b072d333`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.7.7.68
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.7.7.68 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f94767786dd605041010b9d16653de707d91e62034e95623a17796da8185b2`  
		Last Modified: Thu, 02 Oct 2025 01:12:26 GMT  
		Size: 7.6 MB (7576770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd8cfb8284a935883ded63626c9a02613f38a6f1d72e24a0487bc8725e835c9`  
		Last Modified: Thu, 02 Oct 2025 03:50:04 GMT  
		Size: 172.0 MB (171978314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b798be5d225971c859628d094e0957d2abbb945f0113b2d8a98191455b56fa`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 183.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b80b1373027e5b7339e0c84585c86f0ed7781c65afed3f8fd7cf06b7db4a3ba`  
		Last Modified: Thu, 02 Oct 2025 01:12:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d58690354538fb0a70d4a5106b1341eac71c7c43859cf5ca8c1cddee95f880`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf0e7fcee7279dd29c01faff2af14f1efb62774b342ee417b91dde2375649973`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af957979b178b1b8c4ed03ba8373db31657a1a88f924857fdee7437e2af1bfc`  
		Last Modified: Thu, 02 Oct 2025 01:12:24 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.7.7.68-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:0cc600df8da426fb45d86649d9350a4680b090ba14c3c65c3ad418fea36fcf1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abaab9efc046d1524a4b74c6557dc78d6a28688a6ea76b10198972b47b53904`

```dockerfile
```

-	Layers:
	-	`sha256:77191bebcc2e1327227c0cb0b905aede42a7f88f90087ceb3693e0e9b0b620be`  
		Last Modified: Thu, 02 Oct 2025 03:49:51 GMT  
		Size: 25.6 KB (25649 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:613890f20c8128e9800d8b84abe50da018738af10db4852f86def606fe81de8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45284e11c1916b8d698c58fd4b1846a5cc479def5c671dc893ba67141b54ee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048d65318933af6af4c7e2790f9c3383163df5fa896bbbf80fd440a452c99378`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4883af93add6aae279fee4649bdd1d9a995335a7b6cd56571e0ede5cfa3c90`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 7.6 MB (7576745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62f433a9dc52cc27e53173033688da9385d89f33f61dd1e46616b648cfff9`  
		Last Modified: Thu, 02 Oct 2025 02:24:49 GMT  
		Size: 176.7 MB (176677340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef118ea534c5f67e1733824d0cd7a13aaba75dc7bb545ce03afab3286467ca5`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4bec4fdc4dd175e242482d8672c5c8afd4a7fc3fa304e09269fae978f4c184`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91de072e68e8b01b4fd9357d35930c646ef7ccc02b54c6c03ce76759ec1818`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769598cb0247656c5f52149dd01b09b949dd69468ce37a3cfb5e98734203a77`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ca6509233f0226292153cc6fcbd7220b85bda4fae17c3f358a26ab50d72a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf4e7ea6c71047f751747bf2ab58a259474d110a32215457e7662746ac40a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b22bc64f6f1857003da985a561708f816fe8b2ef5b91efe7f618f012e9f0ab`

```dockerfile
```

-	Layers:
	-	`sha256:bf39405f3719575281fce885837c911be2e82299da903bf952b3b3da3de8edf3`  
		Last Modified: Thu, 02 Oct 2025 03:50:05 GMT  
		Size: 26.9 KB (26908 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:613890f20c8128e9800d8b84abe50da018738af10db4852f86def606fe81de8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45284e11c1916b8d698c58fd4b1846a5cc479def5c671dc893ba67141b54ee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048d65318933af6af4c7e2790f9c3383163df5fa896bbbf80fd440a452c99378`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4883af93add6aae279fee4649bdd1d9a995335a7b6cd56571e0ede5cfa3c90`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 7.6 MB (7576745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62f433a9dc52cc27e53173033688da9385d89f33f61dd1e46616b648cfff9`  
		Last Modified: Thu, 02 Oct 2025 02:24:49 GMT  
		Size: 176.7 MB (176677340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef118ea534c5f67e1733824d0cd7a13aaba75dc7bb545ce03afab3286467ca5`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4bec4fdc4dd175e242482d8672c5c8afd4a7fc3fa304e09269fae978f4c184`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91de072e68e8b01b4fd9357d35930c646ef7ccc02b54c6c03ce76759ec1818`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769598cb0247656c5f52149dd01b09b949dd69468ce37a3cfb5e98734203a77`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ca6509233f0226292153cc6fcbd7220b85bda4fae17c3f358a26ab50d72a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf4e7ea6c71047f751747bf2ab58a259474d110a32215457e7662746ac40a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b22bc64f6f1857003da985a561708f816fe8b2ef5b91efe7f618f012e9f0ab`

```dockerfile
```

-	Layers:
	-	`sha256:bf39405f3719575281fce885837c911be2e82299da903bf952b3b3da3de8edf3`  
		Last Modified: Thu, 02 Oct 2025 03:50:05 GMT  
		Size: 26.9 KB (26908 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.7`

```console
$ docker pull clickhouse@sha256:613890f20c8128e9800d8b84abe50da018738af10db4852f86def606fe81de8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.7` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.7` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45284e11c1916b8d698c58fd4b1846a5cc479def5c671dc893ba67141b54ee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048d65318933af6af4c7e2790f9c3383163df5fa896bbbf80fd440a452c99378`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4883af93add6aae279fee4649bdd1d9a995335a7b6cd56571e0ede5cfa3c90`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 7.6 MB (7576745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62f433a9dc52cc27e53173033688da9385d89f33f61dd1e46616b648cfff9`  
		Last Modified: Thu, 02 Oct 2025 02:24:49 GMT  
		Size: 176.7 MB (176677340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef118ea534c5f67e1733824d0cd7a13aaba75dc7bb545ce03afab3286467ca5`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4bec4fdc4dd175e242482d8672c5c8afd4a7fc3fa304e09269fae978f4c184`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91de072e68e8b01b4fd9357d35930c646ef7ccc02b54c6c03ce76759ec1818`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769598cb0247656c5f52149dd01b09b949dd69468ce37a3cfb5e98734203a77`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ca6509233f0226292153cc6fcbd7220b85bda4fae17c3f358a26ab50d72a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.7` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf4e7ea6c71047f751747bf2ab58a259474d110a32215457e7662746ac40a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b22bc64f6f1857003da985a561708f816fe8b2ef5b91efe7f618f012e9f0ab`

```dockerfile
```

-	Layers:
	-	`sha256:bf39405f3719575281fce885837c911be2e82299da903bf952b3b3da3de8edf3`  
		Last Modified: Thu, 02 Oct 2025 03:50:05 GMT  
		Size: 26.9 KB (26908 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.7-jammy`

```console
$ docker pull clickhouse@sha256:613890f20c8128e9800d8b84abe50da018738af10db4852f86def606fe81de8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.7-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.7-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45284e11c1916b8d698c58fd4b1846a5cc479def5c671dc893ba67141b54ee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048d65318933af6af4c7e2790f9c3383163df5fa896bbbf80fd440a452c99378`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4883af93add6aae279fee4649bdd1d9a995335a7b6cd56571e0ede5cfa3c90`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 7.6 MB (7576745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62f433a9dc52cc27e53173033688da9385d89f33f61dd1e46616b648cfff9`  
		Last Modified: Thu, 02 Oct 2025 02:24:49 GMT  
		Size: 176.7 MB (176677340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef118ea534c5f67e1733824d0cd7a13aaba75dc7bb545ce03afab3286467ca5`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4bec4fdc4dd175e242482d8672c5c8afd4a7fc3fa304e09269fae978f4c184`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91de072e68e8b01b4fd9357d35930c646ef7ccc02b54c6c03ce76759ec1818`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769598cb0247656c5f52149dd01b09b949dd69468ce37a3cfb5e98734203a77`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ca6509233f0226292153cc6fcbd7220b85bda4fae17c3f358a26ab50d72a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.7-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf4e7ea6c71047f751747bf2ab58a259474d110a32215457e7662746ac40a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b22bc64f6f1857003da985a561708f816fe8b2ef5b91efe7f618f012e9f0ab`

```dockerfile
```

-	Layers:
	-	`sha256:bf39405f3719575281fce885837c911be2e82299da903bf952b3b3da3de8edf3`  
		Last Modified: Thu, 02 Oct 2025 03:50:05 GMT  
		Size: 26.9 KB (26908 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.7.3`

```console
$ docker pull clickhouse@sha256:613890f20c8128e9800d8b84abe50da018738af10db4852f86def606fe81de8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.7.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.7.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.7.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45284e11c1916b8d698c58fd4b1846a5cc479def5c671dc893ba67141b54ee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048d65318933af6af4c7e2790f9c3383163df5fa896bbbf80fd440a452c99378`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4883af93add6aae279fee4649bdd1d9a995335a7b6cd56571e0ede5cfa3c90`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 7.6 MB (7576745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62f433a9dc52cc27e53173033688da9385d89f33f61dd1e46616b648cfff9`  
		Last Modified: Thu, 02 Oct 2025 02:24:49 GMT  
		Size: 176.7 MB (176677340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef118ea534c5f67e1733824d0cd7a13aaba75dc7bb545ce03afab3286467ca5`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4bec4fdc4dd175e242482d8672c5c8afd4a7fc3fa304e09269fae978f4c184`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91de072e68e8b01b4fd9357d35930c646ef7ccc02b54c6c03ce76759ec1818`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769598cb0247656c5f52149dd01b09b949dd69468ce37a3cfb5e98734203a77`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ca6509233f0226292153cc6fcbd7220b85bda4fae17c3f358a26ab50d72a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.7.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf4e7ea6c71047f751747bf2ab58a259474d110a32215457e7662746ac40a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b22bc64f6f1857003da985a561708f816fe8b2ef5b91efe7f618f012e9f0ab`

```dockerfile
```

-	Layers:
	-	`sha256:bf39405f3719575281fce885837c911be2e82299da903bf952b3b3da3de8edf3`  
		Last Modified: Thu, 02 Oct 2025 03:50:05 GMT  
		Size: 26.9 KB (26908 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.7.3-jammy`

```console
$ docker pull clickhouse@sha256:613890f20c8128e9800d8b84abe50da018738af10db4852f86def606fe81de8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.7.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.7.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.7.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45284e11c1916b8d698c58fd4b1846a5cc479def5c671dc893ba67141b54ee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048d65318933af6af4c7e2790f9c3383163df5fa896bbbf80fd440a452c99378`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4883af93add6aae279fee4649bdd1d9a995335a7b6cd56571e0ede5cfa3c90`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 7.6 MB (7576745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62f433a9dc52cc27e53173033688da9385d89f33f61dd1e46616b648cfff9`  
		Last Modified: Thu, 02 Oct 2025 02:24:49 GMT  
		Size: 176.7 MB (176677340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef118ea534c5f67e1733824d0cd7a13aaba75dc7bb545ce03afab3286467ca5`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4bec4fdc4dd175e242482d8672c5c8afd4a7fc3fa304e09269fae978f4c184`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91de072e68e8b01b4fd9357d35930c646ef7ccc02b54c6c03ce76759ec1818`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769598cb0247656c5f52149dd01b09b949dd69468ce37a3cfb5e98734203a77`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ca6509233f0226292153cc6fcbd7220b85bda4fae17c3f358a26ab50d72a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.7.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf4e7ea6c71047f751747bf2ab58a259474d110a32215457e7662746ac40a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b22bc64f6f1857003da985a561708f816fe8b2ef5b91efe7f618f012e9f0ab`

```dockerfile
```

-	Layers:
	-	`sha256:bf39405f3719575281fce885837c911be2e82299da903bf952b3b3da3de8edf3`  
		Last Modified: Thu, 02 Oct 2025 03:50:05 GMT  
		Size: 26.9 KB (26908 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:613890f20c8128e9800d8b84abe50da018738af10db4852f86def606fe81de8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45284e11c1916b8d698c58fd4b1846a5cc479def5c671dc893ba67141b54ee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048d65318933af6af4c7e2790f9c3383163df5fa896bbbf80fd440a452c99378`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4883af93add6aae279fee4649bdd1d9a995335a7b6cd56571e0ede5cfa3c90`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 7.6 MB (7576745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62f433a9dc52cc27e53173033688da9385d89f33f61dd1e46616b648cfff9`  
		Last Modified: Thu, 02 Oct 2025 02:24:49 GMT  
		Size: 176.7 MB (176677340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef118ea534c5f67e1733824d0cd7a13aaba75dc7bb545ce03afab3286467ca5`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4bec4fdc4dd175e242482d8672c5c8afd4a7fc3fa304e09269fae978f4c184`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91de072e68e8b01b4fd9357d35930c646ef7ccc02b54c6c03ce76759ec1818`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769598cb0247656c5f52149dd01b09b949dd69468ce37a3cfb5e98734203a77`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ca6509233f0226292153cc6fcbd7220b85bda4fae17c3f358a26ab50d72a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf4e7ea6c71047f751747bf2ab58a259474d110a32215457e7662746ac40a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b22bc64f6f1857003da985a561708f816fe8b2ef5b91efe7f618f012e9f0ab`

```dockerfile
```

-	Layers:
	-	`sha256:bf39405f3719575281fce885837c911be2e82299da903bf952b3b3da3de8edf3`  
		Last Modified: Thu, 02 Oct 2025 03:50:05 GMT  
		Size: 26.9 KB (26908 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:613890f20c8128e9800d8b84abe50da018738af10db4852f86def606fe81de8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45284e11c1916b8d698c58fd4b1846a5cc479def5c671dc893ba67141b54ee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048d65318933af6af4c7e2790f9c3383163df5fa896bbbf80fd440a452c99378`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4883af93add6aae279fee4649bdd1d9a995335a7b6cd56571e0ede5cfa3c90`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 7.6 MB (7576745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62f433a9dc52cc27e53173033688da9385d89f33f61dd1e46616b648cfff9`  
		Last Modified: Thu, 02 Oct 2025 02:24:49 GMT  
		Size: 176.7 MB (176677340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef118ea534c5f67e1733824d0cd7a13aaba75dc7bb545ce03afab3286467ca5`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4bec4fdc4dd175e242482d8672c5c8afd4a7fc3fa304e09269fae978f4c184`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91de072e68e8b01b4fd9357d35930c646ef7ccc02b54c6c03ce76759ec1818`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769598cb0247656c5f52149dd01b09b949dd69468ce37a3cfb5e98734203a77`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ca6509233f0226292153cc6fcbd7220b85bda4fae17c3f358a26ab50d72a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf4e7ea6c71047f751747bf2ab58a259474d110a32215457e7662746ac40a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b22bc64f6f1857003da985a561708f816fe8b2ef5b91efe7f618f012e9f0ab`

```dockerfile
```

-	Layers:
	-	`sha256:bf39405f3719575281fce885837c911be2e82299da903bf952b3b3da3de8edf3`  
		Last Modified: Thu, 02 Oct 2025 03:50:05 GMT  
		Size: 26.9 KB (26908 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:613890f20c8128e9800d8b84abe50da018738af10db4852f86def606fe81de8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45284e11c1916b8d698c58fd4b1846a5cc479def5c671dc893ba67141b54ee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048d65318933af6af4c7e2790f9c3383163df5fa896bbbf80fd440a452c99378`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4883af93add6aae279fee4649bdd1d9a995335a7b6cd56571e0ede5cfa3c90`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 7.6 MB (7576745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62f433a9dc52cc27e53173033688da9385d89f33f61dd1e46616b648cfff9`  
		Last Modified: Thu, 02 Oct 2025 02:24:49 GMT  
		Size: 176.7 MB (176677340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef118ea534c5f67e1733824d0cd7a13aaba75dc7bb545ce03afab3286467ca5`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4bec4fdc4dd175e242482d8672c5c8afd4a7fc3fa304e09269fae978f4c184`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91de072e68e8b01b4fd9357d35930c646ef7ccc02b54c6c03ce76759ec1818`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769598cb0247656c5f52149dd01b09b949dd69468ce37a3cfb5e98734203a77`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ca6509233f0226292153cc6fcbd7220b85bda4fae17c3f358a26ab50d72a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf4e7ea6c71047f751747bf2ab58a259474d110a32215457e7662746ac40a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b22bc64f6f1857003da985a561708f816fe8b2ef5b91efe7f618f012e9f0ab`

```dockerfile
```

-	Layers:
	-	`sha256:bf39405f3719575281fce885837c911be2e82299da903bf952b3b3da3de8edf3`  
		Last Modified: Thu, 02 Oct 2025 03:50:05 GMT  
		Size: 26.9 KB (26908 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:613890f20c8128e9800d8b84abe50da018738af10db4852f86def606fe81de8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:af3aef7502fa1c8a5598030c3efd562cc9d1c2f7098d05d5bdf998f2b841bac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227759917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407e4509f562e8b0351a5f719f3f0cf025f6cb227639ba3410be5f1a579e3de6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580422714323634b611a3fb8e44e73f8afecca28874ed636a4da68d011d04a33`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 7.6 MB (7598477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acdb8ce9ea1d3e217a551662c8d886f0e4e75c384b8d756c20afca3133128d5`  
		Last Modified: Thu, 25 Sep 2025 17:39:58 GMT  
		Size: 189.8 MB (189754480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b93ce6e1cd16537660e7a840cefd7288af66f50e29520da80812db8a96f859f`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4a142b373583cac3d6ff628ab96cc5ce62dcc20634182cc35ffe189f5ecbd6`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853a8448be63a282281b7d3532179b999e06c71f71193ace44ca7663e7ac7f3`  
		Last Modified: Thu, 25 Sep 2025 17:39:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bb954bdec7066f13486a0ee79ae48235e89cb9541bc29e1df89d91321fd145`  
		Last Modified: Thu, 25 Sep 2025 17:39:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a09584ea34ca452b5835dbfa91afae8b438ec674592e458a5591be2bb02594c`  
		Last Modified: Thu, 25 Sep 2025 17:39:46 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:78442cad9b27dabbdd92a482c474550fdd5495a71428c3c78692bb8d987b1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cca2e460a8c84fb617d84a2f865422b2d5f4876871eccdb119782d3d04f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:e77fe48b80219b8db20edf27d679ad5f5e267f5698627fccfc280d4d982be475`  
		Last Modified: Thu, 25 Sep 2025 18:49:46 GMT  
		Size: 26.7 KB (26671 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:45284e11c1916b8d698c58fd4b1846a5cc479def5c671dc893ba67141b54ee6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212507218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048d65318933af6af4c7e2790f9c3383163df5fa896bbbf80fd440a452c99378`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 25 Sep 2025 16:06:42 GMT
ARG RELEASE
# Thu, 25 Sep 2025 16:06:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 25 Sep 2025 16:06:42 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 25 Sep 2025 16:06:42 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Thu, 25 Sep 2025 16:06:42 GMT
CMD ["/bin/bash"]
# Thu, 25 Sep 2025 16:06:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 25 Sep 2025 16:06:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPO_CHANNEL=stable
# Thu, 25 Sep 2025 16:06:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 25 Sep 2025 16:06:42 GMT
ARG VERSION=25.8.7.3
# Thu, 25 Sep 2025 16:06:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
ENV LANG=en_US.UTF-8
# Thu, 25 Sep 2025 16:06:42 GMT
ENV TZ=UTC
# Thu, 25 Sep 2025 16:06:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.7.3 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 25 Sep 2025 16:06:42 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 25 Sep 2025 16:06:42 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 25 Sep 2025 16:06:42 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 25 Sep 2025 16:06:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4883af93add6aae279fee4649bdd1d9a995335a7b6cd56571e0ede5cfa3c90`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 7.6 MB (7576745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c62f433a9dc52cc27e53173033688da9385d89f33f61dd1e46616b648cfff9`  
		Last Modified: Thu, 02 Oct 2025 02:24:49 GMT  
		Size: 176.7 MB (176677340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef118ea534c5f67e1733824d0cd7a13aaba75dc7bb545ce03afab3286467ca5`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4bec4fdc4dd175e242482d8672c5c8afd4a7fc3fa304e09269fae978f4c184`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c91de072e68e8b01b4fd9357d35930c646ef7ccc02b54c6c03ce76759ec1818`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769598cb0247656c5f52149dd01b09b949dd69468ce37a3cfb5e98734203a77`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d3ca6509233f0226292153cc6fcbd7220b85bda4fae17c3f358a26ab50d72a3`  
		Last Modified: Thu, 02 Oct 2025 01:12:03 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bf4e7ea6c71047f751747bf2ab58a259474d110a32215457e7662746ac40a5d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 KB (26908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b22bc64f6f1857003da985a561708f816fe8b2ef5b91efe7f618f012e9f0ab`

```dockerfile
```

-	Layers:
	-	`sha256:bf39405f3719575281fce885837c911be2e82299da903bf952b3b3da3de8edf3`  
		Last Modified: Thu, 02 Oct 2025 03:50:05 GMT  
		Size: 26.9 KB (26908 bytes)  
		MIME: application/vnd.in-toto+json
