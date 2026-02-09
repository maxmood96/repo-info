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
