<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `clickhouse`

-	[`clickhouse:25.10`](#clickhouse2510)
-	[`clickhouse:25.10-jammy`](#clickhouse2510-jammy)
-	[`clickhouse:25.10.3`](#clickhouse25103)
-	[`clickhouse:25.10.3-jammy`](#clickhouse25103-jammy)
-	[`clickhouse:25.10.3.100`](#clickhouse25103100)
-	[`clickhouse:25.10.3.100-jammy`](#clickhouse25103100-jammy)
-	[`clickhouse:25.11`](#clickhouse2511)
-	[`clickhouse:25.11-jammy`](#clickhouse2511-jammy)
-	[`clickhouse:25.11.1`](#clickhouse25111)
-	[`clickhouse:25.11.1-jammy`](#clickhouse25111-jammy)
-	[`clickhouse:25.11.1.558`](#clickhouse25111558)
-	[`clickhouse:25.11.1.558-jammy`](#clickhouse25111558-jammy)
-	[`clickhouse:25.3`](#clickhouse253)
-	[`clickhouse:25.3-jammy`](#clickhouse253-jammy)
-	[`clickhouse:25.3.9`](#clickhouse2539)
-	[`clickhouse:25.3.9-jammy`](#clickhouse2539-jammy)
-	[`clickhouse:25.3.9.72`](#clickhouse253972)
-	[`clickhouse:25.3.9.72-jammy`](#clickhouse253972-jammy)
-	[`clickhouse:25.8`](#clickhouse258)
-	[`clickhouse:25.8-jammy`](#clickhouse258-jammy)
-	[`clickhouse:25.8.12`](#clickhouse25812)
-	[`clickhouse:25.8.12-jammy`](#clickhouse25812-jammy)
-	[`clickhouse:25.8.12.129`](#clickhouse25812129)
-	[`clickhouse:25.8.12.129-jammy`](#clickhouse25812129-jammy)
-	[`clickhouse:25.9`](#clickhouse259)
-	[`clickhouse:25.9-jammy`](#clickhouse259-jammy)
-	[`clickhouse:25.9.6`](#clickhouse2596)
-	[`clickhouse:25.9.6-jammy`](#clickhouse2596-jammy)
-	[`clickhouse:25.9.6.117`](#clickhouse2596117)
-	[`clickhouse:25.9.6.117-jammy`](#clickhouse2596117-jammy)
-	[`clickhouse:jammy`](#clickhousejammy)
-	[`clickhouse:latest`](#clickhouselatest)
-	[`clickhouse:lts`](#clickhouselts)
-	[`clickhouse:lts-jammy`](#clickhouselts-jammy)

## `clickhouse:25.10`

```console
$ docker pull clickhouse@sha256:c9739650884bcc5dd109c283ce545b87d58c0f751880aa425170a59604aec341
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10` - linux; amd64

```console
$ docker pull clickhouse@sha256:f0d8c09cd53e9787cb3ee8f7e8e7cfde488fdddcb0b0502469b80b3b8a84c4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231983240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2269ab9ff71a3eb770715c7a3fd75761efe8ef23a6c788abaa57f2e3cb78562`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:36 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 23:09:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:10:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:10:03 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:10:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:10:03 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:10:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:10:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bd02d54aca9e4b5dc021fa7f9e576a07e5be62fc7ee172d0ed4137944cacc9`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 7.6 MB (7598588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6316601fd9c34b60c5ca2605fa55d8290e2bd5ac69198cd0a53467a567f7fc83`  
		Last Modified: Fri, 14 Nov 2025 01:49:55 GMT  
		Size: 194.0 MB (193977827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba39390138026777c687e3508ed8fd34055ace99ecec73f69c797cafd8492cc5`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276dfe45586cc645faa4c6655eebeeee38ea04261463b342d877bb60f895e787`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5975ad1545a1b9982f545077922f5494e5c50dde1ed46614c6aa7b1ccac1dca1`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07b39058858cb54734eaea1eb73e6efcc4ab04b4dc823c4d49ae39c219cd92e`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abed04583b3f8484627b7110037ce3ab26c7588a582f0da788ee9733c83ff42`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ae05d5e36eeccc46858a9c47b42e6578e2fdcb657160f8fc633a3969c05d158d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604d4c960d9c1b2ffe0e50ce35b612b69e231b9afad0c7f6da252c01c5a4f6e6`

```dockerfile
```

-	Layers:
	-	`sha256:130306bcdc0b3daacdfe7da0deb2a61f1322af37824c618b9d715bde6aa88ba3`  
		Last Modified: Fri, 14 Nov 2025 01:49:24 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:eeb67abeca6c00dd7fac755651c7ed2042118211e8ee5e999ba9cdfdf56aaa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216505816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4601fbc006cdf774790f0afb3a7ab6d279f4acf3f6380c3ab0ff11a9bca50c9b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:31 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 23:09:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:09:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:09:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:09:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:09:58 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:09:58 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:09:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:09:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:09:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:09:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:09:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41daf4310e4fd0bfd906fb1dd237436605457dfdf700a83ca5ae05cfccbe3813`  
		Last Modified: Thu, 13 Nov 2025 23:10:28 GMT  
		Size: 7.6 MB (7576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0f5ce5c4571b4cd2464c78cbcd31672ad12226725a8e1232e8c3ef3620f9e0`  
		Last Modified: Fri, 14 Nov 2025 01:49:52 GMT  
		Size: 180.7 MB (180675112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e8a51714ff93bb140e12b0158c088b6cde1651b653c1e455860479be6303b3`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a87b3cb86dd50e65da599ed4a968edc62c5594830a198faad91aa3dcabcc814`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e50b7ab24f69fdcd396dd7a078c175c8467d0556dbc8b3fcc5380d6706706d8`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcd2bca9e63b0ebf70cbb92ffe0393da57cf1fb923a96941174aeb3097fcec6`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112adfbc3ee3dc6c7d4917a8ce15830879e6ca2aaeaeb47fa47375bc0c20b711`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10` - unknown; unknown

```console
$ docker pull clickhouse@sha256:409797aa5d0365a362df23fc70f1d4ce92527bb13e6286b7c888e5248ab34776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cf6e4289fb787eb33803b732451b0a765a8ddcc8f98c1a84d2f72a690e44f7`

```dockerfile
```

-	Layers:
	-	`sha256:d4f623fa03cf7b7f07af675778466cf0ce1e0569ca834dc8872842cbdd413a01`  
		Last Modified: Fri, 14 Nov 2025 01:49:27 GMT  
		Size: 26.3 KB (26258 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10-jammy`

```console
$ docker pull clickhouse@sha256:c9739650884bcc5dd109c283ce545b87d58c0f751880aa425170a59604aec341
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.10-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f0d8c09cd53e9787cb3ee8f7e8e7cfde488fdddcb0b0502469b80b3b8a84c4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231983240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2269ab9ff71a3eb770715c7a3fd75761efe8ef23a6c788abaa57f2e3cb78562`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:36 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 23:09:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:10:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:10:03 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:10:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:10:03 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:10:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:10:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bd02d54aca9e4b5dc021fa7f9e576a07e5be62fc7ee172d0ed4137944cacc9`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 7.6 MB (7598588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6316601fd9c34b60c5ca2605fa55d8290e2bd5ac69198cd0a53467a567f7fc83`  
		Last Modified: Fri, 14 Nov 2025 01:49:55 GMT  
		Size: 194.0 MB (193977827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba39390138026777c687e3508ed8fd34055ace99ecec73f69c797cafd8492cc5`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276dfe45586cc645faa4c6655eebeeee38ea04261463b342d877bb60f895e787`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5975ad1545a1b9982f545077922f5494e5c50dde1ed46614c6aa7b1ccac1dca1`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07b39058858cb54734eaea1eb73e6efcc4ab04b4dc823c4d49ae39c219cd92e`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abed04583b3f8484627b7110037ce3ab26c7588a582f0da788ee9733c83ff42`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ae05d5e36eeccc46858a9c47b42e6578e2fdcb657160f8fc633a3969c05d158d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604d4c960d9c1b2ffe0e50ce35b612b69e231b9afad0c7f6da252c01c5a4f6e6`

```dockerfile
```

-	Layers:
	-	`sha256:130306bcdc0b3daacdfe7da0deb2a61f1322af37824c618b9d715bde6aa88ba3`  
		Last Modified: Fri, 14 Nov 2025 01:49:24 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.10-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:eeb67abeca6c00dd7fac755651c7ed2042118211e8ee5e999ba9cdfdf56aaa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216505816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4601fbc006cdf774790f0afb3a7ab6d279f4acf3f6380c3ab0ff11a9bca50c9b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:31 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 23:09:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:09:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:09:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:09:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:09:58 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:09:58 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:09:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:09:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:09:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:09:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:09:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41daf4310e4fd0bfd906fb1dd237436605457dfdf700a83ca5ae05cfccbe3813`  
		Last Modified: Thu, 13 Nov 2025 23:10:28 GMT  
		Size: 7.6 MB (7576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0f5ce5c4571b4cd2464c78cbcd31672ad12226725a8e1232e8c3ef3620f9e0`  
		Last Modified: Fri, 14 Nov 2025 01:49:52 GMT  
		Size: 180.7 MB (180675112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e8a51714ff93bb140e12b0158c088b6cde1651b653c1e455860479be6303b3`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a87b3cb86dd50e65da599ed4a968edc62c5594830a198faad91aa3dcabcc814`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e50b7ab24f69fdcd396dd7a078c175c8467d0556dbc8b3fcc5380d6706706d8`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcd2bca9e63b0ebf70cbb92ffe0393da57cf1fb923a96941174aeb3097fcec6`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112adfbc3ee3dc6c7d4917a8ce15830879e6ca2aaeaeb47fa47375bc0c20b711`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.10-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:409797aa5d0365a362df23fc70f1d4ce92527bb13e6286b7c888e5248ab34776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cf6e4289fb787eb33803b732451b0a765a8ddcc8f98c1a84d2f72a690e44f7`

```dockerfile
```

-	Layers:
	-	`sha256:d4f623fa03cf7b7f07af675778466cf0ce1e0569ca834dc8872842cbdd413a01`  
		Last Modified: Fri, 14 Nov 2025 01:49:27 GMT  
		Size: 26.3 KB (26258 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.10.3`

**does not exist** (yet?)

## `clickhouse:25.10.3-jammy`

**does not exist** (yet?)

## `clickhouse:25.10.3.100`

**does not exist** (yet?)

## `clickhouse:25.10.3.100-jammy`

**does not exist** (yet?)

## `clickhouse:25.11`

**does not exist** (yet?)

## `clickhouse:25.11-jammy`

**does not exist** (yet?)

## `clickhouse:25.11.1`

**does not exist** (yet?)

## `clickhouse:25.11.1-jammy`

**does not exist** (yet?)

## `clickhouse:25.11.1.558`

**does not exist** (yet?)

## `clickhouse:25.11.1.558-jammy`

**does not exist** (yet?)

## `clickhouse:25.3`

```console
$ docker pull clickhouse@sha256:509f40d59a36806c386658dbfdc8d71acf8ce7deea1026c321b0f84e17bf3dde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3` - linux; amd64

```console
$ docker pull clickhouse@sha256:5d9c64240bc560de8e8d9c93140cc4359c0ff304b07a7cd1c2679567b3b94fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205506934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e715b2066fd4bc812eef8c6324d86df70fbaaf77c7cd56eef3d72f90bdfd5e96`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:07 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:11:07 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:11:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:11:07 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:11:07 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:11:07 GMT
ARG VERSION=25.3.8.23
# Thu, 13 Nov 2025 23:11:07 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:11:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:11:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:32 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:11:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:11:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:11:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:11:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:11:33 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:11:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:11:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7b8f20c35aa726a2a2d693d7e36f83cd59bbd450d9653953f9f1af39a61f8`  
		Last Modified: Thu, 13 Nov 2025 23:12:06 GMT  
		Size: 7.2 MB (7151720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db321aa3bf519ce0487594eaf55d0049ee38917776e5cd4f923bb7c7bff5a8fb`  
		Last Modified: Fri, 14 Nov 2025 01:50:08 GMT  
		Size: 167.9 MB (167948167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20762d915b29677310eb3d1a13acc05534f07d27b821aba037f684bd5128107`  
		Last Modified: Thu, 13 Nov 2025 23:12:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c28d9dea9befa8041b5be636cf3baef8a47a4fca4c897f9e16f8e2376ba906b`  
		Last Modified: Thu, 13 Nov 2025 23:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3672535be501e8c0a4fd0529a10574401767676c08ce99ba3839513e677b27`  
		Last Modified: Thu, 13 Nov 2025 23:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb61afb15d225fdf6c7b8be260fff3299a812b446ff177099fcf99211bbab71`  
		Last Modified: Thu, 13 Nov 2025 23:12:03 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a580ac5e62da00358c0a12a1bc317d4078be64a3ed4e9ae617d70215cbc88b84`  
		Last Modified: Thu, 13 Nov 2025 23:12:03 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c2ad3d31d32160099b67ac0ffff34057a8a6044135047b81d77719932b284caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615da9764c3834d821b216e5d8af1a5369637d3898c86ec6eea43b4e5dca26c0`

```dockerfile
```

-	Layers:
	-	`sha256:ccfb716f60bfc42a6ab508acc23cbd397cb5579c0a6e9df55b2d929fb6dcc4d5`  
		Last Modified: Fri, 14 Nov 2025 01:49:41 GMT  
		Size: 25.2 KB (25220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:76434c561f32b1e9c8bfe9c0c59ad59c3d980c9eba57ed0dd311f340494f67e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192984230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32b246c85a9f2e2ada3e7e0e6ac3de932161eacd9c3d3d7b8a13219cd3bc1b4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:11:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:11:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:11:19 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:11:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:11:19 GMT
ARG VERSION=25.3.8.23
# Thu, 13 Nov 2025 23:11:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:11:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:11:51 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:51 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:11:51 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:11:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:11:51 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:11:51 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:11:51 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6912feaefe3b412f987ceed3719d12bfec150caa10588edf69c3799a7a6a5dfa`  
		Last Modified: Thu, 13 Nov 2025 23:12:17 GMT  
		Size: 7.1 MB (7127279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c7c7cfeb2d9c62f8ab55587dab6536b17e58f8250beb569c7ae5ee3043454b`  
		Last Modified: Fri, 14 Nov 2025 01:50:11 GMT  
		Size: 157.6 MB (157602826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad1d1737dee66712f2b8b88c4cd8c4fe10ee8aabfee88c2b951f0447f97f2a4`  
		Last Modified: Thu, 13 Nov 2025 23:12:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff01d9c21ecad113fd960818930c51712828d4b1b6d85202a8cd206756b68be6`  
		Last Modified: Thu, 13 Nov 2025 23:12:17 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7743bacd828b809c1f642f45bf849918632d8c5965adef92c9cdb94337b7686`  
		Last Modified: Thu, 13 Nov 2025 23:12:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191a1946cf2cb9b748060c8dd52e7011c58452d5cfe54902b007ea8eae7805da`  
		Last Modified: Thu, 13 Nov 2025 23:12:17 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e33a0216ac1156c05ce1982ddee3e11e8bf3cb092c202ef574a92a5f6b29cf0`  
		Last Modified: Thu, 13 Nov 2025 23:12:17 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d100812de32e2ba40ef59741802152e948e35cde3d5c464bf3a47deaa653a6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975f830118bf5a968f7661b5e189c3b7da15f3f207d6c75f7a9ebace1248e389`

```dockerfile
```

-	Layers:
	-	`sha256:41d71eb3eb86ca1ef77d6f74942baa4b152be0dd4edff47206e2a3e2612fbaa8`  
		Last Modified: Fri, 14 Nov 2025 01:49:44 GMT  
		Size: 25.4 KB (25408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3-jammy`

```console
$ docker pull clickhouse@sha256:509f40d59a36806c386658dbfdc8d71acf8ce7deea1026c321b0f84e17bf3dde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.3-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:5d9c64240bc560de8e8d9c93140cc4359c0ff304b07a7cd1c2679567b3b94fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205506934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e715b2066fd4bc812eef8c6324d86df70fbaaf77c7cd56eef3d72f90bdfd5e96`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:07 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:11:07 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:11:07 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:11:07 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:11:07 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:11:07 GMT
ARG VERSION=25.3.8.23
# Thu, 13 Nov 2025 23:11:07 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:11:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:11:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:32 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:11:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:11:33 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:11:33 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:11:33 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:11:33 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:11:33 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:11:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84a7b8f20c35aa726a2a2d693d7e36f83cd59bbd450d9653953f9f1af39a61f8`  
		Last Modified: Thu, 13 Nov 2025 23:12:06 GMT  
		Size: 7.2 MB (7151720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db321aa3bf519ce0487594eaf55d0049ee38917776e5cd4f923bb7c7bff5a8fb`  
		Last Modified: Fri, 14 Nov 2025 01:50:08 GMT  
		Size: 167.9 MB (167948167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20762d915b29677310eb3d1a13acc05534f07d27b821aba037f684bd5128107`  
		Last Modified: Thu, 13 Nov 2025 23:12:03 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c28d9dea9befa8041b5be636cf3baef8a47a4fca4c897f9e16f8e2376ba906b`  
		Last Modified: Thu, 13 Nov 2025 23:12:03 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3672535be501e8c0a4fd0529a10574401767676c08ce99ba3839513e677b27`  
		Last Modified: Thu, 13 Nov 2025 23:12:03 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb61afb15d225fdf6c7b8be260fff3299a812b446ff177099fcf99211bbab71`  
		Last Modified: Thu, 13 Nov 2025 23:12:03 GMT  
		Size: 362.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a580ac5e62da00358c0a12a1bc317d4078be64a3ed4e9ae617d70215cbc88b84`  
		Last Modified: Thu, 13 Nov 2025 23:12:03 GMT  
		Size: 3.8 KB (3835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:c2ad3d31d32160099b67ac0ffff34057a8a6044135047b81d77719932b284caa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.2 KB (25220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615da9764c3834d821b216e5d8af1a5369637d3898c86ec6eea43b4e5dca26c0`

```dockerfile
```

-	Layers:
	-	`sha256:ccfb716f60bfc42a6ab508acc23cbd397cb5579c0a6e9df55b2d929fb6dcc4d5`  
		Last Modified: Fri, 14 Nov 2025 01:49:41 GMT  
		Size: 25.2 KB (25220 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.3-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:76434c561f32b1e9c8bfe9c0c59ad59c3d980c9eba57ed0dd311f340494f67e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.0 MB (192984230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d32b246c85a9f2e2ada3e7e0e6ac3de932161eacd9c3d3d7b8a13219cd3bc1b4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:11:19 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:11:19 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:11:19 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         ca-certificates         locales         tzdata         wget     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:11:19 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:11:19 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:11:19 GMT
ARG VERSION=25.3.8.23
# Thu, 13 Nov 2025 23:11:19 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:11:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:50 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:11:51 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:51 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:11:51 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.3.8.23 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:11:51 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:11:51 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:11:51 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:11:51 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:11:51 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:11:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6912feaefe3b412f987ceed3719d12bfec150caa10588edf69c3799a7a6a5dfa`  
		Last Modified: Thu, 13 Nov 2025 23:12:17 GMT  
		Size: 7.1 MB (7127279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c7c7cfeb2d9c62f8ab55587dab6536b17e58f8250beb569c7ae5ee3043454b`  
		Last Modified: Fri, 14 Nov 2025 01:50:11 GMT  
		Size: 157.6 MB (157602826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad1d1737dee66712f2b8b88c4cd8c4fe10ee8aabfee88c2b951f0447f97f2a4`  
		Last Modified: Thu, 13 Nov 2025 23:12:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff01d9c21ecad113fd960818930c51712828d4b1b6d85202a8cd206756b68be6`  
		Last Modified: Thu, 13 Nov 2025 23:12:17 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7743bacd828b809c1f642f45bf849918632d8c5965adef92c9cdb94337b7686`  
		Last Modified: Thu, 13 Nov 2025 23:12:17 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191a1946cf2cb9b748060c8dd52e7011c58452d5cfe54902b007ea8eae7805da`  
		Last Modified: Thu, 13 Nov 2025 23:12:17 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e33a0216ac1156c05ce1982ddee3e11e8bf3cb092c202ef574a92a5f6b29cf0`  
		Last Modified: Thu, 13 Nov 2025 23:12:17 GMT  
		Size: 3.8 KB (3836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.3-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:d100812de32e2ba40ef59741802152e948e35cde3d5c464bf3a47deaa653a6b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:975f830118bf5a968f7661b5e189c3b7da15f3f207d6c75f7a9ebace1248e389`

```dockerfile
```

-	Layers:
	-	`sha256:41d71eb3eb86ca1ef77d6f74942baa4b152be0dd4edff47206e2a3e2612fbaa8`  
		Last Modified: Fri, 14 Nov 2025 01:49:44 GMT  
		Size: 25.4 KB (25408 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.3.9`

**does not exist** (yet?)

## `clickhouse:25.3.9-jammy`

**does not exist** (yet?)

## `clickhouse:25.3.9.72`

**does not exist** (yet?)

## `clickhouse:25.3.9.72-jammy`

**does not exist** (yet?)

## `clickhouse:25.8`

```console
$ docker pull clickhouse@sha256:6aef4b3c7197eadee1ebd1c8d6f69b99f33ec3c6c0f11c72eba0b840d87b5c11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8` - linux; amd64

```console
$ docker pull clickhouse@sha256:7cc58df1643fd52b0ca3383515fd8f31d1f139d67915649c969797cad6a354af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227833996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7aeb0043cc0bf471c3bfe8d6e479602da58acba8e3209f6765d3d4ddfe931f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:39 GMT
ARG VERSION=25.8.11.66
# Thu, 13 Nov 2025 23:09:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:27 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:11:27 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:11:27 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:11:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49009f2b2c2df1a49119795bda88cde6e506edbff6400db80ecd8d86d116b501`  
		Last Modified: Thu, 13 Nov 2025 23:10:39 GMT  
		Size: 7.6 MB (7598523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005342a1838b259d962a4cf009039849846ccc8ea03343a19a652ed39af17fe6`  
		Last Modified: Fri, 14 Nov 2025 01:50:41 GMT  
		Size: 189.8 MB (189828651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece9f4b41dc9b366993db6769e2ccbabaedc53c61f118a490f71226b4109c2b8`  
		Last Modified: Thu, 13 Nov 2025 23:11:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df89e3dd735bdb60842d324ca69a0cdf08ea627d5715954be9c02a7bddc083fd`  
		Last Modified: Thu, 13 Nov 2025 23:11:59 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d540a46cec9e08a70070c5473f907ef9ebd343b1455e35ead22101f33f16d5aa`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13489c6a19ffae6ca4a1a697997abfea421d97dc0e4d329cfdec851a1a58dc8`  
		Last Modified: Thu, 13 Nov 2025 23:11:59 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2669082c40680a175603060ead5872da333f97d1adce6e9e5053915731f29727`  
		Last Modified: Thu, 13 Nov 2025 23:11:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bcd7a2a953ddb47c85d97e4e32ba098dab2a4efd2cc7966bfdd03c31009de2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468fd697778fed7af280221c44238083efc701a93d2852f0d33bcf1c55d14988`

```dockerfile
```

-	Layers:
	-	`sha256:3f0ac54eef11d20388b7f190f1980fd3456d080d2931f37a9d1d075ac0661437`  
		Last Modified: Fri, 14 Nov 2025 01:49:59 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e55a58f599f187e7158d26961cb7da1033e3787999595aae7ff8f01ba2fcd741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212646216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b13d2311cccbdb9a36bcd1f7f5c229d955417df764572854968cee1ad2d2903`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:31 GMT
ARG VERSION=25.8.11.66
# Thu, 13 Nov 2025 23:09:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:27 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:11:27 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:11:27 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:11:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41daf4310e4fd0bfd906fb1dd237436605457dfdf700a83ca5ae05cfccbe3813`  
		Last Modified: Thu, 13 Nov 2025 23:10:28 GMT  
		Size: 7.6 MB (7576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69beadc0132fd0ac430847591b7fc587c7315d8c02b468441b0d152bdb69849f`  
		Last Modified: Fri, 14 Nov 2025 01:50:43 GMT  
		Size: 176.8 MB (176815517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3de0d633a907044d9de2a16b105e20461f6de9c5f7e8e53aad3f962f6447e7`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142026ec3e591d8ec720b560cb7dff225329e0b6188d6c182f25a64dff3b81bc`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d540a46cec9e08a70070c5473f907ef9ebd343b1455e35ead22101f33f16d5aa`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2345173a6e1bee0c60380913799dfbbe2556aba6ca21d90e069c7ab1eeb5267`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b6632187ea1162cc7c9b747358fd3c723bd89ab778ee14ba9cac47f222c7b4`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9bfa10e94b8f2ff156d0e20f66b2d903d92dd9f6e7b790c7aceb25a71c071036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341dab6e3fce0075f1c08c28e1201d4d08cc753ac5e50143d4ecf66d5d4fd547`

```dockerfile
```

-	Layers:
	-	`sha256:34678b811459c3e99a3a650cdc6638109c0d80d92c800c6678b26314b5f309c4`  
		Last Modified: Fri, 14 Nov 2025 01:50:02 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8-jammy`

```console
$ docker pull clickhouse@sha256:6aef4b3c7197eadee1ebd1c8d6f69b99f33ec3c6c0f11c72eba0b840d87b5c11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.8-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:7cc58df1643fd52b0ca3383515fd8f31d1f139d67915649c969797cad6a354af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227833996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7aeb0043cc0bf471c3bfe8d6e479602da58acba8e3209f6765d3d4ddfe931f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:39 GMT
ARG VERSION=25.8.11.66
# Thu, 13 Nov 2025 23:09:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:27 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:11:27 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:11:27 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:11:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49009f2b2c2df1a49119795bda88cde6e506edbff6400db80ecd8d86d116b501`  
		Last Modified: Thu, 13 Nov 2025 23:10:39 GMT  
		Size: 7.6 MB (7598523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005342a1838b259d962a4cf009039849846ccc8ea03343a19a652ed39af17fe6`  
		Last Modified: Fri, 14 Nov 2025 01:50:41 GMT  
		Size: 189.8 MB (189828651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece9f4b41dc9b366993db6769e2ccbabaedc53c61f118a490f71226b4109c2b8`  
		Last Modified: Thu, 13 Nov 2025 23:11:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df89e3dd735bdb60842d324ca69a0cdf08ea627d5715954be9c02a7bddc083fd`  
		Last Modified: Thu, 13 Nov 2025 23:11:59 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d540a46cec9e08a70070c5473f907ef9ebd343b1455e35ead22101f33f16d5aa`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13489c6a19ffae6ca4a1a697997abfea421d97dc0e4d329cfdec851a1a58dc8`  
		Last Modified: Thu, 13 Nov 2025 23:11:59 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2669082c40680a175603060ead5872da333f97d1adce6e9e5053915731f29727`  
		Last Modified: Thu, 13 Nov 2025 23:11:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bcd7a2a953ddb47c85d97e4e32ba098dab2a4efd2cc7966bfdd03c31009de2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468fd697778fed7af280221c44238083efc701a93d2852f0d33bcf1c55d14988`

```dockerfile
```

-	Layers:
	-	`sha256:3f0ac54eef11d20388b7f190f1980fd3456d080d2931f37a9d1d075ac0661437`  
		Last Modified: Fri, 14 Nov 2025 01:49:59 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.8-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e55a58f599f187e7158d26961cb7da1033e3787999595aae7ff8f01ba2fcd741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212646216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b13d2311cccbdb9a36bcd1f7f5c229d955417df764572854968cee1ad2d2903`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:31 GMT
ARG VERSION=25.8.11.66
# Thu, 13 Nov 2025 23:09:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:27 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:11:27 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:11:27 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:11:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41daf4310e4fd0bfd906fb1dd237436605457dfdf700a83ca5ae05cfccbe3813`  
		Last Modified: Thu, 13 Nov 2025 23:10:28 GMT  
		Size: 7.6 MB (7576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69beadc0132fd0ac430847591b7fc587c7315d8c02b468441b0d152bdb69849f`  
		Last Modified: Fri, 14 Nov 2025 01:50:43 GMT  
		Size: 176.8 MB (176815517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3de0d633a907044d9de2a16b105e20461f6de9c5f7e8e53aad3f962f6447e7`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142026ec3e591d8ec720b560cb7dff225329e0b6188d6c182f25a64dff3b81bc`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d540a46cec9e08a70070c5473f907ef9ebd343b1455e35ead22101f33f16d5aa`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2345173a6e1bee0c60380913799dfbbe2556aba6ca21d90e069c7ab1eeb5267`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b6632187ea1162cc7c9b747358fd3c723bd89ab778ee14ba9cac47f222c7b4`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.8-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9bfa10e94b8f2ff156d0e20f66b2d903d92dd9f6e7b790c7aceb25a71c071036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341dab6e3fce0075f1c08c28e1201d4d08cc753ac5e50143d4ecf66d5d4fd547`

```dockerfile
```

-	Layers:
	-	`sha256:34678b811459c3e99a3a650cdc6638109c0d80d92c800c6678b26314b5f309c4`  
		Last Modified: Fri, 14 Nov 2025 01:50:02 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.8.12`

**does not exist** (yet?)

## `clickhouse:25.8.12-jammy`

**does not exist** (yet?)

## `clickhouse:25.8.12.129`

**does not exist** (yet?)

## `clickhouse:25.8.12.129-jammy`

**does not exist** (yet?)

## `clickhouse:25.9`

```console
$ docker pull clickhouse@sha256:a2bbe928375005160b8e5971f2e796d7ccc45fc929bd51a572c457c1913a77f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9` - linux; amd64

```console
$ docker pull clickhouse@sha256:576ebc6f9f33f88062c10aaca04e6a48409e39235fdc62483c0a7ab48cee8ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228850078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96fe8cc9ee47a343d3711d56bed3bea4f83e98afb5170e834350d63247762b8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:39 GMT
ARG VERSION=25.9.5.21
# Thu, 13 Nov 2025 23:09:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:10:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:10:06 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:10:06 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:10:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:10:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:10:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:10:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:10:06 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:10:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:10:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49009f2b2c2df1a49119795bda88cde6e506edbff6400db80ecd8d86d116b501`  
		Last Modified: Thu, 13 Nov 2025 23:10:39 GMT  
		Size: 7.6 MB (7598523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888f41dda202e159ec6e2c8f0bfea5c84529a2b381c26a42eaa8962403bb9d5f`  
		Last Modified: Fri, 14 Nov 2025 01:50:56 GMT  
		Size: 190.8 MB (190844730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92564939577a8b0d5dd8533661894a66650cf632f3b5f08a5c5bb02eb68c318`  
		Last Modified: Thu, 13 Nov 2025 23:10:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c7e692fbf93a43a2687546aff3a4e88834d4ac3d8e91a6f6605e0be0c2bd26`  
		Last Modified: Thu, 13 Nov 2025 23:10:39 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3744e8373ca98c0ed74b20dee68d61a5fc4c66af753181eeb2128b484168dc8`  
		Last Modified: Thu, 13 Nov 2025 23:10:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febc55e32466063aca4419effdb6176e32e9918089805e093462cf567f50956b`  
		Last Modified: Thu, 13 Nov 2025 23:10:39 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a686c58e73a7bd60b59f1dc2a2324710aec63fb71cc7cec28478b753db3cfa`  
		Last Modified: Thu, 13 Nov 2025 23:10:39 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dac770f255dc9f8c1c97974b6668eaf9ae95914c760ff67a24145afa18c7e592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeed3540fcd3025ccd741b1df21add54d557509a1f493d7577e0b441d830ff9a`

```dockerfile
```

-	Layers:
	-	`sha256:86d519e97b9a4b9d1632c6a49289d799d510df0d1258c994d664c7560942b077`  
		Last Modified: Fri, 14 Nov 2025 01:50:17 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f81623ff6a772c3a122a62a0e8f1a6a367a842a9b213385a2c22afd138c73967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214127475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7d9e1785a4e633e5108b0425ca89cc0aafde2824771612f977ac94b0ced711`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:10:05 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:10:05 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:10:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:10:05 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:10:05 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:10:05 GMT
ARG VERSION=25.9.5.21
# Thu, 13 Nov 2025 23:10:05 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:10:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:10:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:10:32 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:10:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:10:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:10:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:10:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:10:32 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:10:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:10:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6870ee054db774056a3a73ebe8cc3bb8cd7530b511a595287a52d875c516aef3`  
		Last Modified: Thu, 13 Nov 2025 23:11:01 GMT  
		Size: 7.6 MB (7576766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add3c45521b02f843d7f37d238309011d63debf35005c19e8152950790db7b7c`  
		Last Modified: Fri, 14 Nov 2025 01:50:49 GMT  
		Size: 178.3 MB (178296816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad7aedadb8481f6492aeed058a103d4b8fdeee0d088b677a2430e24c69a4848`  
		Last Modified: Thu, 13 Nov 2025 23:11:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f59c43c4d42307976d11d06627b06fc559044c989f05d805f68deec8b52447c`  
		Last Modified: Thu, 13 Nov 2025 23:11:01 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324b13b7eb447655092f0919f027c907879455118fa6f262f68eece9f6b8506`  
		Last Modified: Thu, 13 Nov 2025 23:11:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0850ef52d7a640d9f805eee9648422f152fe789d2eeac4b3b33092d4e04f8997`  
		Last Modified: Thu, 13 Nov 2025 23:11:01 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab9638a1a8f79db0867290383ba091bb84fc55c92c0d0d6752a525bb02a57b`  
		Last Modified: Thu, 13 Nov 2025 23:11:01 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4e3b17d7b6c3df573e525a60f47c4a7de553731cb1d851d187185c637b5bfbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797fab4065e05e572faf4c2a6e177662379dc85d0b317853bf50f71dd9367264`

```dockerfile
```

-	Layers:
	-	`sha256:e5f7834eeae1473e7e03ba30fd45000a2288896285441ede5d1fec52e6b80e97`  
		Last Modified: Fri, 14 Nov 2025 01:50:21 GMT  
		Size: 25.6 KB (25605 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9-jammy`

```console
$ docker pull clickhouse@sha256:a2bbe928375005160b8e5971f2e796d7ccc45fc929bd51a572c457c1913a77f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:25.9-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:576ebc6f9f33f88062c10aaca04e6a48409e39235fdc62483c0a7ab48cee8ae0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228850078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b96fe8cc9ee47a343d3711d56bed3bea4f83e98afb5170e834350d63247762b8`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:39 GMT
ARG VERSION=25.9.5.21
# Thu, 13 Nov 2025 23:09:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:10:04 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:10:06 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:10:06 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:10:06 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:10:06 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:10:06 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:10:06 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:10:06 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:10:06 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:10:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49009f2b2c2df1a49119795bda88cde6e506edbff6400db80ecd8d86d116b501`  
		Last Modified: Thu, 13 Nov 2025 23:10:39 GMT  
		Size: 7.6 MB (7598523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888f41dda202e159ec6e2c8f0bfea5c84529a2b381c26a42eaa8962403bb9d5f`  
		Last Modified: Fri, 14 Nov 2025 01:50:56 GMT  
		Size: 190.8 MB (190844730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92564939577a8b0d5dd8533661894a66650cf632f3b5f08a5c5bb02eb68c318`  
		Last Modified: Thu, 13 Nov 2025 23:10:39 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c7e692fbf93a43a2687546aff3a4e88834d4ac3d8e91a6f6605e0be0c2bd26`  
		Last Modified: Thu, 13 Nov 2025 23:10:39 GMT  
		Size: 865.8 KB (865751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3744e8373ca98c0ed74b20dee68d61a5fc4c66af753181eeb2128b484168dc8`  
		Last Modified: Thu, 13 Nov 2025 23:10:39 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febc55e32466063aca4419effdb6176e32e9918089805e093462cf567f50956b`  
		Last Modified: Thu, 13 Nov 2025 23:10:39 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a686c58e73a7bd60b59f1dc2a2324710aec63fb71cc7cec28478b753db3cfa`  
		Last Modified: Thu, 13 Nov 2025 23:10:39 GMT  
		Size: 3.6 KB (3612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:dac770f255dc9f8c1c97974b6668eaf9ae95914c760ff67a24145afa18c7e592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 KB (25418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeed3540fcd3025ccd741b1df21add54d557509a1f493d7577e0b441d830ff9a`

```dockerfile
```

-	Layers:
	-	`sha256:86d519e97b9a4b9d1632c6a49289d799d510df0d1258c994d664c7560942b077`  
		Last Modified: Fri, 14 Nov 2025 01:50:17 GMT  
		Size: 25.4 KB (25418 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:25.9-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:f81623ff6a772c3a122a62a0e8f1a6a367a842a9b213385a2c22afd138c73967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **214.1 MB (214127475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7d9e1785a4e633e5108b0425ca89cc0aafde2824771612f977ac94b0ced711`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:10:05 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:10:05 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:10:05 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:10:05 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:10:05 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:10:05 GMT
ARG VERSION=25.9.5.21
# Thu, 13 Nov 2025 23:10:05 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:10:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:10:32 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:10:32 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:10:32 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.9.5.21 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:10:32 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:10:32 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:10:32 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:10:32 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:10:32 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:10:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6870ee054db774056a3a73ebe8cc3bb8cd7530b511a595287a52d875c516aef3`  
		Last Modified: Thu, 13 Nov 2025 23:11:01 GMT  
		Size: 7.6 MB (7576766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add3c45521b02f843d7f37d238309011d63debf35005c19e8152950790db7b7c`  
		Last Modified: Fri, 14 Nov 2025 01:50:49 GMT  
		Size: 178.3 MB (178296816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad7aedadb8481f6492aeed058a103d4b8fdeee0d088b677a2430e24c69a4848`  
		Last Modified: Thu, 13 Nov 2025 23:11:01 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f59c43c4d42307976d11d06627b06fc559044c989f05d805f68deec8b52447c`  
		Last Modified: Thu, 13 Nov 2025 23:11:01 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1324b13b7eb447655092f0919f027c907879455118fa6f262f68eece9f6b8506`  
		Last Modified: Thu, 13 Nov 2025 23:11:01 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0850ef52d7a640d9f805eee9648422f152fe789d2eeac4b3b33092d4e04f8997`  
		Last Modified: Thu, 13 Nov 2025 23:11:01 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ab9638a1a8f79db0867290383ba091bb84fc55c92c0d0d6752a525bb02a57b`  
		Last Modified: Thu, 13 Nov 2025 23:11:01 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:25.9-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:4e3b17d7b6c3df573e525a60f47c4a7de553731cb1d851d187185c637b5bfbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.6 KB (25605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797fab4065e05e572faf4c2a6e177662379dc85d0b317853bf50f71dd9367264`

```dockerfile
```

-	Layers:
	-	`sha256:e5f7834eeae1473e7e03ba30fd45000a2288896285441ede5d1fec52e6b80e97`  
		Last Modified: Fri, 14 Nov 2025 01:50:21 GMT  
		Size: 25.6 KB (25605 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:25.9.6`

**does not exist** (yet?)

## `clickhouse:25.9.6-jammy`

**does not exist** (yet?)

## `clickhouse:25.9.6.117`

**does not exist** (yet?)

## `clickhouse:25.9.6.117-jammy`

**does not exist** (yet?)

## `clickhouse:jammy`

```console
$ docker pull clickhouse@sha256:c9739650884bcc5dd109c283ce545b87d58c0f751880aa425170a59604aec341
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:f0d8c09cd53e9787cb3ee8f7e8e7cfde488fdddcb0b0502469b80b3b8a84c4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231983240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2269ab9ff71a3eb770715c7a3fd75761efe8ef23a6c788abaa57f2e3cb78562`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:36 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 23:09:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:10:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:10:03 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:10:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:10:03 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:10:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:10:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bd02d54aca9e4b5dc021fa7f9e576a07e5be62fc7ee172d0ed4137944cacc9`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 7.6 MB (7598588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6316601fd9c34b60c5ca2605fa55d8290e2bd5ac69198cd0a53467a567f7fc83`  
		Last Modified: Fri, 14 Nov 2025 01:49:55 GMT  
		Size: 194.0 MB (193977827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba39390138026777c687e3508ed8fd34055ace99ecec73f69c797cafd8492cc5`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276dfe45586cc645faa4c6655eebeeee38ea04261463b342d877bb60f895e787`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5975ad1545a1b9982f545077922f5494e5c50dde1ed46614c6aa7b1ccac1dca1`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07b39058858cb54734eaea1eb73e6efcc4ab04b4dc823c4d49ae39c219cd92e`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abed04583b3f8484627b7110037ce3ab26c7588a582f0da788ee9733c83ff42`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ae05d5e36eeccc46858a9c47b42e6578e2fdcb657160f8fc633a3969c05d158d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604d4c960d9c1b2ffe0e50ce35b612b69e231b9afad0c7f6da252c01c5a4f6e6`

```dockerfile
```

-	Layers:
	-	`sha256:130306bcdc0b3daacdfe7da0deb2a61f1322af37824c618b9d715bde6aa88ba3`  
		Last Modified: Fri, 14 Nov 2025 01:49:24 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:eeb67abeca6c00dd7fac755651c7ed2042118211e8ee5e999ba9cdfdf56aaa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216505816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4601fbc006cdf774790f0afb3a7ab6d279f4acf3f6380c3ab0ff11a9bca50c9b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:31 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 23:09:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:09:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:09:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:09:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:09:58 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:09:58 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:09:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:09:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:09:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:09:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:09:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41daf4310e4fd0bfd906fb1dd237436605457dfdf700a83ca5ae05cfccbe3813`  
		Last Modified: Thu, 13 Nov 2025 23:10:28 GMT  
		Size: 7.6 MB (7576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0f5ce5c4571b4cd2464c78cbcd31672ad12226725a8e1232e8c3ef3620f9e0`  
		Last Modified: Fri, 14 Nov 2025 01:49:52 GMT  
		Size: 180.7 MB (180675112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e8a51714ff93bb140e12b0158c088b6cde1651b653c1e455860479be6303b3`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a87b3cb86dd50e65da599ed4a968edc62c5594830a198faad91aa3dcabcc814`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e50b7ab24f69fdcd396dd7a078c175c8467d0556dbc8b3fcc5380d6706706d8`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcd2bca9e63b0ebf70cbb92ffe0393da57cf1fb923a96941174aeb3097fcec6`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112adfbc3ee3dc6c7d4917a8ce15830879e6ca2aaeaeb47fa47375bc0c20b711`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:409797aa5d0365a362df23fc70f1d4ce92527bb13e6286b7c888e5248ab34776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cf6e4289fb787eb33803b732451b0a765a8ddcc8f98c1a84d2f72a690e44f7`

```dockerfile
```

-	Layers:
	-	`sha256:d4f623fa03cf7b7f07af675778466cf0ce1e0569ca834dc8872842cbdd413a01`  
		Last Modified: Fri, 14 Nov 2025 01:49:27 GMT  
		Size: 26.3 KB (26258 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:latest`

```console
$ docker pull clickhouse@sha256:c9739650884bcc5dd109c283ce545b87d58c0f751880aa425170a59604aec341
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:latest` - linux; amd64

```console
$ docker pull clickhouse@sha256:f0d8c09cd53e9787cb3ee8f7e8e7cfde488fdddcb0b0502469b80b3b8a84c4c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **232.0 MB (231983240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2269ab9ff71a3eb770715c7a3fd75761efe8ef23a6c788abaa57f2e3cb78562`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:36 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:36 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:36 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:36 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:36 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:36 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 23:09:36 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:10:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:02 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:10:03 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:10:03 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:10:03 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:10:03 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:10:03 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:10:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bd02d54aca9e4b5dc021fa7f9e576a07e5be62fc7ee172d0ed4137944cacc9`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 7.6 MB (7598588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6316601fd9c34b60c5ca2605fa55d8290e2bd5ac69198cd0a53467a567f7fc83`  
		Last Modified: Fri, 14 Nov 2025 01:49:55 GMT  
		Size: 194.0 MB (193977827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba39390138026777c687e3508ed8fd34055ace99ecec73f69c797cafd8492cc5`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276dfe45586cc645faa4c6655eebeeee38ea04261463b342d877bb60f895e787`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 865.8 KB (865752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5975ad1545a1b9982f545077922f5494e5c50dde1ed46614c6aa7b1ccac1dca1`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07b39058858cb54734eaea1eb73e6efcc4ab04b4dc823c4d49ae39c219cd92e`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abed04583b3f8484627b7110037ce3ab26c7588a582f0da788ee9733c83ff42`  
		Last Modified: Thu, 13 Nov 2025 23:10:42 GMT  
		Size: 3.6 KB (3610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:ae05d5e36eeccc46858a9c47b42e6578e2fdcb657160f8fc633a3969c05d158d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604d4c960d9c1b2ffe0e50ce35b612b69e231b9afad0c7f6da252c01c5a4f6e6`

```dockerfile
```

-	Layers:
	-	`sha256:130306bcdc0b3daacdfe7da0deb2a61f1322af37824c618b9d715bde6aa88ba3`  
		Last Modified: Fri, 14 Nov 2025 01:49:24 GMT  
		Size: 26.0 KB (26047 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:latest` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:eeb67abeca6c00dd7fac755651c7ed2042118211e8ee5e999ba9cdfdf56aaa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216505816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4601fbc006cdf774790f0afb3a7ab6d279f4acf3f6380c3ab0ff11a9bca50c9b`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:31 GMT
ARG VERSION=25.10.2.65
# Thu, 13 Nov 2025 23:09:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:09:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:09:57 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:09:58 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:09:58 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:09:58 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:09:59 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.10.2.65 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:09:59 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:09:59 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:09:59 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:09:59 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:09:59 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:09:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41daf4310e4fd0bfd906fb1dd237436605457dfdf700a83ca5ae05cfccbe3813`  
		Last Modified: Thu, 13 Nov 2025 23:10:28 GMT  
		Size: 7.6 MB (7576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0f5ce5c4571b4cd2464c78cbcd31672ad12226725a8e1232e8c3ef3620f9e0`  
		Last Modified: Fri, 14 Nov 2025 01:49:52 GMT  
		Size: 180.7 MB (180675112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e8a51714ff93bb140e12b0158c088b6cde1651b653c1e455860479be6303b3`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a87b3cb86dd50e65da599ed4a968edc62c5594830a198faad91aa3dcabcc814`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 865.7 KB (865749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e50b7ab24f69fdcd396dd7a078c175c8467d0556dbc8b3fcc5380d6706706d8`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcd2bca9e63b0ebf70cbb92ffe0393da57cf1fb923a96941174aeb3097fcec6`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112adfbc3ee3dc6c7d4917a8ce15830879e6ca2aaeaeb47fa47375bc0c20b711`  
		Last Modified: Thu, 13 Nov 2025 23:10:27 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:latest` - unknown; unknown

```console
$ docker pull clickhouse@sha256:409797aa5d0365a362df23fc70f1d4ce92527bb13e6286b7c888e5248ab34776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68cf6e4289fb787eb33803b732451b0a765a8ddcc8f98c1a84d2f72a690e44f7`

```dockerfile
```

-	Layers:
	-	`sha256:d4f623fa03cf7b7f07af675778466cf0ce1e0569ca834dc8872842cbdd413a01`  
		Last Modified: Fri, 14 Nov 2025 01:49:27 GMT  
		Size: 26.3 KB (26258 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts`

```console
$ docker pull clickhouse@sha256:6aef4b3c7197eadee1ebd1c8d6f69b99f33ec3c6c0f11c72eba0b840d87b5c11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts` - linux; amd64

```console
$ docker pull clickhouse@sha256:7cc58df1643fd52b0ca3383515fd8f31d1f139d67915649c969797cad6a354af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227833996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7aeb0043cc0bf471c3bfe8d6e479602da58acba8e3209f6765d3d4ddfe931f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:39 GMT
ARG VERSION=25.8.11.66
# Thu, 13 Nov 2025 23:09:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:27 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:11:27 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:11:27 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:11:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49009f2b2c2df1a49119795bda88cde6e506edbff6400db80ecd8d86d116b501`  
		Last Modified: Thu, 13 Nov 2025 23:10:39 GMT  
		Size: 7.6 MB (7598523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005342a1838b259d962a4cf009039849846ccc8ea03343a19a652ed39af17fe6`  
		Last Modified: Fri, 14 Nov 2025 01:50:41 GMT  
		Size: 189.8 MB (189828651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece9f4b41dc9b366993db6769e2ccbabaedc53c61f118a490f71226b4109c2b8`  
		Last Modified: Thu, 13 Nov 2025 23:11:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df89e3dd735bdb60842d324ca69a0cdf08ea627d5715954be9c02a7bddc083fd`  
		Last Modified: Thu, 13 Nov 2025 23:11:59 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d540a46cec9e08a70070c5473f907ef9ebd343b1455e35ead22101f33f16d5aa`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13489c6a19ffae6ca4a1a697997abfea421d97dc0e4d329cfdec851a1a58dc8`  
		Last Modified: Thu, 13 Nov 2025 23:11:59 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2669082c40680a175603060ead5872da333f97d1adce6e9e5053915731f29727`  
		Last Modified: Thu, 13 Nov 2025 23:11:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bcd7a2a953ddb47c85d97e4e32ba098dab2a4efd2cc7966bfdd03c31009de2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468fd697778fed7af280221c44238083efc701a93d2852f0d33bcf1c55d14988`

```dockerfile
```

-	Layers:
	-	`sha256:3f0ac54eef11d20388b7f190f1980fd3456d080d2931f37a9d1d075ac0661437`  
		Last Modified: Fri, 14 Nov 2025 01:49:59 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e55a58f599f187e7158d26961cb7da1033e3787999595aae7ff8f01ba2fcd741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212646216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b13d2311cccbdb9a36bcd1f7f5c229d955417df764572854968cee1ad2d2903`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:31 GMT
ARG VERSION=25.8.11.66
# Thu, 13 Nov 2025 23:09:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:27 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:11:27 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:11:27 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:11:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41daf4310e4fd0bfd906fb1dd237436605457dfdf700a83ca5ae05cfccbe3813`  
		Last Modified: Thu, 13 Nov 2025 23:10:28 GMT  
		Size: 7.6 MB (7576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69beadc0132fd0ac430847591b7fc587c7315d8c02b468441b0d152bdb69849f`  
		Last Modified: Fri, 14 Nov 2025 01:50:43 GMT  
		Size: 176.8 MB (176815517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3de0d633a907044d9de2a16b105e20461f6de9c5f7e8e53aad3f962f6447e7`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142026ec3e591d8ec720b560cb7dff225329e0b6188d6c182f25a64dff3b81bc`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d540a46cec9e08a70070c5473f907ef9ebd343b1455e35ead22101f33f16d5aa`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2345173a6e1bee0c60380913799dfbbe2556aba6ca21d90e069c7ab1eeb5267`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b6632187ea1162cc7c9b747358fd3c723bd89ab778ee14ba9cac47f222c7b4`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9bfa10e94b8f2ff156d0e20f66b2d903d92dd9f6e7b790c7aceb25a71c071036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341dab6e3fce0075f1c08c28e1201d4d08cc753ac5e50143d4ecf66d5d4fd547`

```dockerfile
```

-	Layers:
	-	`sha256:34678b811459c3e99a3a650cdc6638109c0d80d92c800c6678b26314b5f309c4`  
		Last Modified: Fri, 14 Nov 2025 01:50:02 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json

## `clickhouse:lts-jammy`

```console
$ docker pull clickhouse@sha256:6aef4b3c7197eadee1ebd1c8d6f69b99f33ec3c6c0f11c72eba0b840d87b5c11
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clickhouse:lts-jammy` - linux; amd64

```console
$ docker pull clickhouse@sha256:7cc58df1643fd52b0ca3383515fd8f31d1f139d67915649c969797cad6a354af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.8 MB (227833996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7aeb0043cc0bf471c3bfe8d6e479602da58acba8e3209f6765d3d4ddfe931f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:39 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:39 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:39 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:39 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:39 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:39 GMT
ARG VERSION=25.8.11.66
# Thu, 13 Nov 2025 23:09:39 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:27 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:11:27 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:11:27 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:11:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Mon, 13 Oct 2025 19:13:16 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49009f2b2c2df1a49119795bda88cde6e506edbff6400db80ecd8d86d116b501`  
		Last Modified: Thu, 13 Nov 2025 23:10:39 GMT  
		Size: 7.6 MB (7598523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005342a1838b259d962a4cf009039849846ccc8ea03343a19a652ed39af17fe6`  
		Last Modified: Fri, 14 Nov 2025 01:50:41 GMT  
		Size: 189.8 MB (189828651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece9f4b41dc9b366993db6769e2ccbabaedc53c61f118a490f71226b4109c2b8`  
		Last Modified: Thu, 13 Nov 2025 23:11:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df89e3dd735bdb60842d324ca69a0cdf08ea627d5715954be9c02a7bddc083fd`  
		Last Modified: Thu, 13 Nov 2025 23:11:59 GMT  
		Size: 865.8 KB (865750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d540a46cec9e08a70070c5473f907ef9ebd343b1455e35ead22101f33f16d5aa`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13489c6a19ffae6ca4a1a697997abfea421d97dc0e4d329cfdec851a1a58dc8`  
		Last Modified: Thu, 13 Nov 2025 23:11:59 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2669082c40680a175603060ead5872da333f97d1adce6e9e5053915731f29727`  
		Last Modified: Thu, 13 Nov 2025 23:11:59 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:bcd7a2a953ddb47c85d97e4e32ba098dab2a4efd2cc7966bfdd03c31009de2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 KB (26045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468fd697778fed7af280221c44238083efc701a93d2852f0d33bcf1c55d14988`

```dockerfile
```

-	Layers:
	-	`sha256:3f0ac54eef11d20388b7f190f1980fd3456d080d2931f37a9d1d075ac0661437`  
		Last Modified: Fri, 14 Nov 2025 01:49:59 GMT  
		Size: 26.0 KB (26045 bytes)  
		MIME: application/vnd.in-toto+json

### `clickhouse:lts-jammy` - linux; arm64 variant v8

```console
$ docker pull clickhouse@sha256:e55a58f599f187e7158d26961cb7da1033e3787999595aae7ff8f01ba2fcd741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.6 MB (212646216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b13d2311cccbdb9a36bcd1f7f5c229d955417df764572854968cee1ad2d2903`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 13 Oct 2025 17:25:16 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:25:18 GMT
ADD file:2e0e653363da35febc0204e69cb713c0d1497720522f79d3d531980a7f291a39 in / 
# Mon, 13 Oct 2025 17:25:18 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:09:31 GMT
ARG DEBIAN_FRONTEND=noninteractive
# Thu, 13 Nov 2025 23:09:31 GMT
ARG apt_archive=http://archive.ubuntu.com
# Thu, 13 Nov 2025 23:09:31 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com
RUN sed -i "s|http://archive.ubuntu.com|${apt_archive}|g" /etc/apt/sources.list     && groupadd -r clickhouse --gid=101     && useradd -r -g clickhouse --uid=101 --home-dir=/var/lib/clickhouse --shell=/bin/bash clickhouse     && apt-get update     && apt-get install --yes --no-install-recommends         busybox         ca-certificates         locales         tzdata         wget     && busybox --install -s     && rm -rf /var/lib/apt/lists/* /var/cache/debconf /tmp/* # buildkit
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPO_CHANNEL=stable
# Thu, 13 Nov 2025 23:09:31 GMT
ARG REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main
# Thu, 13 Nov 2025 23:09:31 GMT
ARG VERSION=25.8.11.66
# Thu, 13 Nov 2025 23:09:31 GMT
ARG PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
# Thu, 13 Nov 2025 23:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse local -q 'SELECT 1' >/dev/null 2>&1 && exit 0 || :     ; apt-get update     && apt-get install --yes --no-install-recommends         dirmngr         gnupg2     && mkdir -p /etc/apt/sources.list.d     && GNUPGHOME=$(mktemp -d)     && GNUPGHOME="$GNUPGHOME" gpg --batch --no-default-keyring         --keyring /usr/share/keyrings/clickhouse-keyring.gpg         --keyserver hkp://keyserver.ubuntu.com:80         --recv-keys 3a9ea1193a97b548be1457d48919f6bd2b48d754     && rm -rf "$GNUPGHOME"     && chmod +r /usr/share/keyrings/clickhouse-keyring.gpg     && echo "${REPOSITORY}" > /etc/apt/sources.list.d/clickhouse.list     && echo "installing from repository: ${REPOSITORY}"     && apt-get update     && for package in ${PACKAGES}; do         packages="${packages} ${package}=${VERSION}"     ; done     && apt-get install --yes --no-install-recommends ${packages} || exit 1     && rm -rf         /var/lib/apt/lists/*         /var/cache/debconf         /tmp/*     && apt-get autoremove --purge -yq dirmngr gnupg2     && chmod ugo+Xrw -R /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:26 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN clickhouse-local -q 'SELECT * FROM system.build_options'     && mkdir -p /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client     && chmod ugo+Xrw -R /var/lib/clickhouse /var/log/clickhouse-server /etc/clickhouse-server /etc/clickhouse-client # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN locale-gen en_US.UTF-8 # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
ENV LANG=en_US.UTF-8
# Thu, 13 Nov 2025 23:11:27 GMT
ENV TZ=UTC
# Thu, 13 Nov 2025 23:11:27 GMT
# ARGS: DEBIAN_FRONTEND=noninteractive apt_archive=http://archive.ubuntu.com REPO_CHANNEL=stable REPOSITORY=deb [signed-by=/usr/share/keyrings/clickhouse-keyring.gpg] https://packages.clickhouse.com/deb stable main VERSION=25.8.11.66 PACKAGES=clickhouse-client clickhouse-server clickhouse-common-static
RUN mkdir /docker-entrypoint-initdb.d # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
COPY docker_related_config.xml /etc/clickhouse-server/config.d/ # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 13 Nov 2025 23:11:27 GMT
EXPOSE map[8123/tcp:{} 9000/tcp:{} 9009/tcp:{}]
# Thu, 13 Nov 2025 23:11:27 GMT
VOLUME [/var/lib/clickhouse]
# Thu, 13 Nov 2025 23:11:27 GMT
ENV CLICKHOUSE_CONFIG=/etc/clickhouse-server/config.xml
# Thu, 13 Nov 2025 23:11:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:0ec3d86457676c7af7a3b6d29565e0e8b30ed98afe5d606e00e565101f812623`  
		Last Modified: Mon, 13 Oct 2025 22:06:29 GMT  
		Size: 27.4 MB (27383877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41daf4310e4fd0bfd906fb1dd237436605457dfdf700a83ca5ae05cfccbe3813`  
		Last Modified: Thu, 13 Nov 2025 23:10:28 GMT  
		Size: 7.6 MB (7576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69beadc0132fd0ac430847591b7fc587c7315d8c02b468441b0d152bdb69849f`  
		Last Modified: Fri, 14 Nov 2025 01:50:43 GMT  
		Size: 176.8 MB (176815517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3de0d633a907044d9de2a16b105e20461f6de9c5f7e8e53aad3f962f6447e7`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142026ec3e591d8ec720b560cb7dff225329e0b6188d6c182f25a64dff3b81bc`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 865.7 KB (865745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d540a46cec9e08a70070c5473f907ef9ebd343b1455e35ead22101f33f16d5aa`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2345173a6e1bee0c60380913799dfbbe2556aba6ca21d90e069c7ab1eeb5267`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b6632187ea1162cc7c9b747358fd3c723bd89ab778ee14ba9cac47f222c7b4`  
		Last Modified: Thu, 13 Nov 2025 23:11:56 GMT  
		Size: 3.6 KB (3611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clickhouse:lts-jammy` - unknown; unknown

```console
$ docker pull clickhouse@sha256:9bfa10e94b8f2ff156d0e20f66b2d903d92dd9f6e7b790c7aceb25a71c071036
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 KB (26257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:341dab6e3fce0075f1c08c28e1201d4d08cc753ac5e50143d4ecf66d5d4fd547`

```dockerfile
```

-	Layers:
	-	`sha256:34678b811459c3e99a3a650cdc6638109c0d80d92c800c6678b26314b5f309c4`  
		Last Modified: Fri, 14 Nov 2025 01:50:02 GMT  
		Size: 26.3 KB (26257 bytes)  
		MIME: application/vnd.in-toto+json
