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
$ docker pull clickhouse@sha256:61e2c3dc4f6f92875785d9d0d5d168c0402ea609c00bd3a0fd535e82d4843d6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e92a9071a611fccc4c4c415b7214ad92813181e147af8cc486894720f3afd33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e931015e63e8237a90fada2a75f9cf799b3399ddfa2a879df60aceb21548bb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 19:04:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:04:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:04:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:04:31 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:04:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:05:03 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:05:03 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:05:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:05:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d11e76d92b34ca2464f06f1b5534c1aa658d18d79e601066da972b4a1b3b7b3`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 7.6 MB (7598327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649e6603f1eab422eabdb13a7684d8e8eb59bef8065e76adcff47137797b1444`  
		Last Modified: Thu, 29 Jan 2026 19:05:29 GMT  
		Size: 195.9 MB (195939032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5eb377013db6e9a55b6b1d07c161a5b38c493729077ef5408b3af1adf17a6c`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b824c2d000aba73ff75fef879c5325cf964868266223722746a961906352704`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786f9fe942aed3143da3638aa087e87f6d96c2c3bfb5bcdef9311d699cf8da0b`  
		Last Modified: Thu, 29 Jan 2026 19:05:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b008c17e29348bae5a7da8be1d543ed82924460798b03b25ef874b15f4c319`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5220fa191a03d2acf360d6d055f57068f5f06f949249ab1f3d9d3f27876e682e`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cad9f57dd3a535d9042d690bd517fe86f3cad9eea324dc2bf65e640852d6f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdce8a029e31639f194a5a9c1c8983a2f74b8ed1f83f9fee140b062e6f035a39`

```dockerfile
```

-	Layers:
	-	`sha256:6d62cd70bb44488b3a347f824b78f2be0d48d1638ca732ff1fc388042995ca1f`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7ea311837e3961aa54b5ab571507611e61dd1fe94d00e63a5f2e058d829a2cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0e8981818491b5bd0bae6592187f9efa21b4c2a33a5742173a0ed1d6faa4da`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 19:03:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:03:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:03:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:03:38 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:03:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:04:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:04:09 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:04:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:04:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:04:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af18034197a8d45f44376dad38bbb78919a069d422a6af988ca7233156d5ef8d`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 7.6 MB (7577347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac5ddae9718e96f67a48fdbdac14adeb61d0d80600a52d8d967fe16a846e84f`  
		Last Modified: Thu, 29 Jan 2026 19:04:31 GMT  
		Size: 183.0 MB (182997150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb14d7324a75d7ff8aae8a38e2662f4b97bbd60187f621f58588d069a8fb8f`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4372dfa16d58d7c8950abf7bd1cd5a6661aadc8e12440e5d93d82143c6a3ed`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f5d92dd9113ccba5dc52767a85ec37f5440a1fc87bc3dcb8ba379859e726ff`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d725d747cbb30582656472c52713e1ac6bdc4e202ce8462a3f8cf484281f424d`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea767d8cb96970dcf22eb1242cdcf9ade4048b816d69275431300deb81936504`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b99049cd701b8281f4f39587651069368457c20284a595f6f693169dbe08a599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39034a13d817e59a13dabf1d8387fa3828cd3d196b235ed43ce6628382ad3f37`

```dockerfile
```

-	Layers:
	-	`sha256:0ccb4d668478efc07fe1420466ad6ef0a4c07e9513c134a0646f67902a853eb9`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11-jammy`

```console
$ docker pull clickhouse@sha256:61e2c3dc4f6f92875785d9d0d5d168c0402ea609c00bd3a0fd535e82d4843d6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e92a9071a611fccc4c4c415b7214ad92813181e147af8cc486894720f3afd33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e931015e63e8237a90fada2a75f9cf799b3399ddfa2a879df60aceb21548bb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 19:04:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:04:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:04:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:04:31 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:04:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:05:03 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:05:03 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:05:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:05:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d11e76d92b34ca2464f06f1b5534c1aa658d18d79e601066da972b4a1b3b7b3`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 7.6 MB (7598327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649e6603f1eab422eabdb13a7684d8e8eb59bef8065e76adcff47137797b1444`  
		Last Modified: Thu, 29 Jan 2026 19:05:29 GMT  
		Size: 195.9 MB (195939032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5eb377013db6e9a55b6b1d07c161a5b38c493729077ef5408b3af1adf17a6c`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b824c2d000aba73ff75fef879c5325cf964868266223722746a961906352704`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786f9fe942aed3143da3638aa087e87f6d96c2c3bfb5bcdef9311d699cf8da0b`  
		Last Modified: Thu, 29 Jan 2026 19:05:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b008c17e29348bae5a7da8be1d543ed82924460798b03b25ef874b15f4c319`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5220fa191a03d2acf360d6d055f57068f5f06f949249ab1f3d9d3f27876e682e`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cad9f57dd3a535d9042d690bd517fe86f3cad9eea324dc2bf65e640852d6f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdce8a029e31639f194a5a9c1c8983a2f74b8ed1f83f9fee140b062e6f035a39`

```dockerfile
```

-	Layers:
	-	`sha256:6d62cd70bb44488b3a347f824b78f2be0d48d1638ca732ff1fc388042995ca1f`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7ea311837e3961aa54b5ab571507611e61dd1fe94d00e63a5f2e058d829a2cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0e8981818491b5bd0bae6592187f9efa21b4c2a33a5742173a0ed1d6faa4da`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 19:03:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:03:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:03:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:03:38 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:03:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:04:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:04:09 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:04:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:04:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:04:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af18034197a8d45f44376dad38bbb78919a069d422a6af988ca7233156d5ef8d`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 7.6 MB (7577347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac5ddae9718e96f67a48fdbdac14adeb61d0d80600a52d8d967fe16a846e84f`  
		Last Modified: Thu, 29 Jan 2026 19:04:31 GMT  
		Size: 183.0 MB (182997150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb14d7324a75d7ff8aae8a38e2662f4b97bbd60187f621f58588d069a8fb8f`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4372dfa16d58d7c8950abf7bd1cd5a6661aadc8e12440e5d93d82143c6a3ed`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f5d92dd9113ccba5dc52767a85ec37f5440a1fc87bc3dcb8ba379859e726ff`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d725d747cbb30582656472c52713e1ac6bdc4e202ce8462a3f8cf484281f424d`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea767d8cb96970dcf22eb1242cdcf9ade4048b816d69275431300deb81936504`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b99049cd701b8281f4f39587651069368457c20284a595f6f693169dbe08a599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39034a13d817e59a13dabf1d8387fa3828cd3d196b235ed43ce6628382ad3f37`

```dockerfile
```

-	Layers:
	-	`sha256:0ccb4d668478efc07fe1420466ad6ef0a4c07e9513c134a0646f67902a853eb9`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.8`

```console
$ docker pull clickhouse@sha256:61e2c3dc4f6f92875785d9d0d5d168c0402ea609c00bd3a0fd535e82d4843d6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e92a9071a611fccc4c4c415b7214ad92813181e147af8cc486894720f3afd33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e931015e63e8237a90fada2a75f9cf799b3399ddfa2a879df60aceb21548bb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 19:04:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:04:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:04:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:04:31 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:04:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:05:03 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:05:03 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:05:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:05:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d11e76d92b34ca2464f06f1b5534c1aa658d18d79e601066da972b4a1b3b7b3`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 7.6 MB (7598327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649e6603f1eab422eabdb13a7684d8e8eb59bef8065e76adcff47137797b1444`  
		Last Modified: Thu, 29 Jan 2026 19:05:29 GMT  
		Size: 195.9 MB (195939032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5eb377013db6e9a55b6b1d07c161a5b38c493729077ef5408b3af1adf17a6c`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b824c2d000aba73ff75fef879c5325cf964868266223722746a961906352704`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786f9fe942aed3143da3638aa087e87f6d96c2c3bfb5bcdef9311d699cf8da0b`  
		Last Modified: Thu, 29 Jan 2026 19:05:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b008c17e29348bae5a7da8be1d543ed82924460798b03b25ef874b15f4c319`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5220fa191a03d2acf360d6d055f57068f5f06f949249ab1f3d9d3f27876e682e`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cad9f57dd3a535d9042d690bd517fe86f3cad9eea324dc2bf65e640852d6f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdce8a029e31639f194a5a9c1c8983a2f74b8ed1f83f9fee140b062e6f035a39`

```dockerfile
```

-	Layers:
	-	`sha256:6d62cd70bb44488b3a347f824b78f2be0d48d1638ca732ff1fc388042995ca1f`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7ea311837e3961aa54b5ab571507611e61dd1fe94d00e63a5f2e058d829a2cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0e8981818491b5bd0bae6592187f9efa21b4c2a33a5742173a0ed1d6faa4da`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 19:03:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:03:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:03:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:03:38 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:03:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:04:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:04:09 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:04:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:04:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:04:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af18034197a8d45f44376dad38bbb78919a069d422a6af988ca7233156d5ef8d`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 7.6 MB (7577347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac5ddae9718e96f67a48fdbdac14adeb61d0d80600a52d8d967fe16a846e84f`  
		Last Modified: Thu, 29 Jan 2026 19:04:31 GMT  
		Size: 183.0 MB (182997150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb14d7324a75d7ff8aae8a38e2662f4b97bbd60187f621f58588d069a8fb8f`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4372dfa16d58d7c8950abf7bd1cd5a6661aadc8e12440e5d93d82143c6a3ed`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f5d92dd9113ccba5dc52767a85ec37f5440a1fc87bc3dcb8ba379859e726ff`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d725d747cbb30582656472c52713e1ac6bdc4e202ce8462a3f8cf484281f424d`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea767d8cb96970dcf22eb1242cdcf9ade4048b816d69275431300deb81936504`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b99049cd701b8281f4f39587651069368457c20284a595f6f693169dbe08a599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39034a13d817e59a13dabf1d8387fa3828cd3d196b235ed43ce6628382ad3f37`

```dockerfile
```

-	Layers:
	-	`sha256:0ccb4d668478efc07fe1420466ad6ef0a4c07e9513c134a0646f67902a853eb9`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.8-jammy`

```console
$ docker pull clickhouse@sha256:61e2c3dc4f6f92875785d9d0d5d168c0402ea609c00bd3a0fd535e82d4843d6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e92a9071a611fccc4c4c415b7214ad92813181e147af8cc486894720f3afd33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e931015e63e8237a90fada2a75f9cf799b3399ddfa2a879df60aceb21548bb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 19:04:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:04:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:04:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:04:31 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:04:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:05:03 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:05:03 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:05:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:05:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d11e76d92b34ca2464f06f1b5534c1aa658d18d79e601066da972b4a1b3b7b3`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 7.6 MB (7598327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649e6603f1eab422eabdb13a7684d8e8eb59bef8065e76adcff47137797b1444`  
		Last Modified: Thu, 29 Jan 2026 19:05:29 GMT  
		Size: 195.9 MB (195939032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5eb377013db6e9a55b6b1d07c161a5b38c493729077ef5408b3af1adf17a6c`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b824c2d000aba73ff75fef879c5325cf964868266223722746a961906352704`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786f9fe942aed3143da3638aa087e87f6d96c2c3bfb5bcdef9311d699cf8da0b`  
		Last Modified: Thu, 29 Jan 2026 19:05:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b008c17e29348bae5a7da8be1d543ed82924460798b03b25ef874b15f4c319`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5220fa191a03d2acf360d6d055f57068f5f06f949249ab1f3d9d3f27876e682e`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cad9f57dd3a535d9042d690bd517fe86f3cad9eea324dc2bf65e640852d6f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdce8a029e31639f194a5a9c1c8983a2f74b8ed1f83f9fee140b062e6f035a39`

```dockerfile
```

-	Layers:
	-	`sha256:6d62cd70bb44488b3a347f824b78f2be0d48d1638ca732ff1fc388042995ca1f`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7ea311837e3961aa54b5ab571507611e61dd1fe94d00e63a5f2e058d829a2cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0e8981818491b5bd0bae6592187f9efa21b4c2a33a5742173a0ed1d6faa4da`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 19:03:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:03:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:03:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:03:38 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:03:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:04:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:04:09 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:04:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:04:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:04:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af18034197a8d45f44376dad38bbb78919a069d422a6af988ca7233156d5ef8d`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 7.6 MB (7577347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac5ddae9718e96f67a48fdbdac14adeb61d0d80600a52d8d967fe16a846e84f`  
		Last Modified: Thu, 29 Jan 2026 19:04:31 GMT  
		Size: 183.0 MB (182997150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb14d7324a75d7ff8aae8a38e2662f4b97bbd60187f621f58588d069a8fb8f`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4372dfa16d58d7c8950abf7bd1cd5a6661aadc8e12440e5d93d82143c6a3ed`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f5d92dd9113ccba5dc52767a85ec37f5440a1fc87bc3dcb8ba379859e726ff`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d725d747cbb30582656472c52713e1ac6bdc4e202ce8462a3f8cf484281f424d`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea767d8cb96970dcf22eb1242cdcf9ade4048b816d69275431300deb81936504`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b99049cd701b8281f4f39587651069368457c20284a595f6f693169dbe08a599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39034a13d817e59a13dabf1d8387fa3828cd3d196b235ed43ce6628382ad3f37`

```dockerfile
```

-	Layers:
	-	`sha256:0ccb4d668478efc07fe1420466ad6ef0a4c07e9513c134a0646f67902a853eb9`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.8.25`

```console
$ docker pull clickhouse@sha256:61e2c3dc4f6f92875785d9d0d5d168c0402ea609c00bd3a0fd535e82d4843d6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.8.25` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e92a9071a611fccc4c4c415b7214ad92813181e147af8cc486894720f3afd33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e931015e63e8237a90fada2a75f9cf799b3399ddfa2a879df60aceb21548bb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 19:04:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:04:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:04:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:04:31 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:04:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:05:03 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:05:03 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:05:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:05:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d11e76d92b34ca2464f06f1b5534c1aa658d18d79e601066da972b4a1b3b7b3`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 7.6 MB (7598327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649e6603f1eab422eabdb13a7684d8e8eb59bef8065e76adcff47137797b1444`  
		Last Modified: Thu, 29 Jan 2026 19:05:29 GMT  
		Size: 195.9 MB (195939032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5eb377013db6e9a55b6b1d07c161a5b38c493729077ef5408b3af1adf17a6c`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b824c2d000aba73ff75fef879c5325cf964868266223722746a961906352704`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786f9fe942aed3143da3638aa087e87f6d96c2c3bfb5bcdef9311d699cf8da0b`  
		Last Modified: Thu, 29 Jan 2026 19:05:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b008c17e29348bae5a7da8be1d543ed82924460798b03b25ef874b15f4c319`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5220fa191a03d2acf360d6d055f57068f5f06f949249ab1f3d9d3f27876e682e`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8.25` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cad9f57dd3a535d9042d690bd517fe86f3cad9eea324dc2bf65e640852d6f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdce8a029e31639f194a5a9c1c8983a2f74b8ed1f83f9fee140b062e6f035a39`

```dockerfile
```

-	Layers:
	-	`sha256:6d62cd70bb44488b3a347f824b78f2be0d48d1638ca732ff1fc388042995ca1f`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.8.25` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7ea311837e3961aa54b5ab571507611e61dd1fe94d00e63a5f2e058d829a2cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0e8981818491b5bd0bae6592187f9efa21b4c2a33a5742173a0ed1d6faa4da`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 19:03:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:03:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:03:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:03:38 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:03:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:04:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:04:09 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:04:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:04:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:04:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af18034197a8d45f44376dad38bbb78919a069d422a6af988ca7233156d5ef8d`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 7.6 MB (7577347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac5ddae9718e96f67a48fdbdac14adeb61d0d80600a52d8d967fe16a846e84f`  
		Last Modified: Thu, 29 Jan 2026 19:04:31 GMT  
		Size: 183.0 MB (182997150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb14d7324a75d7ff8aae8a38e2662f4b97bbd60187f621f58588d069a8fb8f`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4372dfa16d58d7c8950abf7bd1cd5a6661aadc8e12440e5d93d82143c6a3ed`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f5d92dd9113ccba5dc52767a85ec37f5440a1fc87bc3dcb8ba379859e726ff`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d725d747cbb30582656472c52713e1ac6bdc4e202ce8462a3f8cf484281f424d`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea767d8cb96970dcf22eb1242cdcf9ade4048b816d69275431300deb81936504`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8.25` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b99049cd701b8281f4f39587651069368457c20284a595f6f693169dbe08a599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39034a13d817e59a13dabf1d8387fa3828cd3d196b235ed43ce6628382ad3f37`

```dockerfile
```

-	Layers:
	-	`sha256:0ccb4d668478efc07fe1420466ad6ef0a4c07e9513c134a0646f67902a853eb9`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.11.8.25-jammy`

```console
$ docker pull clickhouse@sha256:61e2c3dc4f6f92875785d9d0d5d168c0402ea609c00bd3a0fd535e82d4843d6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.11.8.25-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:1e92a9071a611fccc4c4c415b7214ad92813181e147af8cc486894720f3afd33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233944074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2e931015e63e8237a90fada2a75f9cf799b3399ddfa2a879df60aceb21548bb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 19:04:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:04:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:04:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:04:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:04:31 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:04:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:01 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:05:03 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:05:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:05:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:05:03 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:05:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:05:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d11e76d92b34ca2464f06f1b5534c1aa658d18d79e601066da972b4a1b3b7b3`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 7.6 MB (7598327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649e6603f1eab422eabdb13a7684d8e8eb59bef8065e76adcff47137797b1444`  
		Last Modified: Thu, 29 Jan 2026 19:05:29 GMT  
		Size: 195.9 MB (195939032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5eb377013db6e9a55b6b1d07c161a5b38c493729077ef5408b3af1adf17a6c`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 184.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b824c2d000aba73ff75fef879c5325cf964868266223722746a961906352704`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786f9fe942aed3143da3638aa087e87f6d96c2c3bfb5bcdef9311d699cf8da0b`  
		Last Modified: Thu, 29 Jan 2026 19:05:26 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b008c17e29348bae5a7da8be1d543ed82924460798b03b25ef874b15f4c319`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5220fa191a03d2acf360d6d055f57068f5f06f949249ab1f3d9d3f27876e682e`  
		Last Modified: Thu, 29 Jan 2026 19:05:27 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8.25-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:3cad9f57dd3a535d9042d690bd517fe86f3cad9eea324dc2bf65e640852d6f0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdce8a029e31639f194a5a9c1c8983a2f74b8ed1f83f9fee140b062e6f035a39`

```dockerfile
```

-	Layers:
	-	`sha256:6d62cd70bb44488b3a347f824b78f2be0d48d1638ca732ff1fc388042995ca1f`  
		Last Modified: Thu, 29 Jan 2026 19:05:25 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.11.8.25-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:7ea311837e3961aa54b5ab571507611e61dd1fe94d00e63a5f2e058d829a2cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.8 MB (218828044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0e8981818491b5bd0bae6592187f9efa21b4c2a33a5742173a0ed1d6faa4da`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Thu, 29 Jan 2026 19:03:38 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 29 Jan 2026 19:03:38 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 29 Jan 2026 19:03:38 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPO_CHANNEL=stable
# Thu, 29 Jan 2026 19:03:38 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 29 Jan 2026 19:03:38 GMT
ARG VERSION=25.11.8.25
# Thu, 29 Jan 2026 19:03:38 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 29 Jan 2026 19:04:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:08 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
ENV LANG=en_US.UTF-8
# Thu, 29 Jan 2026 19:04:09 GMT
ENV TZ=UTC
# Thu, 29 Jan 2026 19:04:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.11.8.25 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 29 Jan 2026 19:04:09 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 29 Jan 2026 19:04:09 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 29 Jan 2026 19:04:09 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 29 Jan 2026 19:04:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af18034197a8d45f44376dad38bbb78919a069d422a6af988ca7233156d5ef8d`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 7.6 MB (7577347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac5ddae9718e96f67a48fdbdac14adeb61d0d80600a52d8d967fe16a846e84f`  
		Last Modified: Thu, 29 Jan 2026 19:04:31 GMT  
		Size: 183.0 MB (182997150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddb14d7324a75d7ff8aae8a38e2662f4b97bbd60187f621f58588d069a8fb8f`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4372dfa16d58d7c8950abf7bd1cd5a6661aadc8e12440e5d93d82143c6a3ed`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f5d92dd9113ccba5dc52767a85ec37f5440a1fc87bc3dcb8ba379859e726ff`  
		Last Modified: Thu, 29 Jan 2026 19:04:28 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d725d747cbb30582656472c52713e1ac6bdc4e202ce8462a3f8cf484281f424d`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea767d8cb96970dcf22eb1242cdcf9ade4048b816d69275431300deb81936504`  
		Last Modified: Thu, 29 Jan 2026 19:04:29 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.11.8.25-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b99049cd701b8281f4f39587651069368457c20284a595f6f693169dbe08a599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39034a13d817e59a13dabf1d8387fa3828cd3d196b235ed43ce6628382ad3f37`

```dockerfile
```

-	Layers:
	-	`sha256:0ccb4d668478efc07fe1420466ad6ef0a4c07e9513c134a0646f67902a853eb9`  
		Last Modified: Thu, 29 Jan 2026 19:04:27 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12`

```console
$ docker pull clickhouse@sha256:2c55b8abc96a804c895f903e85d093a32dfc2ec1c9060da59af36bd24210ff10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12` - linux; amd64

```console
$ docker pull clickhouse@sha256:f5d34c2ca9820776c5caa971f844a589d4a0ad514786bbc224da4fec0783e22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246336449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace786d945703abf2fdf5360b5c9ae7db6f6b2855023093413e33e3410033621`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:37 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:37 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:37 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:37 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:37 GMT
ARG VERSION=25.12.5.44
# Mon, 09 Feb 2026 19:25:37 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:06 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:06 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1bee7891ee835f80d9ea3c337f089e4d4c5c746d13dde6d3ebd5c323f0612c`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 7.6 MB (7598396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0ce0ee21c47da2b40262a15e02a854229ff848a8fcfb29925665f32cdf296f`  
		Last Modified: Mon, 09 Feb 2026 19:26:32 GMT  
		Size: 208.3 MB (208331334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2d133c574df0cfa824c641410e4ba1c3e447dcff2322d9a25ee98b59d37b71`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc605d5de901a7e6336a922f6622749645902592ca338541b241f1da57dffe3`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fa78aedd6caca205e01e65378a244180abd21e68ba16acdcd6015964fcc761`  
		Last Modified: Mon, 09 Feb 2026 19:26:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d8742747b7d384d0f5e4f8293974e93ee12cec36676898fcbd7e1f180bd488`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b5bd28bcc5dcbe897485cd139839c5dc64b5bb2d3b32b7f327ada02a64a69e`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6b62ce8043f679b87fa9e306a6ce5d31373b57827a4062a4c3773aa51f88631a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8087ec5a178b76c50bcdb326592d46d9131de528c2c8e8b3a2162d44afc591d2`

```dockerfile
```

-	Layers:
	-	`sha256:d7c47fc44bbb54311c32bd7a612f7046e0d37c86a5666ab69e1eefbe1945fa6a`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4b5799813306e3a8e767a12f0a58d48a80b6b2ea31e53c027815334eea03ecac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228262613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b21832377bb22afeddc7d892f945ac7a326fb555bbc4b7aa92fa0a775cfa2d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:24:53 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:24:53 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:24:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:24:53 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:24:53 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:24:53 GMT
ARG VERSION=25.12.5.44
# Mon, 09 Feb 2026 19:24:53 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:26 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:26 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:26 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c9a9191b66439b9052bc22174f4e8ae514813dc91db5af58426f4fe2e7f4`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 7.6 MB (7577458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d454d3ee4b48fdb02306c5ba2e17867990f78343ca4f4ba60ac03733ea64eef4`  
		Last Modified: Mon, 09 Feb 2026 19:25:52 GMT  
		Size: 192.4 MB (192431607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f3c6f6d4899efdcea0e71fa57f74380260076a9217d9aea9adc20657ebb761`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2b3cdde424a9f8f713cfa50e453023c9f4771d1ccd3b5910eebc7ea482a4ac`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96df76ae94980530a4e07de65b4f6cac1f24b7ff9b5842a1219134bdaa0a9ead`  
		Last Modified: Mon, 09 Feb 2026 19:25:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e7ae1561b7b40cde311537d5e0309440deff6a7f24f611bc184bda5f1d38bd`  
		Last Modified: Mon, 09 Feb 2026 19:25:50 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c37d7d4e5b47b4645aa14977cbdf0a7c21074a2fdf3482e3b3c0cb271abf80a`  
		Last Modified: Mon, 09 Feb 2026 19:25:50 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12` - unknown; unknown

```console
$ docker pull clickhouse@sha256:04310d0f8e7b6adc99ff7b0cc74284cae6303a4c2665b98ecb47e6a4eae6ba9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de48f9b6058f28fab4ec87d222d9bc99a75e6fc1a4190098219cc5155b166c5`

```dockerfile
```

-	Layers:
	-	`sha256:d78db083114a500e7280bf84a28004b52f269ca2f5d1bcc85dfc7aa7b751b34c`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12-jammy`

```console
$ docker pull clickhouse@sha256:2c55b8abc96a804c895f903e85d093a32dfc2ec1c9060da59af36bd24210ff10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f5d34c2ca9820776c5caa971f844a589d4a0ad514786bbc224da4fec0783e22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246336449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace786d945703abf2fdf5360b5c9ae7db6f6b2855023093413e33e3410033621`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:37 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:37 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:37 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:37 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:37 GMT
ARG VERSION=25.12.5.44
# Mon, 09 Feb 2026 19:25:37 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:06 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:06 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1bee7891ee835f80d9ea3c337f089e4d4c5c746d13dde6d3ebd5c323f0612c`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 7.6 MB (7598396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0ce0ee21c47da2b40262a15e02a854229ff848a8fcfb29925665f32cdf296f`  
		Last Modified: Mon, 09 Feb 2026 19:26:32 GMT  
		Size: 208.3 MB (208331334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2d133c574df0cfa824c641410e4ba1c3e447dcff2322d9a25ee98b59d37b71`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc605d5de901a7e6336a922f6622749645902592ca338541b241f1da57dffe3`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fa78aedd6caca205e01e65378a244180abd21e68ba16acdcd6015964fcc761`  
		Last Modified: Mon, 09 Feb 2026 19:26:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d8742747b7d384d0f5e4f8293974e93ee12cec36676898fcbd7e1f180bd488`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b5bd28bcc5dcbe897485cd139839c5dc64b5bb2d3b32b7f327ada02a64a69e`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6b62ce8043f679b87fa9e306a6ce5d31373b57827a4062a4c3773aa51f88631a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8087ec5a178b76c50bcdb326592d46d9131de528c2c8e8b3a2162d44afc591d2`

```dockerfile
```

-	Layers:
	-	`sha256:d7c47fc44bbb54311c32bd7a612f7046e0d37c86a5666ab69e1eefbe1945fa6a`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4b5799813306e3a8e767a12f0a58d48a80b6b2ea31e53c027815334eea03ecac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228262613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b21832377bb22afeddc7d892f945ac7a326fb555bbc4b7aa92fa0a775cfa2d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:24:53 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:24:53 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:24:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:24:53 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:24:53 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:24:53 GMT
ARG VERSION=25.12.5.44
# Mon, 09 Feb 2026 19:24:53 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:26 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:26 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:26 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c9a9191b66439b9052bc22174f4e8ae514813dc91db5af58426f4fe2e7f4`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 7.6 MB (7577458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d454d3ee4b48fdb02306c5ba2e17867990f78343ca4f4ba60ac03733ea64eef4`  
		Last Modified: Mon, 09 Feb 2026 19:25:52 GMT  
		Size: 192.4 MB (192431607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f3c6f6d4899efdcea0e71fa57f74380260076a9217d9aea9adc20657ebb761`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2b3cdde424a9f8f713cfa50e453023c9f4771d1ccd3b5910eebc7ea482a4ac`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96df76ae94980530a4e07de65b4f6cac1f24b7ff9b5842a1219134bdaa0a9ead`  
		Last Modified: Mon, 09 Feb 2026 19:25:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e7ae1561b7b40cde311537d5e0309440deff6a7f24f611bc184bda5f1d38bd`  
		Last Modified: Mon, 09 Feb 2026 19:25:50 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c37d7d4e5b47b4645aa14977cbdf0a7c21074a2fdf3482e3b3c0cb271abf80a`  
		Last Modified: Mon, 09 Feb 2026 19:25:50 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:04310d0f8e7b6adc99ff7b0cc74284cae6303a4c2665b98ecb47e6a4eae6ba9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de48f9b6058f28fab4ec87d222d9bc99a75e6fc1a4190098219cc5155b166c5`

```dockerfile
```

-	Layers:
	-	`sha256:d78db083114a500e7280bf84a28004b52f269ca2f5d1bcc85dfc7aa7b751b34c`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.5`

```console
$ docker pull clickhouse@sha256:2c55b8abc96a804c895f903e85d093a32dfc2ec1c9060da59af36bd24210ff10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.5` - linux; amd64

```console
$ docker pull clickhouse@sha256:f5d34c2ca9820776c5caa971f844a589d4a0ad514786bbc224da4fec0783e22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246336449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace786d945703abf2fdf5360b5c9ae7db6f6b2855023093413e33e3410033621`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:37 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:37 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:37 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:37 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:37 GMT
ARG VERSION=25.12.5.44
# Mon, 09 Feb 2026 19:25:37 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:06 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:06 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1bee7891ee835f80d9ea3c337f089e4d4c5c746d13dde6d3ebd5c323f0612c`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 7.6 MB (7598396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0ce0ee21c47da2b40262a15e02a854229ff848a8fcfb29925665f32cdf296f`  
		Last Modified: Mon, 09 Feb 2026 19:26:32 GMT  
		Size: 208.3 MB (208331334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2d133c574df0cfa824c641410e4ba1c3e447dcff2322d9a25ee98b59d37b71`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc605d5de901a7e6336a922f6622749645902592ca338541b241f1da57dffe3`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fa78aedd6caca205e01e65378a244180abd21e68ba16acdcd6015964fcc761`  
		Last Modified: Mon, 09 Feb 2026 19:26:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d8742747b7d384d0f5e4f8293974e93ee12cec36676898fcbd7e1f180bd488`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b5bd28bcc5dcbe897485cd139839c5dc64b5bb2d3b32b7f327ada02a64a69e`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6b62ce8043f679b87fa9e306a6ce5d31373b57827a4062a4c3773aa51f88631a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8087ec5a178b76c50bcdb326592d46d9131de528c2c8e8b3a2162d44afc591d2`

```dockerfile
```

-	Layers:
	-	`sha256:d7c47fc44bbb54311c32bd7a612f7046e0d37c86a5666ab69e1eefbe1945fa6a`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.5` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4b5799813306e3a8e767a12f0a58d48a80b6b2ea31e53c027815334eea03ecac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228262613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b21832377bb22afeddc7d892f945ac7a326fb555bbc4b7aa92fa0a775cfa2d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:24:53 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:24:53 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:24:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:24:53 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:24:53 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:24:53 GMT
ARG VERSION=25.12.5.44
# Mon, 09 Feb 2026 19:24:53 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:26 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:26 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:26 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c9a9191b66439b9052bc22174f4e8ae514813dc91db5af58426f4fe2e7f4`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 7.6 MB (7577458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d454d3ee4b48fdb02306c5ba2e17867990f78343ca4f4ba60ac03733ea64eef4`  
		Last Modified: Mon, 09 Feb 2026 19:25:52 GMT  
		Size: 192.4 MB (192431607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f3c6f6d4899efdcea0e71fa57f74380260076a9217d9aea9adc20657ebb761`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2b3cdde424a9f8f713cfa50e453023c9f4771d1ccd3b5910eebc7ea482a4ac`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96df76ae94980530a4e07de65b4f6cac1f24b7ff9b5842a1219134bdaa0a9ead`  
		Last Modified: Mon, 09 Feb 2026 19:25:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e7ae1561b7b40cde311537d5e0309440deff6a7f24f611bc184bda5f1d38bd`  
		Last Modified: Mon, 09 Feb 2026 19:25:50 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c37d7d4e5b47b4645aa14977cbdf0a7c21074a2fdf3482e3b3c0cb271abf80a`  
		Last Modified: Mon, 09 Feb 2026 19:25:50 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.5` - unknown; unknown

```console
$ docker pull clickhouse@sha256:04310d0f8e7b6adc99ff7b0cc74284cae6303a4c2665b98ecb47e6a4eae6ba9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de48f9b6058f28fab4ec87d222d9bc99a75e6fc1a4190098219cc5155b166c5`

```dockerfile
```

-	Layers:
	-	`sha256:d78db083114a500e7280bf84a28004b52f269ca2f5d1bcc85dfc7aa7b751b34c`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.5-jammy`

```console
$ docker pull clickhouse@sha256:2c55b8abc96a804c895f903e85d093a32dfc2ec1c9060da59af36bd24210ff10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.5-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f5d34c2ca9820776c5caa971f844a589d4a0ad514786bbc224da4fec0783e22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246336449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace786d945703abf2fdf5360b5c9ae7db6f6b2855023093413e33e3410033621`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:37 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:37 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:37 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:37 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:37 GMT
ARG VERSION=25.12.5.44
# Mon, 09 Feb 2026 19:25:37 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:06 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:06 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1bee7891ee835f80d9ea3c337f089e4d4c5c746d13dde6d3ebd5c323f0612c`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 7.6 MB (7598396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0ce0ee21c47da2b40262a15e02a854229ff848a8fcfb29925665f32cdf296f`  
		Last Modified: Mon, 09 Feb 2026 19:26:32 GMT  
		Size: 208.3 MB (208331334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2d133c574df0cfa824c641410e4ba1c3e447dcff2322d9a25ee98b59d37b71`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc605d5de901a7e6336a922f6622749645902592ca338541b241f1da57dffe3`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fa78aedd6caca205e01e65378a244180abd21e68ba16acdcd6015964fcc761`  
		Last Modified: Mon, 09 Feb 2026 19:26:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d8742747b7d384d0f5e4f8293974e93ee12cec36676898fcbd7e1f180bd488`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b5bd28bcc5dcbe897485cd139839c5dc64b5bb2d3b32b7f327ada02a64a69e`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6b62ce8043f679b87fa9e306a6ce5d31373b57827a4062a4c3773aa51f88631a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8087ec5a178b76c50bcdb326592d46d9131de528c2c8e8b3a2162d44afc591d2`

```dockerfile
```

-	Layers:
	-	`sha256:d7c47fc44bbb54311c32bd7a612f7046e0d37c86a5666ab69e1eefbe1945fa6a`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.5-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4b5799813306e3a8e767a12f0a58d48a80b6b2ea31e53c027815334eea03ecac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228262613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b21832377bb22afeddc7d892f945ac7a326fb555bbc4b7aa92fa0a775cfa2d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:24:53 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:24:53 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:24:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:24:53 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:24:53 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:24:53 GMT
ARG VERSION=25.12.5.44
# Mon, 09 Feb 2026 19:24:53 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:26 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:26 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:26 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c9a9191b66439b9052bc22174f4e8ae514813dc91db5af58426f4fe2e7f4`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 7.6 MB (7577458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d454d3ee4b48fdb02306c5ba2e17867990f78343ca4f4ba60ac03733ea64eef4`  
		Last Modified: Mon, 09 Feb 2026 19:25:52 GMT  
		Size: 192.4 MB (192431607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f3c6f6d4899efdcea0e71fa57f74380260076a9217d9aea9adc20657ebb761`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2b3cdde424a9f8f713cfa50e453023c9f4771d1ccd3b5910eebc7ea482a4ac`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96df76ae94980530a4e07de65b4f6cac1f24b7ff9b5842a1219134bdaa0a9ead`  
		Last Modified: Mon, 09 Feb 2026 19:25:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e7ae1561b7b40cde311537d5e0309440deff6a7f24f611bc184bda5f1d38bd`  
		Last Modified: Mon, 09 Feb 2026 19:25:50 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c37d7d4e5b47b4645aa14977cbdf0a7c21074a2fdf3482e3b3c0cb271abf80a`  
		Last Modified: Mon, 09 Feb 2026 19:25:50 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.5-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:04310d0f8e7b6adc99ff7b0cc74284cae6303a4c2665b98ecb47e6a4eae6ba9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de48f9b6058f28fab4ec87d222d9bc99a75e6fc1a4190098219cc5155b166c5`

```dockerfile
```

-	Layers:
	-	`sha256:d78db083114a500e7280bf84a28004b52f269ca2f5d1bcc85dfc7aa7b751b34c`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.5.44`

```console
$ docker pull clickhouse@sha256:2c55b8abc96a804c895f903e85d093a32dfc2ec1c9060da59af36bd24210ff10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.5.44` - linux; amd64

```console
$ docker pull clickhouse@sha256:f5d34c2ca9820776c5caa971f844a589d4a0ad514786bbc224da4fec0783e22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246336449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace786d945703abf2fdf5360b5c9ae7db6f6b2855023093413e33e3410033621`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:37 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:37 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:37 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:37 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:37 GMT
ARG VERSION=25.12.5.44
# Mon, 09 Feb 2026 19:25:37 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:06 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:06 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1bee7891ee835f80d9ea3c337f089e4d4c5c746d13dde6d3ebd5c323f0612c`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 7.6 MB (7598396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0ce0ee21c47da2b40262a15e02a854229ff848a8fcfb29925665f32cdf296f`  
		Last Modified: Mon, 09 Feb 2026 19:26:32 GMT  
		Size: 208.3 MB (208331334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2d133c574df0cfa824c641410e4ba1c3e447dcff2322d9a25ee98b59d37b71`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc605d5de901a7e6336a922f6622749645902592ca338541b241f1da57dffe3`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fa78aedd6caca205e01e65378a244180abd21e68ba16acdcd6015964fcc761`  
		Last Modified: Mon, 09 Feb 2026 19:26:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d8742747b7d384d0f5e4f8293974e93ee12cec36676898fcbd7e1f180bd488`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b5bd28bcc5dcbe897485cd139839c5dc64b5bb2d3b32b7f327ada02a64a69e`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.5.44` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6b62ce8043f679b87fa9e306a6ce5d31373b57827a4062a4c3773aa51f88631a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8087ec5a178b76c50bcdb326592d46d9131de528c2c8e8b3a2162d44afc591d2`

```dockerfile
```

-	Layers:
	-	`sha256:d7c47fc44bbb54311c32bd7a612f7046e0d37c86a5666ab69e1eefbe1945fa6a`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.5.44` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4b5799813306e3a8e767a12f0a58d48a80b6b2ea31e53c027815334eea03ecac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228262613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b21832377bb22afeddc7d892f945ac7a326fb555bbc4b7aa92fa0a775cfa2d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:24:53 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:24:53 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:24:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:24:53 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:24:53 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:24:53 GMT
ARG VERSION=25.12.5.44
# Mon, 09 Feb 2026 19:24:53 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:26 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:26 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:26 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c9a9191b66439b9052bc22174f4e8ae514813dc91db5af58426f4fe2e7f4`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 7.6 MB (7577458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d454d3ee4b48fdb02306c5ba2e17867990f78343ca4f4ba60ac03733ea64eef4`  
		Last Modified: Mon, 09 Feb 2026 19:25:52 GMT  
		Size: 192.4 MB (192431607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f3c6f6d4899efdcea0e71fa57f74380260076a9217d9aea9adc20657ebb761`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2b3cdde424a9f8f713cfa50e453023c9f4771d1ccd3b5910eebc7ea482a4ac`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96df76ae94980530a4e07de65b4f6cac1f24b7ff9b5842a1219134bdaa0a9ead`  
		Last Modified: Mon, 09 Feb 2026 19:25:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e7ae1561b7b40cde311537d5e0309440deff6a7f24f611bc184bda5f1d38bd`  
		Last Modified: Mon, 09 Feb 2026 19:25:50 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c37d7d4e5b47b4645aa14977cbdf0a7c21074a2fdf3482e3b3c0cb271abf80a`  
		Last Modified: Mon, 09 Feb 2026 19:25:50 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.5.44` - unknown; unknown

```console
$ docker pull clickhouse@sha256:04310d0f8e7b6adc99ff7b0cc74284cae6303a4c2665b98ecb47e6a4eae6ba9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de48f9b6058f28fab4ec87d222d9bc99a75e6fc1a4190098219cc5155b166c5`

```dockerfile
```

-	Layers:
	-	`sha256:d78db083114a500e7280bf84a28004b52f269ca2f5d1bcc85dfc7aa7b751b34c`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.12.5.44-jammy`

```console
$ docker pull clickhouse@sha256:2c55b8abc96a804c895f903e85d093a32dfc2ec1c9060da59af36bd24210ff10
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.12.5.44-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f5d34c2ca9820776c5caa971f844a589d4a0ad514786bbc224da4fec0783e22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.3 MB (246336449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace786d945703abf2fdf5360b5c9ae7db6f6b2855023093413e33e3410033621`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:37 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:37 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:37 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:37 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:37 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:37 GMT
ARG VERSION=25.12.5.44
# Mon, 09 Feb 2026 19:25:37 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:06 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:06 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1bee7891ee835f80d9ea3c337f089e4d4c5c746d13dde6d3ebd5c323f0612c`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 7.6 MB (7598396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0ce0ee21c47da2b40262a15e02a854229ff848a8fcfb29925665f32cdf296f`  
		Last Modified: Mon, 09 Feb 2026 19:26:32 GMT  
		Size: 208.3 MB (208331334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf2d133c574df0cfa824c641410e4ba1c3e447dcff2322d9a25ee98b59d37b71`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc605d5de901a7e6336a922f6622749645902592ca338541b241f1da57dffe3`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fa78aedd6caca205e01e65378a244180abd21e68ba16acdcd6015964fcc761`  
		Last Modified: Mon, 09 Feb 2026 19:26:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d8742747b7d384d0f5e4f8293974e93ee12cec36676898fcbd7e1f180bd488`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b5bd28bcc5dcbe897485cd139839c5dc64b5bb2d3b32b7f327ada02a64a69e`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 3.6 KB (3638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.5.44-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:6b62ce8043f679b87fa9e306a6ce5d31373b57827a4062a4c3773aa51f88631a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8087ec5a178b76c50bcdb326592d46d9131de528c2c8e8b3a2162d44afc591d2`

```dockerfile
```

-	Layers:
	-	`sha256:d7c47fc44bbb54311c32bd7a612f7046e0d37c86a5666ab69e1eefbe1945fa6a`  
		Last Modified: Mon, 09 Feb 2026 19:26:28 GMT  
		Size: 25.4 KB (25437 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.12.5.44-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:4b5799813306e3a8e767a12f0a58d48a80b6b2ea31e53c027815334eea03ecac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.3 MB (228262613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b21832377bb22afeddc7d892f945ac7a326fb555bbc4b7aa92fa0a775cfa2d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:24:53 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:24:53 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:24:53 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:24:53 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:24:53 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:24:53 GMT
ARG VERSION=25.12.5.44
# Mon, 09 Feb 2026 19:24:53 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:25 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:26 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.12.5.44 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:26 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:26 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:26 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c9a9191b66439b9052bc22174f4e8ae514813dc91db5af58426f4fe2e7f4`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 7.6 MB (7577458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d454d3ee4b48fdb02306c5ba2e17867990f78343ca4f4ba60ac03733ea64eef4`  
		Last Modified: Mon, 09 Feb 2026 19:25:52 GMT  
		Size: 192.4 MB (192431607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77f3c6f6d4899efdcea0e71fa57f74380260076a9217d9aea9adc20657ebb761`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2b3cdde424a9f8f713cfa50e453023c9f4771d1ccd3b5910eebc7ea482a4ac`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96df76ae94980530a4e07de65b4f6cac1f24b7ff9b5842a1219134bdaa0a9ead`  
		Last Modified: Mon, 09 Feb 2026 19:25:49 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e7ae1561b7b40cde311537d5e0309440deff6a7f24f611bc184bda5f1d38bd`  
		Last Modified: Mon, 09 Feb 2026 19:25:50 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c37d7d4e5b47b4645aa14977cbdf0a7c21074a2fdf3482e3b3c0cb271abf80a`  
		Last Modified: Mon, 09 Feb 2026 19:25:50 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.12.5.44-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:04310d0f8e7b6adc99ff7b0cc74284cae6303a4c2665b98ecb47e6a4eae6ba9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de48f9b6058f28fab4ec87d222d9bc99a75e6fc1a4190098219cc5155b166c5`

```dockerfile
```

-	Layers:
	-	`sha256:d78db083114a500e7280bf84a28004b52f269ca2f5d1bcc85dfc7aa7b751b34c`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 25.6 KB (25625 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:d386385425a13e066673853c3ce6c371c15bdaf13d72b3c6c19a5b0ed566b155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:589ce4735f19bfb3a4e79e44858f87616dbb1c5529d96547474339c27723bfe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870e14a84693b7482566ab4040be4997f35e0964f604e8113a169f2d6379a5b3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:26:02 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:26:02 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:26:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:26:02 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:26:02 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:26:02 GMT
ARG VERSION=25.3.14.14
# Mon, 09 Feb 2026 19:26:02 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:29 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:29 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a77c937b2ed632a13efa495aff5e5e309a84100be1acda4cfee00208890843`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 7.2 MB (7151620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1653cd8bcf544d71ef43d720a50cebba2df846ad6d26dd06080301c5dab7189`  
		Last Modified: Mon, 09 Feb 2026 19:26:53 GMT  
		Size: 168.8 MB (168777531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6537059d5c76d6b74be6bd9150abbe940f2fb6a18eb0623be30ff4b6be06a7`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a5a4ae591f98104b2fdd82701f2777b055dea4bbd7cc1dd1c4693a314c1321`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10af7aa178eec8fb5ab74ae82b77d690ba8e90098b80076cb76501b5e91db13e`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c1224082c82c7119ff02fea9a2eedb1d1fda5f4ab5de89df1056f8ee6bdf9c`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a349ffe4ed170c7ae5475b3bcf19e83ca37eea1772830d5bc8b353d08b328d`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:28362f806c358e88253ec8c1696c18c7d5bd5aff6c7ac46b79ac66f67d39ad9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11d441b3f191533a58995489a0e5a775bfab1ed8b94b04c451520ae8681f513`

```dockerfile
```

-	Layers:
	-	`sha256:be3869b57e0dd333e2feec769ba96ff2f8a3a3ede9bd11d41870f1a51d46bbd6`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0e010927d84aeccbb8ac4e94bf180358d7ccc745dff34259167eedd82f3848d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193804806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210c1d31e64b46b6b06331e9c29aa1ca6f4d8b3c0f2979d3ca457fe7bb991c06`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:26:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:26:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:26:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:26:03 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:26:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:26:03 GMT
ARG VERSION=25.3.14.14
# Mon, 09 Feb 2026 19:26:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:28 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6fb5eaaa8307c11177c8aee5398e10df8a226ca52748dd2d28130d2b79d829`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 7.1 MB (7127990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7ebec55f27dbe1c8651240157487c1bfc17dc7bb3cc1579b2f1de04724b194`  
		Last Modified: Mon, 09 Feb 2026 19:26:48 GMT  
		Size: 158.4 MB (158423068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864318820027bcdcba2972523ebbf5d8471c1d2c684a491cb8f2226a99dfbeb5`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3badd0d6eedc78141a8af74647dce439dec4b83d36bfe8f1736d299a3da36543`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0583c5a852ea3e219c65df1bafed71d3793690504aa0e88bfe94a2abdad58155`  
		Last Modified: Mon, 09 Feb 2026 19:26:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2032c1b586a0ba1a35db47b06facf25ae5aead7f25dc853dbf5be604e015a8b6`  
		Last Modified: Mon, 09 Feb 2026 19:26:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5a16da4dc6faf589287c308a4f27ddd84e90d4b9923c6f033fe7951c76f2cf`  
		Last Modified: Mon, 09 Feb 2026 19:26:47 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:124a84f028df18723b9bbe1f726db5c5bc917887e7153c8d70668d5b50aaa9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2de1e52eff741d51961a6a0d04d7cdb17082b188b79a4be1270c24c5a537224`

```dockerfile
```

-	Layers:
	-	`sha256:c390845d0ab63ba648f7164df3b3e4dde3f1a20edb6a36c922632e2409afb0ef`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:d386385425a13e066673853c3ce6c371c15bdaf13d72b3c6c19a5b0ed566b155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:589ce4735f19bfb3a4e79e44858f87616dbb1c5529d96547474339c27723bfe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870e14a84693b7482566ab4040be4997f35e0964f604e8113a169f2d6379a5b3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:26:02 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:26:02 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:26:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:26:02 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:26:02 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:26:02 GMT
ARG VERSION=25.3.14.14
# Mon, 09 Feb 2026 19:26:02 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:29 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:29 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a77c937b2ed632a13efa495aff5e5e309a84100be1acda4cfee00208890843`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 7.2 MB (7151620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1653cd8bcf544d71ef43d720a50cebba2df846ad6d26dd06080301c5dab7189`  
		Last Modified: Mon, 09 Feb 2026 19:26:53 GMT  
		Size: 168.8 MB (168777531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6537059d5c76d6b74be6bd9150abbe940f2fb6a18eb0623be30ff4b6be06a7`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a5a4ae591f98104b2fdd82701f2777b055dea4bbd7cc1dd1c4693a314c1321`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10af7aa178eec8fb5ab74ae82b77d690ba8e90098b80076cb76501b5e91db13e`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c1224082c82c7119ff02fea9a2eedb1d1fda5f4ab5de89df1056f8ee6bdf9c`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a349ffe4ed170c7ae5475b3bcf19e83ca37eea1772830d5bc8b353d08b328d`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:28362f806c358e88253ec8c1696c18c7d5bd5aff6c7ac46b79ac66f67d39ad9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11d441b3f191533a58995489a0e5a775bfab1ed8b94b04c451520ae8681f513`

```dockerfile
```

-	Layers:
	-	`sha256:be3869b57e0dd333e2feec769ba96ff2f8a3a3ede9bd11d41870f1a51d46bbd6`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0e010927d84aeccbb8ac4e94bf180358d7ccc745dff34259167eedd82f3848d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193804806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210c1d31e64b46b6b06331e9c29aa1ca6f4d8b3c0f2979d3ca457fe7bb991c06`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:26:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:26:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:26:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:26:03 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:26:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:26:03 GMT
ARG VERSION=25.3.14.14
# Mon, 09 Feb 2026 19:26:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:28 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6fb5eaaa8307c11177c8aee5398e10df8a226ca52748dd2d28130d2b79d829`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 7.1 MB (7127990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7ebec55f27dbe1c8651240157487c1bfc17dc7bb3cc1579b2f1de04724b194`  
		Last Modified: Mon, 09 Feb 2026 19:26:48 GMT  
		Size: 158.4 MB (158423068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864318820027bcdcba2972523ebbf5d8471c1d2c684a491cb8f2226a99dfbeb5`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3badd0d6eedc78141a8af74647dce439dec4b83d36bfe8f1736d299a3da36543`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0583c5a852ea3e219c65df1bafed71d3793690504aa0e88bfe94a2abdad58155`  
		Last Modified: Mon, 09 Feb 2026 19:26:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2032c1b586a0ba1a35db47b06facf25ae5aead7f25dc853dbf5be604e015a8b6`  
		Last Modified: Mon, 09 Feb 2026 19:26:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5a16da4dc6faf589287c308a4f27ddd84e90d4b9923c6f033fe7951c76f2cf`  
		Last Modified: Mon, 09 Feb 2026 19:26:47 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:124a84f028df18723b9bbe1f726db5c5bc917887e7153c8d70668d5b50aaa9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2de1e52eff741d51961a6a0d04d7cdb17082b188b79a4be1270c24c5a537224`

```dockerfile
```

-	Layers:
	-	`sha256:c390845d0ab63ba648f7164df3b3e4dde3f1a20edb6a36c922632e2409afb0ef`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14`

```console
$ docker pull clickhouse@sha256:d386385425a13e066673853c3ce6c371c15bdaf13d72b3c6c19a5b0ed566b155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.14` - linux; amd64

```console
$ docker pull clickhouse@sha256:589ce4735f19bfb3a4e79e44858f87616dbb1c5529d96547474339c27723bfe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870e14a84693b7482566ab4040be4997f35e0964f604e8113a169f2d6379a5b3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:26:02 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:26:02 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:26:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:26:02 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:26:02 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:26:02 GMT
ARG VERSION=25.3.14.14
# Mon, 09 Feb 2026 19:26:02 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:29 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:29 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a77c937b2ed632a13efa495aff5e5e309a84100be1acda4cfee00208890843`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 7.2 MB (7151620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1653cd8bcf544d71ef43d720a50cebba2df846ad6d26dd06080301c5dab7189`  
		Last Modified: Mon, 09 Feb 2026 19:26:53 GMT  
		Size: 168.8 MB (168777531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6537059d5c76d6b74be6bd9150abbe940f2fb6a18eb0623be30ff4b6be06a7`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a5a4ae591f98104b2fdd82701f2777b055dea4bbd7cc1dd1c4693a314c1321`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10af7aa178eec8fb5ab74ae82b77d690ba8e90098b80076cb76501b5e91db13e`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c1224082c82c7119ff02fea9a2eedb1d1fda5f4ab5de89df1056f8ee6bdf9c`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a349ffe4ed170c7ae5475b3bcf19e83ca37eea1772830d5bc8b353d08b328d`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:28362f806c358e88253ec8c1696c18c7d5bd5aff6c7ac46b79ac66f67d39ad9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11d441b3f191533a58995489a0e5a775bfab1ed8b94b04c451520ae8681f513`

```dockerfile
```

-	Layers:
	-	`sha256:be3869b57e0dd333e2feec769ba96ff2f8a3a3ede9bd11d41870f1a51d46bbd6`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.14` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0e010927d84aeccbb8ac4e94bf180358d7ccc745dff34259167eedd82f3848d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193804806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210c1d31e64b46b6b06331e9c29aa1ca6f4d8b3c0f2979d3ca457fe7bb991c06`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:26:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:26:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:26:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:26:03 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:26:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:26:03 GMT
ARG VERSION=25.3.14.14
# Mon, 09 Feb 2026 19:26:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:28 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6fb5eaaa8307c11177c8aee5398e10df8a226ca52748dd2d28130d2b79d829`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 7.1 MB (7127990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7ebec55f27dbe1c8651240157487c1bfc17dc7bb3cc1579b2f1de04724b194`  
		Last Modified: Mon, 09 Feb 2026 19:26:48 GMT  
		Size: 158.4 MB (158423068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864318820027bcdcba2972523ebbf5d8471c1d2c684a491cb8f2226a99dfbeb5`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3badd0d6eedc78141a8af74647dce439dec4b83d36bfe8f1736d299a3da36543`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0583c5a852ea3e219c65df1bafed71d3793690504aa0e88bfe94a2abdad58155`  
		Last Modified: Mon, 09 Feb 2026 19:26:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2032c1b586a0ba1a35db47b06facf25ae5aead7f25dc853dbf5be604e015a8b6`  
		Last Modified: Mon, 09 Feb 2026 19:26:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5a16da4dc6faf589287c308a4f27ddd84e90d4b9923c6f033fe7951c76f2cf`  
		Last Modified: Mon, 09 Feb 2026 19:26:47 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:124a84f028df18723b9bbe1f726db5c5bc917887e7153c8d70668d5b50aaa9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2de1e52eff741d51961a6a0d04d7cdb17082b188b79a4be1270c24c5a537224`

```dockerfile
```

-	Layers:
	-	`sha256:c390845d0ab63ba648f7164df3b3e4dde3f1a20edb6a36c922632e2409afb0ef`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14-jammy`

```console
$ docker pull clickhouse@sha256:d386385425a13e066673853c3ce6c371c15bdaf13d72b3c6c19a5b0ed566b155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.14-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:589ce4735f19bfb3a4e79e44858f87616dbb1c5529d96547474339c27723bfe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870e14a84693b7482566ab4040be4997f35e0964f604e8113a169f2d6379a5b3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:26:02 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:26:02 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:26:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:26:02 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:26:02 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:26:02 GMT
ARG VERSION=25.3.14.14
# Mon, 09 Feb 2026 19:26:02 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:29 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:29 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a77c937b2ed632a13efa495aff5e5e309a84100be1acda4cfee00208890843`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 7.2 MB (7151620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1653cd8bcf544d71ef43d720a50cebba2df846ad6d26dd06080301c5dab7189`  
		Last Modified: Mon, 09 Feb 2026 19:26:53 GMT  
		Size: 168.8 MB (168777531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6537059d5c76d6b74be6bd9150abbe940f2fb6a18eb0623be30ff4b6be06a7`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a5a4ae591f98104b2fdd82701f2777b055dea4bbd7cc1dd1c4693a314c1321`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10af7aa178eec8fb5ab74ae82b77d690ba8e90098b80076cb76501b5e91db13e`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c1224082c82c7119ff02fea9a2eedb1d1fda5f4ab5de89df1056f8ee6bdf9c`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a349ffe4ed170c7ae5475b3bcf19e83ca37eea1772830d5bc8b353d08b328d`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:28362f806c358e88253ec8c1696c18c7d5bd5aff6c7ac46b79ac66f67d39ad9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11d441b3f191533a58995489a0e5a775bfab1ed8b94b04c451520ae8681f513`

```dockerfile
```

-	Layers:
	-	`sha256:be3869b57e0dd333e2feec769ba96ff2f8a3a3ede9bd11d41870f1a51d46bbd6`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.14-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0e010927d84aeccbb8ac4e94bf180358d7ccc745dff34259167eedd82f3848d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193804806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210c1d31e64b46b6b06331e9c29aa1ca6f4d8b3c0f2979d3ca457fe7bb991c06`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:26:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:26:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:26:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:26:03 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:26:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:26:03 GMT
ARG VERSION=25.3.14.14
# Mon, 09 Feb 2026 19:26:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:28 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6fb5eaaa8307c11177c8aee5398e10df8a226ca52748dd2d28130d2b79d829`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 7.1 MB (7127990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7ebec55f27dbe1c8651240157487c1bfc17dc7bb3cc1579b2f1de04724b194`  
		Last Modified: Mon, 09 Feb 2026 19:26:48 GMT  
		Size: 158.4 MB (158423068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864318820027bcdcba2972523ebbf5d8471c1d2c684a491cb8f2226a99dfbeb5`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3badd0d6eedc78141a8af74647dce439dec4b83d36bfe8f1736d299a3da36543`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0583c5a852ea3e219c65df1bafed71d3793690504aa0e88bfe94a2abdad58155`  
		Last Modified: Mon, 09 Feb 2026 19:26:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2032c1b586a0ba1a35db47b06facf25ae5aead7f25dc853dbf5be604e015a8b6`  
		Last Modified: Mon, 09 Feb 2026 19:26:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5a16da4dc6faf589287c308a4f27ddd84e90d4b9923c6f033fe7951c76f2cf`  
		Last Modified: Mon, 09 Feb 2026 19:26:47 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:124a84f028df18723b9bbe1f726db5c5bc917887e7153c8d70668d5b50aaa9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2de1e52eff741d51961a6a0d04d7cdb17082b188b79a4be1270c24c5a537224`

```dockerfile
```

-	Layers:
	-	`sha256:c390845d0ab63ba648f7164df3b3e4dde3f1a20edb6a36c922632e2409afb0ef`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14.14`

```console
$ docker pull clickhouse@sha256:d386385425a13e066673853c3ce6c371c15bdaf13d72b3c6c19a5b0ed566b155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.14.14` - linux; amd64

```console
$ docker pull clickhouse@sha256:589ce4735f19bfb3a4e79e44858f87616dbb1c5529d96547474339c27723bfe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870e14a84693b7482566ab4040be4997f35e0964f604e8113a169f2d6379a5b3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:26:02 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:26:02 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:26:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:26:02 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:26:02 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:26:02 GMT
ARG VERSION=25.3.14.14
# Mon, 09 Feb 2026 19:26:02 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:29 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:29 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a77c937b2ed632a13efa495aff5e5e309a84100be1acda4cfee00208890843`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 7.2 MB (7151620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1653cd8bcf544d71ef43d720a50cebba2df846ad6d26dd06080301c5dab7189`  
		Last Modified: Mon, 09 Feb 2026 19:26:53 GMT  
		Size: 168.8 MB (168777531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6537059d5c76d6b74be6bd9150abbe940f2fb6a18eb0623be30ff4b6be06a7`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a5a4ae591f98104b2fdd82701f2777b055dea4bbd7cc1dd1c4693a314c1321`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10af7aa178eec8fb5ab74ae82b77d690ba8e90098b80076cb76501b5e91db13e`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c1224082c82c7119ff02fea9a2eedb1d1fda5f4ab5de89df1056f8ee6bdf9c`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a349ffe4ed170c7ae5475b3bcf19e83ca37eea1772830d5bc8b353d08b328d`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:28362f806c358e88253ec8c1696c18c7d5bd5aff6c7ac46b79ac66f67d39ad9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11d441b3f191533a58995489a0e5a775bfab1ed8b94b04c451520ae8681f513`

```dockerfile
```

-	Layers:
	-	`sha256:be3869b57e0dd333e2feec769ba96ff2f8a3a3ede9bd11d41870f1a51d46bbd6`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.14.14` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0e010927d84aeccbb8ac4e94bf180358d7ccc745dff34259167eedd82f3848d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193804806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210c1d31e64b46b6b06331e9c29aa1ca6f4d8b3c0f2979d3ca457fe7bb991c06`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:26:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:26:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:26:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:26:03 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:26:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:26:03 GMT
ARG VERSION=25.3.14.14
# Mon, 09 Feb 2026 19:26:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:28 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6fb5eaaa8307c11177c8aee5398e10df8a226ca52748dd2d28130d2b79d829`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 7.1 MB (7127990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7ebec55f27dbe1c8651240157487c1bfc17dc7bb3cc1579b2f1de04724b194`  
		Last Modified: Mon, 09 Feb 2026 19:26:48 GMT  
		Size: 158.4 MB (158423068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864318820027bcdcba2972523ebbf5d8471c1d2c684a491cb8f2226a99dfbeb5`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3badd0d6eedc78141a8af74647dce439dec4b83d36bfe8f1736d299a3da36543`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0583c5a852ea3e219c65df1bafed71d3793690504aa0e88bfe94a2abdad58155`  
		Last Modified: Mon, 09 Feb 2026 19:26:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2032c1b586a0ba1a35db47b06facf25ae5aead7f25dc853dbf5be604e015a8b6`  
		Last Modified: Mon, 09 Feb 2026 19:26:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5a16da4dc6faf589287c308a4f27ddd84e90d4b9923c6f033fe7951c76f2cf`  
		Last Modified: Mon, 09 Feb 2026 19:26:47 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14` - unknown; unknown

```console
$ docker pull clickhouse@sha256:124a84f028df18723b9bbe1f726db5c5bc917887e7153c8d70668d5b50aaa9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2de1e52eff741d51961a6a0d04d7cdb17082b188b79a4be1270c24c5a537224`

```dockerfile
```

-	Layers:
	-	`sha256:c390845d0ab63ba648f7164df3b3e4dde3f1a20edb6a36c922632e2409afb0ef`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.14.14-jammy`

```console
$ docker pull clickhouse@sha256:d386385425a13e066673853c3ce6c371c15bdaf13d72b3c6c19a5b0ed566b155
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3.14.14-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:589ce4735f19bfb3a4e79e44858f87616dbb1c5529d96547474339c27723bfe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.3 MB (206336073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:870e14a84693b7482566ab4040be4997f35e0964f604e8113a169f2d6379a5b3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:26:02 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:26:02 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:26:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:26:02 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:26:02 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:26:02 GMT
ARG VERSION=25.3.14.14
# Mon, 09 Feb 2026 19:26:02 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:29 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:29 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:29 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:29 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:29 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a77c937b2ed632a13efa495aff5e5e309a84100be1acda4cfee00208890843`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 7.2 MB (7151620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1653cd8bcf544d71ef43d720a50cebba2df846ad6d26dd06080301c5dab7189`  
		Last Modified: Mon, 09 Feb 2026 19:26:53 GMT  
		Size: 168.8 MB (168777531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6537059d5c76d6b74be6bd9150abbe940f2fb6a18eb0623be30ff4b6be06a7`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a5a4ae591f98104b2fdd82701f2777b055dea4bbd7cc1dd1c4693a314c1321`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 865.8 KB (865753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10af7aa178eec8fb5ab74ae82b77d690ba8e90098b80076cb76501b5e91db13e`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c1224082c82c7119ff02fea9a2eedb1d1fda5f4ab5de89df1056f8ee6bdf9c`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a349ffe4ed170c7ae5475b3bcf19e83ca37eea1772830d5bc8b353d08b328d`  
		Last Modified: Mon, 09 Feb 2026 19:26:50 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:28362f806c358e88253ec8c1696c18c7d5bd5aff6c7ac46b79ac66f67d39ad9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e11d441b3f191533a58995489a0e5a775bfab1ed8b94b04c451520ae8681f513`

```dockerfile
```

-	Layers:
	-	`sha256:be3869b57e0dd333e2feec769ba96ff2f8a3a3ede9bd11d41870f1a51d46bbd6`  
		Last Modified: Mon, 09 Feb 2026 19:26:49 GMT  
		Size: 25.2 KB (25235 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3.14.14-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:0e010927d84aeccbb8ac4e94bf180358d7ccc745dff34259167eedd82f3848d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 MB (193804806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210c1d31e64b46b6b06331e9c29aa1ca6f4d8b3c0f2979d3ca457fe7bb991c06`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:26:03 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:26:03 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:26:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:26:03 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:26:03 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:26:03 GMT
ARG VERSION=25.3.14.14
# Mon, 09 Feb 2026 19:26:03 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:28 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:28 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.14.14 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:28 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:28 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:28 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6fb5eaaa8307c11177c8aee5398e10df8a226ca52748dd2d28130d2b79d829`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 7.1 MB (7127990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e7ebec55f27dbe1c8651240157487c1bfc17dc7bb3cc1579b2f1de04724b194`  
		Last Modified: Mon, 09 Feb 2026 19:26:48 GMT  
		Size: 158.4 MB (158423068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864318820027bcdcba2972523ebbf5d8471c1d2c684a491cb8f2226a99dfbeb5`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3badd0d6eedc78141a8af74647dce439dec4b83d36bfe8f1736d299a3da36543`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0583c5a852ea3e219c65df1bafed71d3793690504aa0e88bfe94a2abdad58155`  
		Last Modified: Mon, 09 Feb 2026 19:26:46 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2032c1b586a0ba1a35db47b06facf25ae5aead7f25dc853dbf5be604e015a8b6`  
		Last Modified: Mon, 09 Feb 2026 19:26:46 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5a16da4dc6faf589287c308a4f27ddd84e90d4b9923c6f033fe7951c76f2cf`  
		Last Modified: Mon, 09 Feb 2026 19:26:47 GMT  
		Size: 3.8 KB (3834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3.14.14-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:124a84f028df18723b9bbe1f726db5c5bc917887e7153c8d70668d5b50aaa9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2de1e52eff741d51961a6a0d04d7cdb17082b188b79a4be1270c24c5a537224`

```dockerfile
```

-	Layers:
	-	`sha256:c390845d0ab63ba648f7164df3b3e4dde3f1a20edb6a36c922632e2409afb0ef`  
		Last Modified: Mon, 09 Feb 2026 19:26:45 GMT  
		Size: 25.4 KB (25423 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:84920b9a25b5c8a212adcd7a146ad81dfabcc424973dba20f5c59e290a388bd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:f6a1295b2d14d196e527e8409ac4705dd7fe3af88d3f722361f67c3539d42318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228944439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0253b7565919469f5389ca707d1452a06646b0f9d8c5e0b8f269caf615911ddf`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:16 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:16 GMT
ARG VERSION=25.8.16.34
# Mon, 09 Feb 2026 19:25:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:45 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:45 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:45 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99570f0435d34b24aac45231ea0fa7e0a7e0e962b1b9d3cbc9fe0cea69275be6`  
		Last Modified: Mon, 09 Feb 2026 19:26:05 GMT  
		Size: 7.6 MB (7598385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b899fd194a87b9af8c90ccbcef12714f388acf5f9860671060cf352564756222`  
		Last Modified: Mon, 09 Feb 2026 19:26:08 GMT  
		Size: 190.9 MB (190939363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa59f2de6256648b152f31d44fa268453f9c34021e7f1452d87aae78e03581b5`  
		Last Modified: Mon, 09 Feb 2026 19:26:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24efb35ec9916375db74a35833ce83d5881ad8d985f525dc4b9c8cb924e2a2d5`  
		Last Modified: Mon, 09 Feb 2026 19:26:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d40dde76a505ae83db462d188b3407f3f6761d0a87d881ccffb21ed36523cb3`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e965f0ac22f2bf7b9d43dec0dbc8d75b51045c8f909c04f0732300b6731a805a`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26991bc2f6a9d75bb46bb4282d69401547da51270840d5aaec91ab9d54211cc`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b2f935903def416f930ab8c0719f47ef2788a3300c32c8f21169f04f0c66774d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83dc69c9ec6ed8cdb73ae6ec69ea9146ee88fa01798d4f9fb4fce20b45d4b69`

```dockerfile
```

-	Layers:
	-	`sha256:2bd223ca45ce30aa21ef9e4893d3f6d5e76664df3187b528ba514bfc3074e698`  
		Last Modified: Mon, 09 Feb 2026 19:26:04 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d14b4e6e073e517f963f21c0559e31f24516918793aec5101f9f54fdb9f0466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213846849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e66a9d25fbfaeea39049e873ba70a933548fa4e14c05689f5969557b58f89e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:42 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:42 GMT
ARG VERSION=25.8.16.34
# Mon, 09 Feb 2026 19:25:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:11 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:11 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c82f17864370e6cdf1f007b8c9d11a870b0bc51635fbe6ddd0750d786cec27`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 7.6 MB (7577444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622c812c4902910e844748b2efc310761357b5c4c58f6284c56b48138b137e0`  
		Last Modified: Mon, 09 Feb 2026 19:26:33 GMT  
		Size: 178.0 MB (178015884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a974dcf9c498586c1cf71d7f04714a1a1697617c5230d259730784190625411`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e630840927f4615707188e5b41fd9935a49a3725243f0004732a26bf9d77d33d`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea686a67e9d34b994b4217ba3734212d2047775be05b9db267305b01815deac`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09fdc0bf6bdffeabf8e4fdee1fda69ef034f1910c584a6bc0b2e55a2c0eb64d`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c2bbf122c71596e3af5f65e9c36cf7887f5976b981ebafaf39f4ab2fc2d787`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4de1ce8516a189809922bb79d7745209095007d4c91eeccb82e208a521cee9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43520ccaaf175a71da3230708a4d63dd10dbdcebb6b583ed67aa95ec0d84499`

```dockerfile
```

-	Layers:
	-	`sha256:e47505f85dee32c839604eba0c36d1194e1f105f7db3d218029599184fe0f99a`  
		Last Modified: Mon, 09 Feb 2026 19:26:29 GMT  
		Size: 26.3 KB (26256 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:84920b9a25b5c8a212adcd7a146ad81dfabcc424973dba20f5c59e290a388bd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f6a1295b2d14d196e527e8409ac4705dd7fe3af88d3f722361f67c3539d42318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228944439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0253b7565919469f5389ca707d1452a06646b0f9d8c5e0b8f269caf615911ddf`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:16 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:16 GMT
ARG VERSION=25.8.16.34
# Mon, 09 Feb 2026 19:25:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:45 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:45 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:45 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99570f0435d34b24aac45231ea0fa7e0a7e0e962b1b9d3cbc9fe0cea69275be6`  
		Last Modified: Mon, 09 Feb 2026 19:26:05 GMT  
		Size: 7.6 MB (7598385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b899fd194a87b9af8c90ccbcef12714f388acf5f9860671060cf352564756222`  
		Last Modified: Mon, 09 Feb 2026 19:26:08 GMT  
		Size: 190.9 MB (190939363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa59f2de6256648b152f31d44fa268453f9c34021e7f1452d87aae78e03581b5`  
		Last Modified: Mon, 09 Feb 2026 19:26:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24efb35ec9916375db74a35833ce83d5881ad8d985f525dc4b9c8cb924e2a2d5`  
		Last Modified: Mon, 09 Feb 2026 19:26:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d40dde76a505ae83db462d188b3407f3f6761d0a87d881ccffb21ed36523cb3`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e965f0ac22f2bf7b9d43dec0dbc8d75b51045c8f909c04f0732300b6731a805a`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26991bc2f6a9d75bb46bb4282d69401547da51270840d5aaec91ab9d54211cc`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b2f935903def416f930ab8c0719f47ef2788a3300c32c8f21169f04f0c66774d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83dc69c9ec6ed8cdb73ae6ec69ea9146ee88fa01798d4f9fb4fce20b45d4b69`

```dockerfile
```

-	Layers:
	-	`sha256:2bd223ca45ce30aa21ef9e4893d3f6d5e76664df3187b528ba514bfc3074e698`  
		Last Modified: Mon, 09 Feb 2026 19:26:04 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d14b4e6e073e517f963f21c0559e31f24516918793aec5101f9f54fdb9f0466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213846849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e66a9d25fbfaeea39049e873ba70a933548fa4e14c05689f5969557b58f89e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:42 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:42 GMT
ARG VERSION=25.8.16.34
# Mon, 09 Feb 2026 19:25:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:11 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:11 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c82f17864370e6cdf1f007b8c9d11a870b0bc51635fbe6ddd0750d786cec27`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 7.6 MB (7577444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622c812c4902910e844748b2efc310761357b5c4c58f6284c56b48138b137e0`  
		Last Modified: Mon, 09 Feb 2026 19:26:33 GMT  
		Size: 178.0 MB (178015884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a974dcf9c498586c1cf71d7f04714a1a1697617c5230d259730784190625411`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e630840927f4615707188e5b41fd9935a49a3725243f0004732a26bf9d77d33d`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea686a67e9d34b994b4217ba3734212d2047775be05b9db267305b01815deac`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09fdc0bf6bdffeabf8e4fdee1fda69ef034f1910c584a6bc0b2e55a2c0eb64d`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c2bbf122c71596e3af5f65e9c36cf7887f5976b981ebafaf39f4ab2fc2d787`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4de1ce8516a189809922bb79d7745209095007d4c91eeccb82e208a521cee9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43520ccaaf175a71da3230708a4d63dd10dbdcebb6b583ed67aa95ec0d84499`

```dockerfile
```

-	Layers:
	-	`sha256:e47505f85dee32c839604eba0c36d1194e1f105f7db3d218029599184fe0f99a`  
		Last Modified: Mon, 09 Feb 2026 19:26:29 GMT  
		Size: 26.3 KB (26256 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.16`

```console
$ docker pull clickhouse@sha256:84920b9a25b5c8a212adcd7a146ad81dfabcc424973dba20f5c59e290a388bd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.16` - linux; amd64

```console
$ docker pull clickhouse@sha256:f6a1295b2d14d196e527e8409ac4705dd7fe3af88d3f722361f67c3539d42318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228944439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0253b7565919469f5389ca707d1452a06646b0f9d8c5e0b8f269caf615911ddf`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:16 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:16 GMT
ARG VERSION=25.8.16.34
# Mon, 09 Feb 2026 19:25:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:45 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:45 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:45 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99570f0435d34b24aac45231ea0fa7e0a7e0e962b1b9d3cbc9fe0cea69275be6`  
		Last Modified: Mon, 09 Feb 2026 19:26:05 GMT  
		Size: 7.6 MB (7598385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b899fd194a87b9af8c90ccbcef12714f388acf5f9860671060cf352564756222`  
		Last Modified: Mon, 09 Feb 2026 19:26:08 GMT  
		Size: 190.9 MB (190939363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa59f2de6256648b152f31d44fa268453f9c34021e7f1452d87aae78e03581b5`  
		Last Modified: Mon, 09 Feb 2026 19:26:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24efb35ec9916375db74a35833ce83d5881ad8d985f525dc4b9c8cb924e2a2d5`  
		Last Modified: Mon, 09 Feb 2026 19:26:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d40dde76a505ae83db462d188b3407f3f6761d0a87d881ccffb21ed36523cb3`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e965f0ac22f2bf7b9d43dec0dbc8d75b51045c8f909c04f0732300b6731a805a`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26991bc2f6a9d75bb46bb4282d69401547da51270840d5aaec91ab9d54211cc`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b2f935903def416f930ab8c0719f47ef2788a3300c32c8f21169f04f0c66774d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83dc69c9ec6ed8cdb73ae6ec69ea9146ee88fa01798d4f9fb4fce20b45d4b69`

```dockerfile
```

-	Layers:
	-	`sha256:2bd223ca45ce30aa21ef9e4893d3f6d5e76664df3187b528ba514bfc3074e698`  
		Last Modified: Mon, 09 Feb 2026 19:26:04 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.16` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d14b4e6e073e517f963f21c0559e31f24516918793aec5101f9f54fdb9f0466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213846849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e66a9d25fbfaeea39049e873ba70a933548fa4e14c05689f5969557b58f89e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:42 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:42 GMT
ARG VERSION=25.8.16.34
# Mon, 09 Feb 2026 19:25:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:11 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:11 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c82f17864370e6cdf1f007b8c9d11a870b0bc51635fbe6ddd0750d786cec27`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 7.6 MB (7577444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622c812c4902910e844748b2efc310761357b5c4c58f6284c56b48138b137e0`  
		Last Modified: Mon, 09 Feb 2026 19:26:33 GMT  
		Size: 178.0 MB (178015884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a974dcf9c498586c1cf71d7f04714a1a1697617c5230d259730784190625411`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e630840927f4615707188e5b41fd9935a49a3725243f0004732a26bf9d77d33d`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea686a67e9d34b994b4217ba3734212d2047775be05b9db267305b01815deac`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09fdc0bf6bdffeabf8e4fdee1fda69ef034f1910c584a6bc0b2e55a2c0eb64d`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c2bbf122c71596e3af5f65e9c36cf7887f5976b981ebafaf39f4ab2fc2d787`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4de1ce8516a189809922bb79d7745209095007d4c91eeccb82e208a521cee9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43520ccaaf175a71da3230708a4d63dd10dbdcebb6b583ed67aa95ec0d84499`

```dockerfile
```

-	Layers:
	-	`sha256:e47505f85dee32c839604eba0c36d1194e1f105f7db3d218029599184fe0f99a`  
		Last Modified: Mon, 09 Feb 2026 19:26:29 GMT  
		Size: 26.3 KB (26256 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.16-jammy`

```console
$ docker pull clickhouse@sha256:84920b9a25b5c8a212adcd7a146ad81dfabcc424973dba20f5c59e290a388bd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.16-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f6a1295b2d14d196e527e8409ac4705dd7fe3af88d3f722361f67c3539d42318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228944439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0253b7565919469f5389ca707d1452a06646b0f9d8c5e0b8f269caf615911ddf`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:16 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:16 GMT
ARG VERSION=25.8.16.34
# Mon, 09 Feb 2026 19:25:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:45 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:45 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:45 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99570f0435d34b24aac45231ea0fa7e0a7e0e962b1b9d3cbc9fe0cea69275be6`  
		Last Modified: Mon, 09 Feb 2026 19:26:05 GMT  
		Size: 7.6 MB (7598385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b899fd194a87b9af8c90ccbcef12714f388acf5f9860671060cf352564756222`  
		Last Modified: Mon, 09 Feb 2026 19:26:08 GMT  
		Size: 190.9 MB (190939363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa59f2de6256648b152f31d44fa268453f9c34021e7f1452d87aae78e03581b5`  
		Last Modified: Mon, 09 Feb 2026 19:26:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24efb35ec9916375db74a35833ce83d5881ad8d985f525dc4b9c8cb924e2a2d5`  
		Last Modified: Mon, 09 Feb 2026 19:26:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d40dde76a505ae83db462d188b3407f3f6761d0a87d881ccffb21ed36523cb3`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e965f0ac22f2bf7b9d43dec0dbc8d75b51045c8f909c04f0732300b6731a805a`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26991bc2f6a9d75bb46bb4282d69401547da51270840d5aaec91ab9d54211cc`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b2f935903def416f930ab8c0719f47ef2788a3300c32c8f21169f04f0c66774d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83dc69c9ec6ed8cdb73ae6ec69ea9146ee88fa01798d4f9fb4fce20b45d4b69`

```dockerfile
```

-	Layers:
	-	`sha256:2bd223ca45ce30aa21ef9e4893d3f6d5e76664df3187b528ba514bfc3074e698`  
		Last Modified: Mon, 09 Feb 2026 19:26:04 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.16-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d14b4e6e073e517f963f21c0559e31f24516918793aec5101f9f54fdb9f0466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213846849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e66a9d25fbfaeea39049e873ba70a933548fa4e14c05689f5969557b58f89e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:42 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:42 GMT
ARG VERSION=25.8.16.34
# Mon, 09 Feb 2026 19:25:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:11 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:11 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c82f17864370e6cdf1f007b8c9d11a870b0bc51635fbe6ddd0750d786cec27`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 7.6 MB (7577444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622c812c4902910e844748b2efc310761357b5c4c58f6284c56b48138b137e0`  
		Last Modified: Mon, 09 Feb 2026 19:26:33 GMT  
		Size: 178.0 MB (178015884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a974dcf9c498586c1cf71d7f04714a1a1697617c5230d259730784190625411`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e630840927f4615707188e5b41fd9935a49a3725243f0004732a26bf9d77d33d`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea686a67e9d34b994b4217ba3734212d2047775be05b9db267305b01815deac`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09fdc0bf6bdffeabf8e4fdee1fda69ef034f1910c584a6bc0b2e55a2c0eb64d`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c2bbf122c71596e3af5f65e9c36cf7887f5976b981ebafaf39f4ab2fc2d787`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4de1ce8516a189809922bb79d7745209095007d4c91eeccb82e208a521cee9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43520ccaaf175a71da3230708a4d63dd10dbdcebb6b583ed67aa95ec0d84499`

```dockerfile
```

-	Layers:
	-	`sha256:e47505f85dee32c839604eba0c36d1194e1f105f7db3d218029599184fe0f99a`  
		Last Modified: Mon, 09 Feb 2026 19:26:29 GMT  
		Size: 26.3 KB (26256 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.16.34`

```console
$ docker pull clickhouse@sha256:84920b9a25b5c8a212adcd7a146ad81dfabcc424973dba20f5c59e290a388bd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.16.34` - linux; amd64

```console
$ docker pull clickhouse@sha256:f6a1295b2d14d196e527e8409ac4705dd7fe3af88d3f722361f67c3539d42318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228944439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0253b7565919469f5389ca707d1452a06646b0f9d8c5e0b8f269caf615911ddf`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:16 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:16 GMT
ARG VERSION=25.8.16.34
# Mon, 09 Feb 2026 19:25:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:45 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:45 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:45 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99570f0435d34b24aac45231ea0fa7e0a7e0e962b1b9d3cbc9fe0cea69275be6`  
		Last Modified: Mon, 09 Feb 2026 19:26:05 GMT  
		Size: 7.6 MB (7598385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b899fd194a87b9af8c90ccbcef12714f388acf5f9860671060cf352564756222`  
		Last Modified: Mon, 09 Feb 2026 19:26:08 GMT  
		Size: 190.9 MB (190939363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa59f2de6256648b152f31d44fa268453f9c34021e7f1452d87aae78e03581b5`  
		Last Modified: Mon, 09 Feb 2026 19:26:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24efb35ec9916375db74a35833ce83d5881ad8d985f525dc4b9c8cb924e2a2d5`  
		Last Modified: Mon, 09 Feb 2026 19:26:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d40dde76a505ae83db462d188b3407f3f6761d0a87d881ccffb21ed36523cb3`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e965f0ac22f2bf7b9d43dec0dbc8d75b51045c8f909c04f0732300b6731a805a`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26991bc2f6a9d75bb46bb4282d69401547da51270840d5aaec91ab9d54211cc`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16.34` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b2f935903def416f930ab8c0719f47ef2788a3300c32c8f21169f04f0c66774d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83dc69c9ec6ed8cdb73ae6ec69ea9146ee88fa01798d4f9fb4fce20b45d4b69`

```dockerfile
```

-	Layers:
	-	`sha256:2bd223ca45ce30aa21ef9e4893d3f6d5e76664df3187b528ba514bfc3074e698`  
		Last Modified: Mon, 09 Feb 2026 19:26:04 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.16.34` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d14b4e6e073e517f963f21c0559e31f24516918793aec5101f9f54fdb9f0466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213846849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e66a9d25fbfaeea39049e873ba70a933548fa4e14c05689f5969557b58f89e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:42 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:42 GMT
ARG VERSION=25.8.16.34
# Mon, 09 Feb 2026 19:25:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:11 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:11 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c82f17864370e6cdf1f007b8c9d11a870b0bc51635fbe6ddd0750d786cec27`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 7.6 MB (7577444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622c812c4902910e844748b2efc310761357b5c4c58f6284c56b48138b137e0`  
		Last Modified: Mon, 09 Feb 2026 19:26:33 GMT  
		Size: 178.0 MB (178015884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a974dcf9c498586c1cf71d7f04714a1a1697617c5230d259730784190625411`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e630840927f4615707188e5b41fd9935a49a3725243f0004732a26bf9d77d33d`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea686a67e9d34b994b4217ba3734212d2047775be05b9db267305b01815deac`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09fdc0bf6bdffeabf8e4fdee1fda69ef034f1910c584a6bc0b2e55a2c0eb64d`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c2bbf122c71596e3af5f65e9c36cf7887f5976b981ebafaf39f4ab2fc2d787`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16.34` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4de1ce8516a189809922bb79d7745209095007d4c91eeccb82e208a521cee9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43520ccaaf175a71da3230708a4d63dd10dbdcebb6b583ed67aa95ec0d84499`

```dockerfile
```

-	Layers:
	-	`sha256:e47505f85dee32c839604eba0c36d1194e1f105f7db3d218029599184fe0f99a`  
		Last Modified: Mon, 09 Feb 2026 19:26:29 GMT  
		Size: 26.3 KB (26256 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.16.34-jammy`

```console
$ docker pull clickhouse@sha256:84920b9a25b5c8a212adcd7a146ad81dfabcc424973dba20f5c59e290a388bd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8.16.34-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f6a1295b2d14d196e527e8409ac4705dd7fe3af88d3f722361f67c3539d42318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228944439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0253b7565919469f5389ca707d1452a06646b0f9d8c5e0b8f269caf615911ddf`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:16 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:16 GMT
ARG VERSION=25.8.16.34
# Mon, 09 Feb 2026 19:25:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:45 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:45 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:45 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99570f0435d34b24aac45231ea0fa7e0a7e0e962b1b9d3cbc9fe0cea69275be6`  
		Last Modified: Mon, 09 Feb 2026 19:26:05 GMT  
		Size: 7.6 MB (7598385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b899fd194a87b9af8c90ccbcef12714f388acf5f9860671060cf352564756222`  
		Last Modified: Mon, 09 Feb 2026 19:26:08 GMT  
		Size: 190.9 MB (190939363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa59f2de6256648b152f31d44fa268453f9c34021e7f1452d87aae78e03581b5`  
		Last Modified: Mon, 09 Feb 2026 19:26:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24efb35ec9916375db74a35833ce83d5881ad8d985f525dc4b9c8cb924e2a2d5`  
		Last Modified: Mon, 09 Feb 2026 19:26:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d40dde76a505ae83db462d188b3407f3f6761d0a87d881ccffb21ed36523cb3`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e965f0ac22f2bf7b9d43dec0dbc8d75b51045c8f909c04f0732300b6731a805a`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26991bc2f6a9d75bb46bb4282d69401547da51270840d5aaec91ab9d54211cc`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16.34-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b2f935903def416f930ab8c0719f47ef2788a3300c32c8f21169f04f0c66774d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83dc69c9ec6ed8cdb73ae6ec69ea9146ee88fa01798d4f9fb4fce20b45d4b69`

```dockerfile
```

-	Layers:
	-	`sha256:2bd223ca45ce30aa21ef9e4893d3f6d5e76664df3187b528ba514bfc3074e698`  
		Last Modified: Mon, 09 Feb 2026 19:26:04 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8.16.34-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d14b4e6e073e517f963f21c0559e31f24516918793aec5101f9f54fdb9f0466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213846849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e66a9d25fbfaeea39049e873ba70a933548fa4e14c05689f5969557b58f89e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:42 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:42 GMT
ARG VERSION=25.8.16.34
# Mon, 09 Feb 2026 19:25:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:11 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:11 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c82f17864370e6cdf1f007b8c9d11a870b0bc51635fbe6ddd0750d786cec27`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 7.6 MB (7577444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622c812c4902910e844748b2efc310761357b5c4c58f6284c56b48138b137e0`  
		Last Modified: Mon, 09 Feb 2026 19:26:33 GMT  
		Size: 178.0 MB (178015884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a974dcf9c498586c1cf71d7f04714a1a1697617c5230d259730784190625411`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e630840927f4615707188e5b41fd9935a49a3725243f0004732a26bf9d77d33d`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea686a67e9d34b994b4217ba3734212d2047775be05b9db267305b01815deac`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09fdc0bf6bdffeabf8e4fdee1fda69ef034f1910c584a6bc0b2e55a2c0eb64d`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c2bbf122c71596e3af5f65e9c36cf7887f5976b981ebafaf39f4ab2fc2d787`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8.16.34-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4de1ce8516a189809922bb79d7745209095007d4c91eeccb82e208a521cee9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43520ccaaf175a71da3230708a4d63dd10dbdcebb6b583ed67aa95ec0d84499`

```dockerfile
```

-	Layers:
	-	`sha256:e47505f85dee32c839604eba0c36d1194e1f105f7db3d218029599184fe0f99a`  
		Last Modified: Mon, 09 Feb 2026 19:26:29 GMT  
		Size: 26.3 KB (26256 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1`

```console
$ docker pull clickhouse@sha256:f40149306cd4b24706543ec865f6586f0b2e19593ef452937a93e208c41582cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1` - linux; amd64

```console
$ docker pull clickhouse@sha256:5641a2d9ee1fd5f3b87e4c3791e789af49408485f8af2ae0bf236c1f70ed80f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (245999619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc2d570a8ce11f3d3cf8cb4f3f7ed3085ddaed6eeb434646b61a0815af3bf60`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:22 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:22 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:22 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:22 GMT
ARG VERSION=26.1.2.11
# Mon, 09 Feb 2026 19:25:22 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:48 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:48 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e89d4c4224633307e650aa84433a6b660f8c2de011f067d18c9fb9882dd7662`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 7.6 MB (7598338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4555bda1b16194a8afdbf3ee2ffc89776df2780313675c593d57849048881e78`  
		Last Modified: Mon, 09 Feb 2026 19:26:18 GMT  
		Size: 208.0 MB (207994566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e487d6fc22f1db13b113aea307c4a285b7d1565309f0a89841431a2f1d9559`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e805883a9bc2ce37b0d1e054dcf41009c6c6ab11b048312cc2c732e571f635`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8568ef8638f6dd5e43b02e60f145aa7680d26231e997bcb7b50254a8d769158f`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8538dd4d75882af1d3314d18fe7cff15bb4b656109c388c66ba7321746186`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53d39fb8b80b58a32696e4ab206c796183a88b0714f1a28c01ff8ebe5c76011`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b998b53c7af9e65241adc5c53da8aa047530a418b21b9841f7057714c2b27f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2886d5b296d804972fe7e3460fa17713561b9cd25e2df2285403346e8240e3`

```dockerfile
```

-	Layers:
	-	`sha256:49762147f6c10714b76bc6dfc3596cb61281ca6faf424f49183530623289b50f`  
		Last Modified: Mon, 09 Feb 2026 19:26:13 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:af0cf9c476b5bccc7474265c9cd3f96c9e797dc6420d0bcbc4b91c0490c1646a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228202926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3bfb5b00ad134d3c22f39a98455a957673ee2cd557c62a20a34af4076dc6d1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:24:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:24:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:24:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:24:56 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:24:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:24:56 GMT
ARG VERSION=26.1.2.11
# Mon, 09 Feb 2026 19:24:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:22 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:22 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4be340bb68d631ec053fdd22bb25e392f2182b948c76f0bf194d97f14dd23`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 7.6 MB (7577485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5673c095c7228070230e529edc432510d181541dc395dabe669cbf9fcb50f9`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 192.4 MB (192371892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6547e30cef57b8bf28884c5d3f6b20615badf2ea5036f3ea5bdad80381fc003`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e68d9aad136559131eb162de41cb3d5af32a2788db468740ca2bbb6c324b78`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7606d74fee863b37b104cc5601df85f3fe1a163f781d340d071e45c58a32305e`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001ab28888118522ef3090ef0466812c368d1c3cbf31daabc22d634398675a45`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a26974a34bad1188a59c097a3c265e09a99ecd7f0ba498402be9bca5ec75951`  
		Last Modified: Mon, 09 Feb 2026 19:25:46 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7bf8744c8924d27bc1357a25a958694671484b62d206afe8937438f41e3196c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f57209a5bbfd75aec4280fcd7c56122cda950a1fe25f7c31fd1f4b7be5799db`

```dockerfile
```

-	Layers:
	-	`sha256:0d6e62cc939f2ab313258f38818ed626298b6ad888b512b2d471eb7b3523059a`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1-jammy`

```console
$ docker pull clickhouse@sha256:f40149306cd4b24706543ec865f6586f0b2e19593ef452937a93e208c41582cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:5641a2d9ee1fd5f3b87e4c3791e789af49408485f8af2ae0bf236c1f70ed80f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (245999619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc2d570a8ce11f3d3cf8cb4f3f7ed3085ddaed6eeb434646b61a0815af3bf60`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:22 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:22 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:22 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:22 GMT
ARG VERSION=26.1.2.11
# Mon, 09 Feb 2026 19:25:22 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:48 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:48 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e89d4c4224633307e650aa84433a6b660f8c2de011f067d18c9fb9882dd7662`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 7.6 MB (7598338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4555bda1b16194a8afdbf3ee2ffc89776df2780313675c593d57849048881e78`  
		Last Modified: Mon, 09 Feb 2026 19:26:18 GMT  
		Size: 208.0 MB (207994566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e487d6fc22f1db13b113aea307c4a285b7d1565309f0a89841431a2f1d9559`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e805883a9bc2ce37b0d1e054dcf41009c6c6ab11b048312cc2c732e571f635`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8568ef8638f6dd5e43b02e60f145aa7680d26231e997bcb7b50254a8d769158f`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8538dd4d75882af1d3314d18fe7cff15bb4b656109c388c66ba7321746186`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53d39fb8b80b58a32696e4ab206c796183a88b0714f1a28c01ff8ebe5c76011`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b998b53c7af9e65241adc5c53da8aa047530a418b21b9841f7057714c2b27f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2886d5b296d804972fe7e3460fa17713561b9cd25e2df2285403346e8240e3`

```dockerfile
```

-	Layers:
	-	`sha256:49762147f6c10714b76bc6dfc3596cb61281ca6faf424f49183530623289b50f`  
		Last Modified: Mon, 09 Feb 2026 19:26:13 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:af0cf9c476b5bccc7474265c9cd3f96c9e797dc6420d0bcbc4b91c0490c1646a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228202926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3bfb5b00ad134d3c22f39a98455a957673ee2cd557c62a20a34af4076dc6d1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:24:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:24:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:24:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:24:56 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:24:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:24:56 GMT
ARG VERSION=26.1.2.11
# Mon, 09 Feb 2026 19:24:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:22 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:22 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4be340bb68d631ec053fdd22bb25e392f2182b948c76f0bf194d97f14dd23`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 7.6 MB (7577485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5673c095c7228070230e529edc432510d181541dc395dabe669cbf9fcb50f9`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 192.4 MB (192371892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6547e30cef57b8bf28884c5d3f6b20615badf2ea5036f3ea5bdad80381fc003`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e68d9aad136559131eb162de41cb3d5af32a2788db468740ca2bbb6c324b78`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7606d74fee863b37b104cc5601df85f3fe1a163f781d340d071e45c58a32305e`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001ab28888118522ef3090ef0466812c368d1c3cbf31daabc22d634398675a45`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a26974a34bad1188a59c097a3c265e09a99ecd7f0ba498402be9bca5ec75951`  
		Last Modified: Mon, 09 Feb 2026 19:25:46 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7bf8744c8924d27bc1357a25a958694671484b62d206afe8937438f41e3196c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f57209a5bbfd75aec4280fcd7c56122cda950a1fe25f7c31fd1f4b7be5799db`

```dockerfile
```

-	Layers:
	-	`sha256:0d6e62cc939f2ab313258f38818ed626298b6ad888b512b2d471eb7b3523059a`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.2`

```console
$ docker pull clickhouse@sha256:f40149306cd4b24706543ec865f6586f0b2e19593ef452937a93e208c41582cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.2` - linux; amd64

```console
$ docker pull clickhouse@sha256:5641a2d9ee1fd5f3b87e4c3791e789af49408485f8af2ae0bf236c1f70ed80f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (245999619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc2d570a8ce11f3d3cf8cb4f3f7ed3085ddaed6eeb434646b61a0815af3bf60`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:22 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:22 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:22 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:22 GMT
ARG VERSION=26.1.2.11
# Mon, 09 Feb 2026 19:25:22 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:48 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:48 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e89d4c4224633307e650aa84433a6b660f8c2de011f067d18c9fb9882dd7662`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 7.6 MB (7598338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4555bda1b16194a8afdbf3ee2ffc89776df2780313675c593d57849048881e78`  
		Last Modified: Mon, 09 Feb 2026 19:26:18 GMT  
		Size: 208.0 MB (207994566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e487d6fc22f1db13b113aea307c4a285b7d1565309f0a89841431a2f1d9559`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e805883a9bc2ce37b0d1e054dcf41009c6c6ab11b048312cc2c732e571f635`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8568ef8638f6dd5e43b02e60f145aa7680d26231e997bcb7b50254a8d769158f`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8538dd4d75882af1d3314d18fe7cff15bb4b656109c388c66ba7321746186`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53d39fb8b80b58a32696e4ab206c796183a88b0714f1a28c01ff8ebe5c76011`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b998b53c7af9e65241adc5c53da8aa047530a418b21b9841f7057714c2b27f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2886d5b296d804972fe7e3460fa17713561b9cd25e2df2285403346e8240e3`

```dockerfile
```

-	Layers:
	-	`sha256:49762147f6c10714b76bc6dfc3596cb61281ca6faf424f49183530623289b50f`  
		Last Modified: Mon, 09 Feb 2026 19:26:13 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.2` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:af0cf9c476b5bccc7474265c9cd3f96c9e797dc6420d0bcbc4b91c0490c1646a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228202926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3bfb5b00ad134d3c22f39a98455a957673ee2cd557c62a20a34af4076dc6d1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:24:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:24:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:24:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:24:56 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:24:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:24:56 GMT
ARG VERSION=26.1.2.11
# Mon, 09 Feb 2026 19:24:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:22 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:22 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4be340bb68d631ec053fdd22bb25e392f2182b948c76f0bf194d97f14dd23`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 7.6 MB (7577485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5673c095c7228070230e529edc432510d181541dc395dabe669cbf9fcb50f9`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 192.4 MB (192371892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6547e30cef57b8bf28884c5d3f6b20615badf2ea5036f3ea5bdad80381fc003`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e68d9aad136559131eb162de41cb3d5af32a2788db468740ca2bbb6c324b78`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7606d74fee863b37b104cc5601df85f3fe1a163f781d340d071e45c58a32305e`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001ab28888118522ef3090ef0466812c368d1c3cbf31daabc22d634398675a45`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a26974a34bad1188a59c097a3c265e09a99ecd7f0ba498402be9bca5ec75951`  
		Last Modified: Mon, 09 Feb 2026 19:25:46 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.2` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7bf8744c8924d27bc1357a25a958694671484b62d206afe8937438f41e3196c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f57209a5bbfd75aec4280fcd7c56122cda950a1fe25f7c31fd1f4b7be5799db`

```dockerfile
```

-	Layers:
	-	`sha256:0d6e62cc939f2ab313258f38818ed626298b6ad888b512b2d471eb7b3523059a`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.2-jammy`

```console
$ docker pull clickhouse@sha256:f40149306cd4b24706543ec865f6586f0b2e19593ef452937a93e208c41582cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.2-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:5641a2d9ee1fd5f3b87e4c3791e789af49408485f8af2ae0bf236c1f70ed80f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (245999619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc2d570a8ce11f3d3cf8cb4f3f7ed3085ddaed6eeb434646b61a0815af3bf60`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:22 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:22 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:22 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:22 GMT
ARG VERSION=26.1.2.11
# Mon, 09 Feb 2026 19:25:22 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:48 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:48 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e89d4c4224633307e650aa84433a6b660f8c2de011f067d18c9fb9882dd7662`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 7.6 MB (7598338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4555bda1b16194a8afdbf3ee2ffc89776df2780313675c593d57849048881e78`  
		Last Modified: Mon, 09 Feb 2026 19:26:18 GMT  
		Size: 208.0 MB (207994566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e487d6fc22f1db13b113aea307c4a285b7d1565309f0a89841431a2f1d9559`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e805883a9bc2ce37b0d1e054dcf41009c6c6ab11b048312cc2c732e571f635`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8568ef8638f6dd5e43b02e60f145aa7680d26231e997bcb7b50254a8d769158f`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8538dd4d75882af1d3314d18fe7cff15bb4b656109c388c66ba7321746186`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53d39fb8b80b58a32696e4ab206c796183a88b0714f1a28c01ff8ebe5c76011`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b998b53c7af9e65241adc5c53da8aa047530a418b21b9841f7057714c2b27f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2886d5b296d804972fe7e3460fa17713561b9cd25e2df2285403346e8240e3`

```dockerfile
```

-	Layers:
	-	`sha256:49762147f6c10714b76bc6dfc3596cb61281ca6faf424f49183530623289b50f`  
		Last Modified: Mon, 09 Feb 2026 19:26:13 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.2-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:af0cf9c476b5bccc7474265c9cd3f96c9e797dc6420d0bcbc4b91c0490c1646a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228202926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3bfb5b00ad134d3c22f39a98455a957673ee2cd557c62a20a34af4076dc6d1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:24:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:24:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:24:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:24:56 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:24:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:24:56 GMT
ARG VERSION=26.1.2.11
# Mon, 09 Feb 2026 19:24:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:22 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:22 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4be340bb68d631ec053fdd22bb25e392f2182b948c76f0bf194d97f14dd23`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 7.6 MB (7577485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5673c095c7228070230e529edc432510d181541dc395dabe669cbf9fcb50f9`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 192.4 MB (192371892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6547e30cef57b8bf28884c5d3f6b20615badf2ea5036f3ea5bdad80381fc003`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e68d9aad136559131eb162de41cb3d5af32a2788db468740ca2bbb6c324b78`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7606d74fee863b37b104cc5601df85f3fe1a163f781d340d071e45c58a32305e`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001ab28888118522ef3090ef0466812c368d1c3cbf31daabc22d634398675a45`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a26974a34bad1188a59c097a3c265e09a99ecd7f0ba498402be9bca5ec75951`  
		Last Modified: Mon, 09 Feb 2026 19:25:46 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.2-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7bf8744c8924d27bc1357a25a958694671484b62d206afe8937438f41e3196c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f57209a5bbfd75aec4280fcd7c56122cda950a1fe25f7c31fd1f4b7be5799db`

```dockerfile
```

-	Layers:
	-	`sha256:0d6e62cc939f2ab313258f38818ed626298b6ad888b512b2d471eb7b3523059a`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.2.11`

```console
$ docker pull clickhouse@sha256:f40149306cd4b24706543ec865f6586f0b2e19593ef452937a93e208c41582cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.2.11` - linux; amd64

```console
$ docker pull clickhouse@sha256:5641a2d9ee1fd5f3b87e4c3791e789af49408485f8af2ae0bf236c1f70ed80f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (245999619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc2d570a8ce11f3d3cf8cb4f3f7ed3085ddaed6eeb434646b61a0815af3bf60`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:22 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:22 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:22 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:22 GMT
ARG VERSION=26.1.2.11
# Mon, 09 Feb 2026 19:25:22 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:48 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:48 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e89d4c4224633307e650aa84433a6b660f8c2de011f067d18c9fb9882dd7662`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 7.6 MB (7598338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4555bda1b16194a8afdbf3ee2ffc89776df2780313675c593d57849048881e78`  
		Last Modified: Mon, 09 Feb 2026 19:26:18 GMT  
		Size: 208.0 MB (207994566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e487d6fc22f1db13b113aea307c4a285b7d1565309f0a89841431a2f1d9559`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e805883a9bc2ce37b0d1e054dcf41009c6c6ab11b048312cc2c732e571f635`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8568ef8638f6dd5e43b02e60f145aa7680d26231e997bcb7b50254a8d769158f`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8538dd4d75882af1d3314d18fe7cff15bb4b656109c388c66ba7321746186`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53d39fb8b80b58a32696e4ab206c796183a88b0714f1a28c01ff8ebe5c76011`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.2.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b998b53c7af9e65241adc5c53da8aa047530a418b21b9841f7057714c2b27f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2886d5b296d804972fe7e3460fa17713561b9cd25e2df2285403346e8240e3`

```dockerfile
```

-	Layers:
	-	`sha256:49762147f6c10714b76bc6dfc3596cb61281ca6faf424f49183530623289b50f`  
		Last Modified: Mon, 09 Feb 2026 19:26:13 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.2.11` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:af0cf9c476b5bccc7474265c9cd3f96c9e797dc6420d0bcbc4b91c0490c1646a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228202926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3bfb5b00ad134d3c22f39a98455a957673ee2cd557c62a20a34af4076dc6d1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:24:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:24:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:24:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:24:56 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:24:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:24:56 GMT
ARG VERSION=26.1.2.11
# Mon, 09 Feb 2026 19:24:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:22 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:22 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4be340bb68d631ec053fdd22bb25e392f2182b948c76f0bf194d97f14dd23`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 7.6 MB (7577485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5673c095c7228070230e529edc432510d181541dc395dabe669cbf9fcb50f9`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 192.4 MB (192371892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6547e30cef57b8bf28884c5d3f6b20615badf2ea5036f3ea5bdad80381fc003`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e68d9aad136559131eb162de41cb3d5af32a2788db468740ca2bbb6c324b78`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7606d74fee863b37b104cc5601df85f3fe1a163f781d340d071e45c58a32305e`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001ab28888118522ef3090ef0466812c368d1c3cbf31daabc22d634398675a45`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a26974a34bad1188a59c097a3c265e09a99ecd7f0ba498402be9bca5ec75951`  
		Last Modified: Mon, 09 Feb 2026 19:25:46 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.2.11` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7bf8744c8924d27bc1357a25a958694671484b62d206afe8937438f41e3196c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f57209a5bbfd75aec4280fcd7c56122cda950a1fe25f7c31fd1f4b7be5799db`

```dockerfile
```

-	Layers:
	-	`sha256:0d6e62cc939f2ab313258f38818ed626298b6ad888b512b2d471eb7b3523059a`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:26.1.2.11-jammy`

```console
$ docker pull clickhouse@sha256:f40149306cd4b24706543ec865f6586f0b2e19593ef452937a93e208c41582cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:26.1.2.11-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:5641a2d9ee1fd5f3b87e4c3791e789af49408485f8af2ae0bf236c1f70ed80f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (245999619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc2d570a8ce11f3d3cf8cb4f3f7ed3085ddaed6eeb434646b61a0815af3bf60`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:22 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:22 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:22 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:22 GMT
ARG VERSION=26.1.2.11
# Mon, 09 Feb 2026 19:25:22 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:48 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:48 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e89d4c4224633307e650aa84433a6b660f8c2de011f067d18c9fb9882dd7662`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 7.6 MB (7598338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4555bda1b16194a8afdbf3ee2ffc89776df2780313675c593d57849048881e78`  
		Last Modified: Mon, 09 Feb 2026 19:26:18 GMT  
		Size: 208.0 MB (207994566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e487d6fc22f1db13b113aea307c4a285b7d1565309f0a89841431a2f1d9559`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e805883a9bc2ce37b0d1e054dcf41009c6c6ab11b048312cc2c732e571f635`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8568ef8638f6dd5e43b02e60f145aa7680d26231e997bcb7b50254a8d769158f`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8538dd4d75882af1d3314d18fe7cff15bb4b656109c388c66ba7321746186`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53d39fb8b80b58a32696e4ab206c796183a88b0714f1a28c01ff8ebe5c76011`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.2.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b998b53c7af9e65241adc5c53da8aa047530a418b21b9841f7057714c2b27f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2886d5b296d804972fe7e3460fa17713561b9cd25e2df2285403346e8240e3`

```dockerfile
```

-	Layers:
	-	`sha256:49762147f6c10714b76bc6dfc3596cb61281ca6faf424f49183530623289b50f`  
		Last Modified: Mon, 09 Feb 2026 19:26:13 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:26.1.2.11-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:af0cf9c476b5bccc7474265c9cd3f96c9e797dc6420d0bcbc4b91c0490c1646a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228202926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3bfb5b00ad134d3c22f39a98455a957673ee2cd557c62a20a34af4076dc6d1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:24:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:24:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:24:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:24:56 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:24:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:24:56 GMT
ARG VERSION=26.1.2.11
# Mon, 09 Feb 2026 19:24:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:22 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:22 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4be340bb68d631ec053fdd22bb25e392f2182b948c76f0bf194d97f14dd23`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 7.6 MB (7577485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5673c095c7228070230e529edc432510d181541dc395dabe669cbf9fcb50f9`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 192.4 MB (192371892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6547e30cef57b8bf28884c5d3f6b20615badf2ea5036f3ea5bdad80381fc003`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e68d9aad136559131eb162de41cb3d5af32a2788db468740ca2bbb6c324b78`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7606d74fee863b37b104cc5601df85f3fe1a163f781d340d071e45c58a32305e`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001ab28888118522ef3090ef0466812c368d1c3cbf31daabc22d634398675a45`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a26974a34bad1188a59c097a3c265e09a99ecd7f0ba498402be9bca5ec75951`  
		Last Modified: Mon, 09 Feb 2026 19:25:46 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:26.1.2.11-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7bf8744c8924d27bc1357a25a958694671484b62d206afe8937438f41e3196c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f57209a5bbfd75aec4280fcd7c56122cda950a1fe25f7c31fd1f4b7be5799db`

```dockerfile
```

-	Layers:
	-	`sha256:0d6e62cc939f2ab313258f38818ed626298b6ad888b512b2d471eb7b3523059a`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:f40149306cd4b24706543ec865f6586f0b2e19593ef452937a93e208c41582cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:5641a2d9ee1fd5f3b87e4c3791e789af49408485f8af2ae0bf236c1f70ed80f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (245999619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc2d570a8ce11f3d3cf8cb4f3f7ed3085ddaed6eeb434646b61a0815af3bf60`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:22 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:22 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:22 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:22 GMT
ARG VERSION=26.1.2.11
# Mon, 09 Feb 2026 19:25:22 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:48 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:48 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e89d4c4224633307e650aa84433a6b660f8c2de011f067d18c9fb9882dd7662`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 7.6 MB (7598338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4555bda1b16194a8afdbf3ee2ffc89776df2780313675c593d57849048881e78`  
		Last Modified: Mon, 09 Feb 2026 19:26:18 GMT  
		Size: 208.0 MB (207994566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e487d6fc22f1db13b113aea307c4a285b7d1565309f0a89841431a2f1d9559`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e805883a9bc2ce37b0d1e054dcf41009c6c6ab11b048312cc2c732e571f635`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8568ef8638f6dd5e43b02e60f145aa7680d26231e997bcb7b50254a8d769158f`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8538dd4d75882af1d3314d18fe7cff15bb4b656109c388c66ba7321746186`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53d39fb8b80b58a32696e4ab206c796183a88b0714f1a28c01ff8ebe5c76011`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b998b53c7af9e65241adc5c53da8aa047530a418b21b9841f7057714c2b27f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2886d5b296d804972fe7e3460fa17713561b9cd25e2df2285403346e8240e3`

```dockerfile
```

-	Layers:
	-	`sha256:49762147f6c10714b76bc6dfc3596cb61281ca6faf424f49183530623289b50f`  
		Last Modified: Mon, 09 Feb 2026 19:26:13 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:af0cf9c476b5bccc7474265c9cd3f96c9e797dc6420d0bcbc4b91c0490c1646a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228202926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3bfb5b00ad134d3c22f39a98455a957673ee2cd557c62a20a34af4076dc6d1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:24:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:24:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:24:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:24:56 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:24:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:24:56 GMT
ARG VERSION=26.1.2.11
# Mon, 09 Feb 2026 19:24:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:22 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:22 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4be340bb68d631ec053fdd22bb25e392f2182b948c76f0bf194d97f14dd23`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 7.6 MB (7577485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5673c095c7228070230e529edc432510d181541dc395dabe669cbf9fcb50f9`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 192.4 MB (192371892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6547e30cef57b8bf28884c5d3f6b20615badf2ea5036f3ea5bdad80381fc003`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e68d9aad136559131eb162de41cb3d5af32a2788db468740ca2bbb6c324b78`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7606d74fee863b37b104cc5601df85f3fe1a163f781d340d071e45c58a32305e`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001ab28888118522ef3090ef0466812c368d1c3cbf31daabc22d634398675a45`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a26974a34bad1188a59c097a3c265e09a99ecd7f0ba498402be9bca5ec75951`  
		Last Modified: Mon, 09 Feb 2026 19:25:46 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7bf8744c8924d27bc1357a25a958694671484b62d206afe8937438f41e3196c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f57209a5bbfd75aec4280fcd7c56122cda950a1fe25f7c31fd1f4b7be5799db`

```dockerfile
```

-	Layers:
	-	`sha256:0d6e62cc939f2ab313258f38818ed626298b6ad888b512b2d471eb7b3523059a`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:f40149306cd4b24706543ec865f6586f0b2e19593ef452937a93e208c41582cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:5641a2d9ee1fd5f3b87e4c3791e789af49408485f8af2ae0bf236c1f70ed80f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.0 MB (245999619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfc2d570a8ce11f3d3cf8cb4f3f7ed3085ddaed6eeb434646b61a0815af3bf60`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:22 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:22 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:22 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:22 GMT
ARG VERSION=26.1.2.11
# Mon, 09 Feb 2026 19:25:22 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:46 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:47 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:48 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:48 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:48 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:48 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:48 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e89d4c4224633307e650aa84433a6b660f8c2de011f067d18c9fb9882dd7662`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 7.6 MB (7598338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4555bda1b16194a8afdbf3ee2ffc89776df2780313675c593d57849048881e78`  
		Last Modified: Mon, 09 Feb 2026 19:26:18 GMT  
		Size: 208.0 MB (207994566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e487d6fc22f1db13b113aea307c4a285b7d1565309f0a89841431a2f1d9559`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e805883a9bc2ce37b0d1e054dcf41009c6c6ab11b048312cc2c732e571f635`  
		Last Modified: Mon, 09 Feb 2026 19:26:14 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8568ef8638f6dd5e43b02e60f145aa7680d26231e997bcb7b50254a8d769158f`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e8538dd4d75882af1d3314d18fe7cff15bb4b656109c388c66ba7321746186`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53d39fb8b80b58a32696e4ab206c796183a88b0714f1a28c01ff8ebe5c76011`  
		Last Modified: Mon, 09 Feb 2026 19:26:15 GMT  
		Size: 3.6 KB (3636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b998b53c7af9e65241adc5c53da8aa047530a418b21b9841f7057714c2b27f1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd2886d5b296d804972fe7e3460fa17713561b9cd25e2df2285403346e8240e3`

```dockerfile
```

-	Layers:
	-	`sha256:49762147f6c10714b76bc6dfc3596cb61281ca6faf424f49183530623289b50f`  
		Last Modified: Mon, 09 Feb 2026 19:26:13 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:af0cf9c476b5bccc7474265c9cd3f96c9e797dc6420d0bcbc4b91c0490c1646a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228202926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de3bfb5b00ad134d3c22f39a98455a957673ee2cd557c62a20a34af4076dc6d1`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:24:56 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:24:56 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:24:56 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:24:56 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:24:56 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:24:56 GMT
ARG VERSION=26.1.2.11
# Mon, 09 Feb 2026 19:24:56 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:20 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:21 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:22 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:22 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=26.1.2.11 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:22 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:22 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:22 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:22 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf4be340bb68d631ec053fdd22bb25e392f2182b948c76f0bf194d97f14dd23`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 7.6 MB (7577485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5673c095c7228070230e529edc432510d181541dc395dabe669cbf9fcb50f9`  
		Last Modified: Mon, 09 Feb 2026 19:25:48 GMT  
		Size: 192.4 MB (192371892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6547e30cef57b8bf28884c5d3f6b20615badf2ea5036f3ea5bdad80381fc003`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e68d9aad136559131eb162de41cb3d5af32a2788db468740ca2bbb6c324b78`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7606d74fee863b37b104cc5601df85f3fe1a163f781d340d071e45c58a32305e`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:001ab28888118522ef3090ef0466812c368d1c3cbf31daabc22d634398675a45`  
		Last Modified: Mon, 09 Feb 2026 19:25:45 GMT  
		Size: 364.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a26974a34bad1188a59c097a3c265e09a99ecd7f0ba498402be9bca5ec75951`  
		Last Modified: Mon, 09 Feb 2026 19:25:46 GMT  
		Size: 3.6 KB (3637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:7bf8744c8924d27bc1357a25a958694671484b62d206afe8937438f41e3196c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 KB (26240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f57209a5bbfd75aec4280fcd7c56122cda950a1fe25f7c31fd1f4b7be5799db`

```dockerfile
```

-	Layers:
	-	`sha256:0d6e62cc939f2ab313258f38818ed626298b6ad888b512b2d471eb7b3523059a`  
		Last Modified: Mon, 09 Feb 2026 19:25:44 GMT  
		Size: 26.2 KB (26240 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:84920b9a25b5c8a212adcd7a146ad81dfabcc424973dba20f5c59e290a388bd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:f6a1295b2d14d196e527e8409ac4705dd7fe3af88d3f722361f67c3539d42318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228944439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0253b7565919469f5389ca707d1452a06646b0f9d8c5e0b8f269caf615911ddf`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:16 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:16 GMT
ARG VERSION=25.8.16.34
# Mon, 09 Feb 2026 19:25:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:45 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:45 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:45 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99570f0435d34b24aac45231ea0fa7e0a7e0e962b1b9d3cbc9fe0cea69275be6`  
		Last Modified: Mon, 09 Feb 2026 19:26:05 GMT  
		Size: 7.6 MB (7598385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b899fd194a87b9af8c90ccbcef12714f388acf5f9860671060cf352564756222`  
		Last Modified: Mon, 09 Feb 2026 19:26:08 GMT  
		Size: 190.9 MB (190939363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa59f2de6256648b152f31d44fa268453f9c34021e7f1452d87aae78e03581b5`  
		Last Modified: Mon, 09 Feb 2026 19:26:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24efb35ec9916375db74a35833ce83d5881ad8d985f525dc4b9c8cb924e2a2d5`  
		Last Modified: Mon, 09 Feb 2026 19:26:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d40dde76a505ae83db462d188b3407f3f6761d0a87d881ccffb21ed36523cb3`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e965f0ac22f2bf7b9d43dec0dbc8d75b51045c8f909c04f0732300b6731a805a`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26991bc2f6a9d75bb46bb4282d69401547da51270840d5aaec91ab9d54211cc`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b2f935903def416f930ab8c0719f47ef2788a3300c32c8f21169f04f0c66774d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83dc69c9ec6ed8cdb73ae6ec69ea9146ee88fa01798d4f9fb4fce20b45d4b69`

```dockerfile
```

-	Layers:
	-	`sha256:2bd223ca45ce30aa21ef9e4893d3f6d5e76664df3187b528ba514bfc3074e698`  
		Last Modified: Mon, 09 Feb 2026 19:26:04 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d14b4e6e073e517f963f21c0559e31f24516918793aec5101f9f54fdb9f0466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213846849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e66a9d25fbfaeea39049e873ba70a933548fa4e14c05689f5969557b58f89e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:42 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:42 GMT
ARG VERSION=25.8.16.34
# Mon, 09 Feb 2026 19:25:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:11 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:11 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c82f17864370e6cdf1f007b8c9d11a870b0bc51635fbe6ddd0750d786cec27`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 7.6 MB (7577444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622c812c4902910e844748b2efc310761357b5c4c58f6284c56b48138b137e0`  
		Last Modified: Mon, 09 Feb 2026 19:26:33 GMT  
		Size: 178.0 MB (178015884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a974dcf9c498586c1cf71d7f04714a1a1697617c5230d259730784190625411`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e630840927f4615707188e5b41fd9935a49a3725243f0004732a26bf9d77d33d`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea686a67e9d34b994b4217ba3734212d2047775be05b9db267305b01815deac`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09fdc0bf6bdffeabf8e4fdee1fda69ef034f1910c584a6bc0b2e55a2c0eb64d`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c2bbf122c71596e3af5f65e9c36cf7887f5976b981ebafaf39f4ab2fc2d787`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4de1ce8516a189809922bb79d7745209095007d4c91eeccb82e208a521cee9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43520ccaaf175a71da3230708a4d63dd10dbdcebb6b583ed67aa95ec0d84499`

```dockerfile
```

-	Layers:
	-	`sha256:e47505f85dee32c839604eba0c36d1194e1f105f7db3d218029599184fe0f99a`  
		Last Modified: Mon, 09 Feb 2026 19:26:29 GMT  
		Size: 26.3 KB (26256 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:84920b9a25b5c8a212adcd7a146ad81dfabcc424973dba20f5c59e290a388bd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f6a1295b2d14d196e527e8409ac4705dd7fe3af88d3f722361f67c3539d42318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228944439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0253b7565919469f5389ca707d1452a06646b0f9d8c5e0b8f269caf615911ddf`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:01:41 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:01:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:01:41 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:01:44 GMT
ADD file:b499000226bd9a7c562ffa8eeb86e2d170f2a563310db6c2d79562ab53e5cb6e in / 
# Fri, 09 Jan 2026 07:01:44 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:16 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:16 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:16 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:16 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:16 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:16 GMT
ARG VERSION=25.8.16.34
# Mon, 09 Feb 2026 19:25:16 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:25:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:44 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:25:45 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:25:45 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:25:45 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:25:45 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:25:45 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:25:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6f4ebca3e823b18dac366f72e537b1772bc3522a5c7ae299d6491fb17378410e`  
		Last Modified: Fri, 09 Jan 2026 07:35:56 GMT  
		Size: 29.5 MB (29536667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99570f0435d34b24aac45231ea0fa7e0a7e0e962b1b9d3cbc9fe0cea69275be6`  
		Last Modified: Mon, 09 Feb 2026 19:26:05 GMT  
		Size: 7.6 MB (7598385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b899fd194a87b9af8c90ccbcef12714f388acf5f9860671060cf352564756222`  
		Last Modified: Mon, 09 Feb 2026 19:26:08 GMT  
		Size: 190.9 MB (190939363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa59f2de6256648b152f31d44fa268453f9c34021e7f1452d87aae78e03581b5`  
		Last Modified: Mon, 09 Feb 2026 19:26:04 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24efb35ec9916375db74a35833ce83d5881ad8d985f525dc4b9c8cb924e2a2d5`  
		Last Modified: Mon, 09 Feb 2026 19:26:05 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d40dde76a505ae83db462d188b3407f3f6761d0a87d881ccffb21ed36523cb3`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e965f0ac22f2bf7b9d43dec0dbc8d75b51045c8f909c04f0732300b6731a805a`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26991bc2f6a9d75bb46bb4282d69401547da51270840d5aaec91ab9d54211cc`  
		Last Modified: Mon, 09 Feb 2026 19:26:06 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:b2f935903def416f930ab8c0719f47ef2788a3300c32c8f21169f04f0c66774d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d83dc69c9ec6ed8cdb73ae6ec69ea9146ee88fa01798d4f9fb4fce20b45d4b69`

```dockerfile
```

-	Layers:
	-	`sha256:2bd223ca45ce30aa21ef9e4893d3f6d5e76664df3187b528ba514bfc3074e698`  
		Last Modified: Mon, 09 Feb 2026 19:26:04 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:6d14b4e6e073e517f963f21c0559e31f24516918793aec5101f9f54fdb9f0466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.8 MB (213846849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04e66a9d25fbfaeea39049e873ba70a933548fa4e14c05689f5969557b58f89e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 09 Jan 2026 07:03:27 GMT
ARG RELEASE
# Fri, 09 Jan 2026 07:03:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 09 Jan 2026 07:03:27 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 09 Jan 2026 07:03:30 GMT
ADD file:643ece0a7a3a6026f87ab17e08013e914d8971796eb302cfa051d97af4bf9939 in / 
# Fri, 09 Jan 2026 07:03:30 GMT
CMD ["/bin/bash"]
# Mon, 09 Feb 2026 19:25:42 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Mon, 09 Feb 2026 19:25:42 GMT
ARG apt_archive=http://archive.ubuntu.com
# Mon, 09 Feb 2026 19:25:42 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Mon, 09 Feb 2026 19:25:42 GMT
ARG REPO_CHANNEL=stable
# Mon, 09 Feb 2026 19:25:42 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Mon, 09 Feb 2026 19:25:42 GMT
ARG VERSION=25.8.16.34
# Mon, 09 Feb 2026 19:25:42 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Mon, 09 Feb 2026 19:26:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:09 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
ENV LANG=en_US.UTF-8
# Mon, 09 Feb 2026 19:26:11 GMT
ENV TZ=UTC
# Mon, 09 Feb 2026 19:26:11 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.16.34 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 09 Feb 2026 19:26:11 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Mon, 09 Feb 2026 19:26:11 GMT
VOLUME [/var/lib/clickhouse]
# Mon, 09 Feb 2026 19:26:11 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Mon, 09 Feb 2026 19:26:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:517f43312bfe3b4db0f0f031d8b6deb1aa5616b07fae71fa0d349f9ce451564f`  
		Last Modified: Fri, 09 Jan 2026 07:36:03 GMT  
		Size: 27.4 MB (27383497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c82f17864370e6cdf1f007b8c9d11a870b0bc51635fbe6ddd0750d786cec27`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 7.6 MB (7577444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e622c812c4902910e844748b2efc310761357b5c4c58f6284c56b48138b137e0`  
		Last Modified: Mon, 09 Feb 2026 19:26:33 GMT  
		Size: 178.0 MB (178015884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a974dcf9c498586c1cf71d7f04714a1a1697617c5230d259730784190625411`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e630840927f4615707188e5b41fd9935a49a3725243f0004732a26bf9d77d33d`  
		Last Modified: Mon, 09 Feb 2026 19:26:30 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea686a67e9d34b994b4217ba3734212d2047775be05b9db267305b01815deac`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09fdc0bf6bdffeabf8e4fdee1fda69ef034f1910c584a6bc0b2e55a2c0eb64d`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c2bbf122c71596e3af5f65e9c36cf7887f5976b981ebafaf39f4ab2fc2d787`  
		Last Modified: Mon, 09 Feb 2026 19:26:31 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4de1ce8516a189809922bb79d7745209095007d4c91eeccb82e208a521cee9eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f43520ccaaf175a71da3230708a4d63dd10dbdcebb6b583ed67aa95ec0d84499`

```dockerfile
```

-	Layers:
	-	`sha256:e47505f85dee32c839604eba0c36d1194e1f105f7db3d218029599184fe0f99a`  
		Last Modified: Mon, 09 Feb 2026 19:26:29 GMT  
		Size: 26.3 KB (26256 bytes)  
		MIME: application/vnd.in-toto+json
